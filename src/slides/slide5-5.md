##### Infrastructure => Secondary Adapter

```typescript
// infrastructure/secondary/ProgramResponse.ts (Response)
interface ProgramResponse {
	id: string;
	// ... autres propriétés de l'API externe
}
```
<!-- .element: class="fragment" -->
```typescript
// infrastructure/secondary/ProgramRepositoryAdapter.ts (Secondary Adapter)
export class ProgramRepositoryAdapter implements ProgramRepositoryPort {
	constructor(private httpClient: AxiosInstance) {}
    
	async fetchPrograms(params: SearchProgramParameters): Promise<Program[]> {
		const response = await this.httpClient.get<ProgramResponse[]>('/api/programs', {
			params: toApiParams(params)
		});
		
		return response.data.map(data => Program.fromResponse(data));
	}
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">C'est l'ADAPTER qui fait la transformation des types externes vers les types du domaine</li>
  <li class="fragment">L'infrastructure dépend du domaine : elle s'adapte aux interfaces définies par le domaine</li>
  <li class="fragment">Implémente le port secondaire</li>
  <li class="fragment">Elle connaît les types externes (ProgramResponse) et fait la transformation</li>
</ul>