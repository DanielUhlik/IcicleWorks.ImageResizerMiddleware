# Register middleware

>Startup.cs: 

```
public void ConfigureServices(IServiceCollection services)
{
    ...
    services.AddImageResizer();

}

public void Configure(IApplicationBuilder app, IHostingEnvironment env, ILoggerFactory loggerFactory)
{
    app.UseImageResizer();
}
```


# Usage

`<img src="/image.jpg?w=1000&quality=70" />`

## Options

Url parameter | Type | Value |
|------|------|--------|
| w | int | 0 - x |
| h | int | 0 - x | 
| autorotate | bool | true / false |
| quality | int | 0 - 100 |
| mode  | string | pad, max, crop, stretch |
