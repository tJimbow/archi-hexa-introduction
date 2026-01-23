##### Le Domaine => Les services/use cases

```typescript
// domain/ProgramSearchService.ts (Use Case)
export class ProgramSearchService implements ProgramSearchPort {
  constructor(private repository: ProgramRepositoryPort) {}

  async searchPlannedPrograms(params: SearchProgramsParameters)
      : Promise<Program[]> {
    const programs = await this.repository.fetchPrograms(params);
    // Règles métier : filtrage, tri, validation...
    return programs.filter(p => p.isPlanned());
  }
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">Il contient les Use Cases qui orchestrent la logique métier</li>
  <li class="fragment">C'est dans ce cas-là l'implémentation du port primaire</li>
</ul>