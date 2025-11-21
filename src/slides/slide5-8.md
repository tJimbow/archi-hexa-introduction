##### Application

```typescript
// main.ts (Bootstrap de l'application)
const httpClient 
    = axios.create({ baseURL: 'https://api.example.com' });
const programRepository 
    = new ProgramRepositoryAdapter(httpClient);
const programSearchService 
    = new ProgramSearchService(programRepository);

app.provide('programSearchService', programSearchService);
```
<!-- .element: class="fragment" -->
<ul>
    <li class="fragment">Elle gère les détails techniques (HTTP, BDD, etc.)</li>
    <li class="fragment">On injecte ici les dépendances</li>
</ul>
