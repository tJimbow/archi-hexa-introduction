##### Le Domaine => Les ports

```typescript
// domain/ProgramSearchPort.ts (Primary Port)
export interface ProgramSearchPort {
  searchPrograms(query: string): Promise<Program[]>;
}
```
<!-- .element: class="fragment" -->
```typescript
// domain/ProgramRepositoryPort.ts (Secondary Port)
export interface ProgramRepositoryPort {
  fetchPrograms(query: string): Promise<Program[]>;
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">Le domaine définit les Ports (Primary et Secondary) avec ses propres types</li>
  <li class="fragment">Ne connaît <strong>pas</strong> l'implémentation concrète</li>
</ul>