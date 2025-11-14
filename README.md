# Architecture Hexagonale - Support de Formation
Support de formation sur l'architecture hexagonale créé avec Reveal.js et TypeScript.
## 🚀 Démarrage rapide
### Installation
```bash
npm install
```
### Lancement en mode développement
```bash
npm run dev
```
### Build pour la production
```bash
npm run build
```
## 📊 Structure de la présentation
### 1. **Introduction** (Slide 1)
Titre et présentation générale de la formation
### 2. **Le Problème** (Slide 2)
- Architecture traditionnelle en couches
- Problèmes de couplage fort
- Difficultés de test et d'évolution
### 3. **Qu'est-ce que l'Architecture Hexagonale ?** (Slide 3 + sous-slides)
- Définition et origine (Alistair Cockburn, 2005)
- **Sous-slide 3.1** : Principe fondamental
- **Sous-slide 3.2** : Pourquoi "hexagonale" ?
### 4. **Les 3 Couches Principales** (Slide 4)
- Le Domaine (Domain)
- Les Ports
- Les Adaptateurs (Adapters)
### 5. **Ports & Adaptateurs : Détails** (Slide 5 + sous-slides)
- Introduction aux ports
- **Sous-slide 5.1** : Ports entrants (Driving/Primary) avec exemple TypeScript
- **Sous-slide 5.2** : Ports sortants (Driven/Secondary) avec exemple TypeScript
- **Sous-slide 5.3** : Types d'adaptateurs (Driving et Driven)
### 6. **Structure de Projet** (Slide 6)
Organisation recommandée des fichiers et dossiers
### 7. **Exemple Concret** (Slide 7 + sous-slide)
- Cas d'usage : Création d'un utilisateur
- **Sous-slide 7.1** : Flux complet d'une requête
### 8. **Avantages** (Slide 8)
- Testabilité
- Flexibilité
- Focus métier
- Isolation
- Maintenabilité
- Indépendance
### 9. **Inconvénients et Défis** (Slide 9)
- Complexité initiale
- Temps de développement
- Courbe d'apprentissage
- Risque de sur-engineering
### 10. **Points Clés à Retenir** (Slide 10)
Résumé et ressources pour aller plus loin
## 📁 Structure du projet
```
archi-hexa-introduction/
├── src/
│   ├── Slides/           # Fichiers Markdown des slides
│   │   ├── slide1.md     # Titre
│   │   ├── slide2.md     # Le problème
│   │   ├── slide3.md     # Définition
│   │   ├── slide3-1.md   # └─ Principe fondamental
│   │   ├── slide3-2.md   # └─ Pourquoi hexagonale
│   │   ├── slide4.md     # Les 3 couches
│   │   ├── slide5.md     # Ports & Adaptateurs
│   │   ├── slide5-1.md   # └─ Ports entrants
│   │   ├── slide5-2.md   # └─ Ports sortants
│   │   ├── slide5-3.md   # └─ Types d'adaptateurs
│   │   ├── slide6.md     # Structure de projet
│   │   ├── slide7.md     # Exemple concret
│   │   ├── slide7-1.md   # └─ Flux complet
│   │   ├── slide8.md     # Avantages
│   │   ├── slide9.md     # Inconvénients
│   │   └── slide10.md    # Conclusion
│   ├── main.ts           # Configuration Reveal.js
│   └── style.css
├── index.html            # Point d'entrée
├── package.json
└── README.md
```
## 🎮 Navigation
- **← →** : Navigation horizontale entre les slides principales
- **↑ ↓** : Navigation verticale dans les sous-slides
- **Esc** : Vue d'ensemble de toutes les slides
- **S** : Mode présentateur avec notes
- **F** : Plein écran
## 🛠️ Technologies utilisées
- **Reveal.js** : Framework de présentation
- **TypeScript** : Langage de programmation
- **Vite** : Build tool et dev server
- **Markdown** : Format des slides
## 📚 Ressources
- [Hexagonal Architecture - Alistair Cockburn](https://alistair.cockburn.us/hexagonal-architecture/)
- [Clean Architecture - Robert C. Martin](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [Domain-Driven Design (DDD)](https://martinfowler.com/tags/domain%20driven%20design.html)
## 📝 Personnalisation
Les slides sont au format Markdown dans le dossier `src/Slides/`. Vous pouvez :
- Modifier le contenu de chaque slide individuellement
- Ajouter de nouvelles slides en créant de nouveaux fichiers `.md`
- Changer le thème dans `src/main.ts` (moon, black, white, league, etc.)
- Personnaliser les styles dans `src/style.css`
## 📄 Licence
Projet éducatif - Libre d'utilisation pour la formation
