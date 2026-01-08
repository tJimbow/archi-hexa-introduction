#### Un exemple d'une requête

```csharp
public class ProgramQuery : IRequest<Program>
{
    public int ProgramId { get; set; }

    public sealed class ProgramQueryHandler(IProgramStore store)
        : IRequestHandler<ProgramQuery, Program?>
    {
        public ValueTask<Program?> Handle(
            ProgramQuery request,
            CancellationToken cancellationToken
        )
        {
            if (programId < 1) 
            { 
                throw new ArgumentException(nameof(programId)); 
            }

            return store.GetProgramAsync(request.ProgramId,
                cancellationToken);
        }
    }
}
```

<!--
=> Bon endroit por FluentValidation
--!>
