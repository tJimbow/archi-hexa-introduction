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
- **Sous-slide 3.3** : 📐 Schéma détaillé de l'architecture avec Primary/Secondary
### 4. **Les 3 Couches Principales** (Slide 4 + sous-slides)
- Introduction aux 3 couches
- **Sous-slide 4.1** : 1️⃣ Le Domaine (Domain) - Entités, règles métier (HTML avec fragments)
- **Sous-slide 4.2** : 2️⃣ Les Ports - Interfaces et contrats (HTML avec fragments, Primary/Secondary)
- **Sous-slide 4.3** : 3️⃣ Les Adaptateurs - Implémentations concrètes
- **Sous-slide 4.4** : Détails supplémentaires
### 5. **Ports & Adaptateurs : Détails** (Slide 5 + sous-slides)
- Introduction aux ports et adaptateurs
- **Sous-slide 5.1** : Distinction Port vs Adapter
- **Sous-slide 5.2** : Exemple de code - Le Domaine (Ports Primary/Secondary, Use Case, Entité)
- **Sous-slide 5.3** : Le PORT - Interface définie dans le domaine
- **Sous-slide 5.4** : L'Infrastructure - Adapters et injection de dépendances
- **Sous-slide 5.5** : Port vs Adapter - Schéma SVG avec exemple ProgramSearch
- **Sous-slide 5.6** : Adaptateurs Primaires (Primary Adapters)
- **Sous-slide 5.7** : Adaptateurs Secondaires (Secondary Adapters)
- **Sous-slide 5.8** : Les Ports - Détails Primary et Secondary
- **Sous-slide 5.9** : Injection de dépendances avec Vue.js
### 6. **Cas d'Usage et Scénarios** (Slide 6 + sous-slides)
- Introduction aux cas d'usage concrets
- **Sous-slide 6.1** : Scénario 1
- **Sous-slide 6.2** : Scénario 2
- **Sous-slide 6.3** : Scénario 3
- **Sous-slide 6.4** : Scénario 4
- **Sous-slide 6.5** : Scénario 5
### 7. **Structure de Projet** (Slide 7)
Organisation recommandée avec exemple ProgramSearch :
- **Organisation des ports** : `domain/ports/primary/` et `domain/ports/secondary/`
- **Infrastructure séparée** : `infrastructure/primary/` (Primary Adapters) et `infrastructure/secondary/` (Secondary Adapters)
- **Bootstrap** : `main.ts` à la racine de `/src` pour l'injection de dépendances
### 8. **Avantages & Inconvénients** (Slide 8 + sous-slides)
- Titre principal ⚖️
- **Sous-slide 8.1** : ✅ Avantages (Testabilité, Flexibilité, Gestion des dépendances, Maintenabilité, etc.)
- **Sous-slide 8.2** : ⚠️ Inconvénients et Défis (Complexité initiale, Courbe d'apprentissage, etc.)
- **Sous-slide 8.3** : 🎯 Au-delà de la complexité métier - Structure, dépendances contrôlées, évolution
### 9. **Points Clés à Retenir** (Slide 9 + sous-slides)
- Résumé des concepts clés
- **Sous-slide 9.1** : Point clé 1
- **Sous-slide 9.2** : Point clé 2
- **Sous-slide 9.3** : Point clé 3

### 10. **Conclusion** (Slide 10)
Slide finale avec ressources et prochaines étapes

---

**Total : 10 slides principales avec de nombreuses sous-slides verticales**
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
│   │   ├── slide3-3.md   # └─ Schéma architecture
│   │   ├── slide4.md     # Les 3 couches
│   │   ├── slide4-1.md   # └─ Le Domaine (HTML)
│   │   ├── slide4-2.md   # └─ Les Ports (HTML)
│   │   ├── slide4-3.md   # └─ Les Adaptateurs
│   │   ├── slide4-4.md   # └─ Détails supplémentaires
│   │   ├── slide5.md     # Ports & Adaptateurs
│   │   ├── slide5-1.md   # └─ Distinction Port vs Adapter
│   │   ├── slide5-2.md   # └─ Exemple Domaine
│   │   ├── slide5-3.md   # └─ Le PORT
│   │   ├── slide5-4.md   # └─ L'Infrastructure
│   │   ├── slide5-5.md   # └─ Schéma SVG ProgramSearch
│   │   ├── slide5-6.md   # └─ Adaptateurs Primaires
│   │   ├── slide5-7.md   # └─ Adaptateurs Secondaires
│   │   ├── slide5-8.md   # └─ Les Ports détails
│   │   ├── slide5-9.md   # └─ Injection dépendances Vue
│   │   ├── slide6.md     # Cas d'usage
│   │   ├── slide6-1.md   # └─ Scénario 1
│   │   ├── slide6-2.md   # └─ Scénario 2
│   │   ├── slide6-3.md   # └─ Scénario 3
│   │   ├── slide6-4.md   # └─ Scénario 4
│   │   ├── slide6-5.md   # └─ Scénario 5
│   │   ├── slide7.md     # Structure de projet
│   │   ├── slide8.md     # Avantages & Inconvénients
│   │   ├── slide8-1.md   # └─ Avantages
│   │   ├── slide8-2.md   # └─ Inconvénients
│   │   ├── slide9.md     # Points clés
│   │   ├── slide9-1.md   # └─ Point clé 1
│   │   ├── slide9-2.md   # └─ Point clé 2
│   │   ├── slide9-3.md   # └─ Point clé 3
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
- **Markdown & HTML** : Format des slides (HTML pour les fragments avancés)
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
## 💡 Concepts Clés Abordés
1. **Isolation du domaine** - Le métier au centre, protégé (❌ ne doit jamais importer de l'infrastructure)
2. **Inversion de dépendances** - Les dépendances pointent vers le domaine
3. **Ports & Adaptateurs** - Contrats définis par le domaine
4. **Primary vs Secondary** - Distinction claire entre pilotage et infrastructure
5. **Le domain définit ses types** - L'infrastructure s'adapte aux types du domain (ex: `SearchProgramParameters`)
6. **Use Cases** - Service métier = Use Case = Application Service
7. **Bootstrap** - Initialisation et injection de dépendances au démarrage (dans `main.ts`)
8. **Testabilité** - Mock facile des ports pour les tests
9. **Flexibilité** - Changement d'infrastructure sans impact sur le métier
### ⚠️ Règle d'Or

**Le domaine ne doit JAMAIS importer quoi que ce soit de l'infrastructure.**

Les types comme `SearchProgramParameters` doivent être définis dans le domaine. Si l'API externe a une structure différente, c'est l'adapter secondaire qui fait la transformation entre les types du domaine et les types de l'API.

## 📄 Licence
Projet éducatif - Libre d'utilisation pour la formation
