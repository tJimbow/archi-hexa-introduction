#### Adaptateur PRIMAIRE : Utilise le Port

**Côté gauche : Pilote l'application (Driving)**<!-- .element: class="fragment" -->

```typescript
// Vue.js Component - ADAPTATEUR PRIMAIRE
const programSearch = inject<ProgramSearchPort>(PROGRAM_SEARCH);
```
<!-- .element: class="fragment" -->
```typescript
async function search() {
  // UTILISE l'interface (le port)
  const results = await programSearch.for(searchParams);
}
```
<!-- .element: class="fragment" -->
<ul>
  <li class="fragment">✅ <strong>Injecte</strong> et <strong>consomme</strong> le port</li>
  <li class="fragment">✅ Ne connaît <strong>pas</strong> l'implémentation concrète</li>
</ul>
