```
namespace Microsoft.Examples.Controllers
{
    using Microsoft.AspNetCore.Mvc;
    [ApiVersion( "1.0" )]
    [ApiVersion( "1.1" )]
    [ApiVersion( "1.0.1" )]
    [ApiVersion( "1.0.2" )]
    [ApiVersion( "1.2" )]
    [ApiVersion( "1.2.2" )]
    [Route( "api/[controller]" )]
    public class ValuesController : Controller
    {
        // GET api/values?api-version=1.0
        [HttpGet, MapToApiVersion( "1.0" )]
        public string GetV1() => $"Controller = {GetType().Name}\nVersion V1.0";

        [HttpGet, MapToApiVersion( "1.1" )]
        public string GetV11() => $"Controller = {GetType().Name}\nVersion V1.1";

        [HttpGet, MapToApiVersion( "1.0.1" )]
        public string GetV12X() => $"Controller = {GetType().Name}\nVersion V1.0.1";

        [HttpGet, MapToApiVersion( "1.0.2" )]
        public string GetV12() => $"Controller = {GetType().Name}\nVersion V1.0.2";

        [HttpGet, MapToApiVersion( "1.2" )]
        public string GetV22() => $"Controller = {GetType().Name}\nVersion V1.2";

        [HttpGet, MapToApiVersion( "1.2.2" )]
        public string GetV222() => $"Controller = {GetType().Name}\nVersion V1.2.2";
    }
}
```
