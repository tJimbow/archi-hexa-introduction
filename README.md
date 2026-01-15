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
### 1. **Introduction** (slide1.md)
Architecture Hexagonale - Introduction et Concepts Fondamentaux
### 2. **Le Problème** (slide2.md)
🤔 Le Problème - Architecture Traditionnelle en Couches
### 3. **Qu'est-ce que l'Architecture Hexagonale ?** (slide3.md et sous-slides)
- 🎯 Qu'est-ce que l'Architecture Hexagonale ?
- Principe Fondamental
- Pourquoi "Hexagonale" ?
- 📚 Schéma de l'Architecture Hexagonale
### 4. **Les 3 Couches Principales** (slide4.md et sous-slides)
- 🏗️ Les 3 Couches Principales
- 1️⃣ Le Domaine (Domain)
- 2️⃣ Les Ports
- 3️⃣ Les Adaptateurs (Adapters)
- Exemples d'Adaptateurs Primaires
### 5. **Ports & Adaptateurs : Détails** (slide5.md et sous-slides)
- 🔌 Domain & Infrastructure : Détails - Exemple complet
- Le Domaine => Les entités
- Le Domaine => Les ports
- Le Domaine => Les services/use cases
- Le Domaine => Résumé
- Infrastructure => Adaptateurs secondaires
- L'Infrastructure => Adaptateurs primaires
- L'Infrastructure => Résumé
- Application (Bootstrap)
- Schéma récapitulatif
### 6. **Domain & Infrastructure : Détails** (slide6.md et sous-slides)
- 🔌 Domain & Infrastructure : Détails - Exemple simplifié
- Le PORT (interfaces de ports)
- Adaptateur PRIMAIRE : Utilise le Port
- Adaptateur SECONDAIRE : Implémente le Port
- 🎯 Schéma récapitulatif
### 7. **Structure de Projet** (slide7.md)
📦 Structure de Projet
### 8. **Exemples et Organisation** (slide8.md et sous-slides)
- ⚡ Exemple Back - Type de mise en œuvre : Fonction Azure
- Les grandes lignes
- Les quatre projets de base
- Le projet Domain
- Un exemple d'un port driven
- Sidebar : Verbage (Inbound)
- Sidebar : Verbage (Outbound)
- Un exemple d'un port driving
- Le projet Infrastructure
- Un exemple d'une implémentation d'un port driven
- Un exemple d'une implémentation d'un port driving
- Le projet Functions
- Un exemple d'une fonction AZF
- Le projet Application
- Un exemple d'une requête
### 9. **Avantages & Inconvénients** (slide9.md et sous-slides)
- ⚖️ Avantages & Inconvénients
- ✅ Avantages
- ⚠️ Inconvénients et Défis
- 🎯 Au-delà de la complexité métier
### 10. **Points Clés à Retenir** (slide10.md)
🎓 Points Clés à Retenir

---

**Total : 10 slides principales avec de nombreuses sous-slides verticales**
## 📁 Structure du projet
```
archi-hexa-introduction/
├── src/
│   ├── counter.ts
│   ├── detail/
│   ├── main.ts
│   ├── slides/
│   │   ├── slide1.md   : Architecture Hexagonale - Introduction et Concepts Fondamentaux
│   │   ├── slide2.md   : 🤔 Le Problème - Architecture Traditionnelle en Couches
│   │   ├── slide3.md   : 🎯 Qu'est-ce que l'Architecture Hexagonale ?
│   │   ├── slide3-1.md : Principe Fondamental
│   │   ├── slide3-2.md : Pourquoi "Hexagonale" ?
│   │   ├── slide3-3.md : 📚 Schéma de l'Architecture Hexagonale
│   │   ├── slide4.md   : 🏗️ Les 3 Couches Principales
│   │   ├── slide4-1.md : 1️⃣ Le Domaine (Domain)
│   │   ├── slide4-2.md : 2️⃣ Les Ports
│   │   ├── slide4-3.md : 3️⃣ Les Adaptateurs (Adapters)
│   │   ├── slide4-4.md : Exemples d'Adaptateurs Primaires
│   │   ├── slide5.md   : 🔌 Domain & Infrastructure : Détails - Exemple complet
│   │   ├── slide5-1.md : Le Domaine => Les entités
│   │   ├── slide5-2.md : Le Domaine => Les ports
│   │   ├── slide5-3.md : Le Domaine => Les services/use cases
│   │   ├── slide5-4.md : Le Domaine => Résumé
│   │   ├── slide5-5.md : Infrastructure => Adaptateurs secondaires
│   │   ├── slide5-6.md : L'Infrastructure => Adaptateurs primaires
│   │   ├── slide5-7.md : L'Infrastructure => Résumé
│   │   ├── slide5-8.md : Application (Bootstrap)
│   │   ├── slide5-9.md : Schéma récapitulatif
│   │   ├── slide6.md   : 🔌 Domain & Infrastructure : Détails - Exemple simplifié
│   │   ├── slide6-1.md : Le PORT (interfaces de ports)
│   │   ├── slide6-2.md : Adaptateur PRIMAIRE : Utilise le Port
│   │   ├── slide6-3.md : Adaptateur SECONDAIRE : Implémente le Port
│   │   ├── slide6-4.md : 🎯 Schéma récapitulatif
│   │   ├── slide7.md   : 📦 Structure de Projet
│   │   ├── slide8.md   : ⚡ Exemple Back - Type de mise en œuvre : Fonction Azure
│   │   ├── slide8-1.md : Les grandes lignes
│   │   ├── slide8-2.md : Les quatre projets de base
│   │   ├── slide8-3.md : Le projet Domain
│   │   ├── slide8-4.md : Un exmple d'un port driven
│   │   ├── slide8-5.md : Sidebar : verbage (inbound)
│   │   ├── slide8-6.md : Sidebar : verbage (outbound)
│   │   ├── slide8-7.md : Un exemple d'un port driving
│   │   ├── slide8-8.md : Le projet infrastructure
│   │   ├── slide8-9.md : Un exemple d'une implémentation d'un port driven
│   │   ├── slide8-10.md: Un exemple d'une implémentation d'un port driving
│   │   ├── slide8-11.md: Le projet Functions
│   │   ├── slide8-12.md: Un exemple d'une fonction AZF
│   │   ├── slide8-13.md: Le projet application
│   │   ├── slide8-14.md: Un exemple d'une requête
│   │   ├── slide9.md   : ⚖️ Avantages & Inconvénients
│   │   ├── slide9-1.md : ✅ Avantages
│   │   ├── slide9-2.md : ⚠️ Inconvénients et Défis
│   │   ├── slide9-3.md : 🎯 Au-delà de la complexité métier
│   │   ├── slide10.md  : 🎓 Points Clés à Retenir
│   │   └── ...
│   ├── style.css
│   ├── typescript.svg
├── index.html
├── package.json
├── package-lock.json
├── tsconfig.json
├── README.md
├── public/
│   ├── vite.svg
│   └── images/
│       ├── hexagonal-complet-example.svg
│       ├── hexagonal-generic.svg
│       └── hexagonal-simple-example.svg
└── ...
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
