#### Un exemple d'un port driven

```csharp
namespace Example.Domain.Port.Driven;

public interface IInboundProgramPort
{
    public ValueTask<IEnumerable<Program>> FetchProgramsAsync
    (
        DateTimeOffset start, 
        DateTimeOffset end, 
        CancellationToken cancellationToken = default
    );

    public ValueTask<Program?> FetchProgramAsync
    (
        int programId, 
        CancellationToken cancellationToken = default
    );
}
```
