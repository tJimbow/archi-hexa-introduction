#### Le PORT : 

```typescript
interface ProgramSearchPort {
  for(params: SearchParams): Promise<SearchResult>;
}
```
<!-- .element: class="fragment" -->
```typescript
export interface ProgramCancelPort {
	for(programs: ProgramIdsToCancelByEntCodeAndType)
	    : Promise<CancelledProgram[]>;
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment"><strong>Utilisé par</strong> : Adaptateurs Primaires (UI, Controllers) via injection de dépendance</li>
  <li class="fragment"><strong>Implémenté par</strong> : Adaptateurs Secondaires (Infrastructure)</li>
</ul>
