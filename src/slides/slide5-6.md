##### L'Infrastructure => Adaptateurs primaires

```typescript
// infrastructure/primary/components/SearchProgram.vue (Composant Vue)
const programSearchService 
    = inject<ProgramSearchPort>('programSearchService');

const searchPrograms = async (query: string) => {
  const programs = await programSearchService.searchPrograms(query);
};
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">L'infrastructure dépend du domaine : elle s'adapte aux interfaces définies par le domaine</li>
  <li class="fragment">Implémente le port primaire</li>
</ul>