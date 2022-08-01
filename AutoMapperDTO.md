# ASP.Net Core DTO and Auto Mapper

PlatformService.csproj:

- Add AutoMapper package

```c#
<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>net5.0</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="AutoMapper.Extensions.Microsoft.DependencyInjection" Version="8.1.1" />
    .
    .
    .
  </ItemGroup>

  <ItemGroup>
    <Protobuf Include="Protos\platforms.proto" GrpcServices="Server" />
  </ItemGroup>

</Project>
```

PlatformCreateDto.cs:

```c#
namespace PlatformService.Dtos
{
    public class PlatformCreateDto
    {
        [Required]
        public string Name { get; set; }

        [Required]
        public string Publisher { get; set; }

        [Required]
        public string Cost { get; set; }
    }
}
```

PlatformReadDto.cs:

```c#

namespace PlatformService.Dtos
{
    public class PlatformReadDto
    {
        public int Id { get; set; }

        public string Name { get; set; }

        public string Publisher { get; set; }

        public string Cost { get; set; }
    }
}
```

Startup.cs

```c#
public void ConfigureServices(IServiceCollection services)
{
    .
    .
    .

    services.AddControllers();
    services.AddAutoMapper(AppDomain.CurrentDomain.GetAssemblies());

    .
    .
    .
}
```

PlatformsProfile.cs:

```c#
using AutoMapper;
using PlatformService.Dtos;
using PlatformService.Models;

namespace PlatformService.Profiles
{
    public class PlatformsProfile : Profile
    {
        public PlatformsProfile()
        {
            // Source -> Target
            CreateMap<Platform, PlatformReadDto>();
            CreateMap<PlatformCreateDto, Platform>();
        }
    }
}
```

In Controller:

```c#
var platformReadDto = _mapper.Map<PlatformReadDto>(platformModel);
```

- [Reference](https://youtu.be/DgVjEo3OGBI?t=5807)
- [The case for two-way mapping in AutoMapper](https://lostechies.com/jimmybogard/2009/09/18/the-case-for-two-way-mapping-in-automapper)
- [Mapping domain model to view model via AutoMapper or not](https://stackoverflow.com/questions/16527921/mapping-domain-model-to-view-model-via-automapper-or-not)
