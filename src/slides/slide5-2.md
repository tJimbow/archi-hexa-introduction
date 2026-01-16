##### Le Domaine => Les ports


```typescript
// Port primaire
// domain/ProgramSearchPort.ts 
export interface ProgramSearchPort {
  searchPrograms(query: string): Promise<Program[]>;
}
```
<!-- .element: class="fragment" -->
```typescript
// Port secondaire
// domain/ProgramRepositoryPort.ts
export interface ProgramRepositoryPort {
  fetchPrograms(query: string): Promise<Program[]>;
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">Le domaine définit les Ports (Primary et Secondary) avec ses propres types</li>
  <li class="fragment">Ne connait <strong>pas</strong> l'implémentation concrète</li>
</ul>