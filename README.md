# VidéoWeb by Claude

Une skill pour **Claude Code** qui permet de créer des scènes vidéo 3D interactives de A à Z, guidé par un assistant intelligent.

Pas besoin de connaître Three.js, WebGL ou Python — il suffit de décrire ce que vous voulez.

---

## Ce que fait cette skill

En tapant `/video3d` suivi d'une description, Claude vous guide à travers un processus en 7 étapes :

1. **Styles visuels** — Claude propose 4 styles adaptés à votre description (ex: Cyberpunk, Low-poly, Photoréaliste, Rétro 80s)
2. **Qualité de rendu** — Choix de la résolution (720p → 4K)
3. **Interview guidée** — Questions une par une sur l'ambiance, les objets, la caméra, les lumières, les animations, la vidéo, le son et les interactions
4. **Brief évolutif** — Un récapitulatif visuel se met à jour en direct après chaque réponse
5. **Génération** — Claude choisit la stack technique adaptée et génère tous les fichiers nécessaires
6. **Modifications** — Affinez la scène en langage naturel ("caméra plus haute", "lumière plus froide"…)
7. **Export** — Code nettoyé + README livré avec `/export`

---

## Installation

### Prérequis

- [Claude Code](https://claude.ai/code) installé sur votre machine

### Étapes

1. Télécharger le fichier `video3d.md`

2. Le placer dans le dossier des commandes globales de Claude Code :

   **Windows**
   ```
   C:\Users\<votre-nom>\.claude\commands\video3d.md
   ```

   **macOS / Linux**
   ```
   ~/.claude/commands/video3d.md
   ```
   > Si le dossier `commands` n'existe pas, créez-le.

3. Redémarrer Claude Code.

---

## Utilisation

Dans n'importe quelle conversation Claude Code, tapez :

```
/video3d un salon cosy avec une télé qui joue de la sci-fi
```

Ou sans description pour être guidé dès le départ :

```
/video3d
```

### Commandes disponibles pendant la session

| Commande | Action |
|---|---|
| `/video3d <description>` | Démarrer une nouvelle scène |
| `go` | Valider le brief et lancer la génération |
| `/export` | Exporter le code final nettoyé |

---

## Exemple de workflow

```
/video3d une forêt la nuit avec des lucioles et de la brume

→ Claude propose 4 styles (Réaliste sombre / Cel-shading / Pixel art / Aquarelle animée)
→ Vous choisissez le style
→ Claude demande la qualité (720p → 4K)
→ Interview guidée : ambiance, objets, caméra, lumières...
→ Brief mis à jour en direct après chaque réponse
→ Vous tapez "go"
→ Claude génère les fichiers (Three.js + shaders de brume + système de particules)
→ Vous demandez "ajoute des sons d'animaux"
→ Claude met à jour uniquement la partie audio
→ Vous tapez /export → code propre + README
```

---

## Technologies générées (selon le projet)

- **Three.js** — scènes 3D interactives
- **p5.js** — rendu génératif et visualisation audio
- **WebGL / GLSL** — shaders personnalisés
- **React Three Fiber** — scènes 3D dans une app React
- **Python** (OpenCV, MoviePy) — traitement et export vidéo

---

Créé avec [Claude Code](https://claude.ai/code)
