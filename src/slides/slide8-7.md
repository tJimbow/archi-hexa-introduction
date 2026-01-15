#### Un exemple d'un port driving

```csharp
namespace Example.Domain.Port.Driving;

public interface IProgramStore
{
    public ValueTask<IEnumerable<Program>> GetCurrentProgramsAsync(
        CancellationToken cancellationToken = default
    );

    public ValueTask<Program> GetProgramAsync(
        int programId,
        CancellationToken cancellationToken = default
    );
}
```
<!--
=> Modelisation d'un objet qui va avoir une implementation qui utilise un ou plusieurs ports driven.
=> Ça implique un peu de logique, mais dans le cas le plus basique, on peut voir un simple emballage.
--!>
