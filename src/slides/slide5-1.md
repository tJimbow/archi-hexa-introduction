##### Le Domaine => Les entités

```typescript
// domain/Program.ts (Entité métier)
export class Program {
  constructor(
    public id: string,
    public name: string,
    public startDate: Date
  ) {}

  isValid(): boolean {
    return this.startDate > new Date();
  }
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">Le domaine contient les entités avec les règles métiers</li>
</ul>