#### Adaptateur SECONDAIRE : Implémente le Port

**Côté droit : Fournit l'implémentation (Driven)**<!-- .element: class="fragment" -->

```typescript
// ADAPTATEUR SECONDAIRE (Infrastructure)
class ProgramSearch implements ProgramSearchPort {
	constructor(private readonly http: Producer<AxiosInstance>) {}
    
	async for(params: SearchParams): Promise<SearchResult> {
		// IMPLÉMENTE le contrat avec Axios
		return this.http().post(API_URL, params);
	}
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">✅ <strong>Implémente</strong> l'interface définie par le domaine</li>
  <li class="fragment">✅ Peut être remplacé facilement (ex: Axios → Fetch)</li>
</ul>
