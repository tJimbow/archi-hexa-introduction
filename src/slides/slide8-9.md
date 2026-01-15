#### Un exemple d'une implementation d'un port driven

```csharp
namespace Example.Implementation.Api;

public interface ApiProgramAdapter(HttpClient client)
    : IInboundProgramPort
{
    public ValueTask<Program> FetchProgramAsync
    (
        int programId, 
        CancellationToken cancellationToken = default
    )
    {
        var response =
            await client.GetAsync($"/programId/{programId}", 
                cancellationToken);

        var content =
            await response.Content
                .ReadAsStringAsync(cancellationToken);

        var dto = JsonSerializer.Deserialize<ProgramDto>(content); 
        return dto.ToModel();       
    }
}
```
