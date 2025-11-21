##### Le Domaine => Les services/use cases

```typescript
// domain/ProgramSearchService.ts (Use Case)
export class ProgramSearchService implements ProgramSearchPort {
  constructor(private repository: ProgramRepositoryPort) {}

  async searchPrograms(params: SearchProgramsParameters)
      : Promise<Program[]> {
    const programs = await this.repository.fetchPrograms(params);
    // Règles métier : filtrage, tri, validation...
    return programs.filter(p => p.isValid());
  }
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">Il contient les Use Cases qui orchestrent la logique métier</li>
</ul>