##### L'Infrastructure => Adaptateurs primaires

```typescript
// infrastructure/primary/components/SearchProgram.vue (Composant Vue)
const programSearch 
    = inject<ProgramSearchPort>('programSearchService');

const foundPrograms = async (params: SearchProgramsParameters) => {
  const programs = await programSearch.searchPlannedPrograms(params);
};
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">L'infrastructure dépend du domaine : elle s'adapte aux interfaces définies par le domaine</li>
  <li class="fragment">Utilise le port primaire</li>
</ul>