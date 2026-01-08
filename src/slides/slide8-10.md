#### Un exemple d'une implementation d'un port driving

```csharp
namespace Example.Implementation;

public interface ProgramStore(IInboundProgramPort inboundPort)
    : IProgramStore
{
    public ValueTask<Program?> GetProgramAsync(
        int programId,
        CancellationToken cancellationToken = default
    )
    {
        var program = inboundPort.FetchProgramAsync(programId, 
            cancellationToken);
            
        if (program.Obsolete) { return null; }
        return program;
    }
}
```
