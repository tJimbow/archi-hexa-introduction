#### Un exemple d'une fonction AZF

```csharp
public class ProgramsFunction(IMediator mediator)
{
    [Function("GetProgram")]
    public async Task<IActionResult> GetProgramAsync(
        HttpRequest request,
        int programId
    )
    {
        ArgumentNullException.ThrowIfNull(request);

        var query = new ProgramQuery { ProgramId = programId };
        var prog = await mediator.Send(query);
        if (prog is null)
        {
            return new NotFoundResult();
        }

        return new OkObjectResult(prog.ToDto());
    }
}
```
