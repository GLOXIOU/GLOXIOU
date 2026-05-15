## 🛠 Tech Rules
* **Code :** Zéro commentaire à l'intérieur du code. Nommage sémantique uniquement.
* **Responsivité :** Mobile-first. Conteneurs centrés (`max-width: 1100px` ou `1400px` pour l'admin).
* **UX :** Interdiction de scroll quand une modale est ouverte. Transitions fluides via `cubic-bezier(0.16, 1, 0.3, 1)`.
* **Structure :** Utilisation systématique de sections `.card` dans une grille `.cards-grid`.

## 🎨 Palette & Style (Soft-Glassmorphism & Blue Accent)
| Élément | Valeur |
| :--- | :--- |
| **Fond Page** | `#f7f9fc` |
| **Texte Principal** | `#2d3748` |
| **Texte Secondaire**| `#718096` |
| **Accent Primary** | `#3182ce` |
| **Accent Hover** | `#2b6cb0` |
| **Bordures Glass** | `rgba(255, 255, 255, 0.4)` |

* **Effet Glassmorphism :**
    * `background: rgba(255, 255, 255, 0.25)`
    * `backdrop-filter: blur(25px) saturate(200%)`
    * `border: 1px solid rgba(255, 255, 255, 0.4)`
    * `box-shadow: inset 0 0 20px rgba(255, 255, 255, 0.5), 0 15px 50px rgba(0, 0, 0, 0.05)`
* **Radius :** `30px` pour les cartes, `16px` pour les inputs, `12px` pour les petits boutons.

## ✨ Background System (5-Layers)
Pour reproduire le fond, l'ordre des couches (z-index) est crucial :
1. **Spheres (Layer 1) :** Cercles flous (`blur(80px)`) avec gradients animés (`float-1` / `float-2`).
2. **Glow (Layer 2) :** `radial-gradient` central avec animation `pulse` (scale 0.9 à 1.1).
3. **Grid (Layer 3) :** `linear-gradient` créant un motif de 40px x 40px (`rgba(0, 0, 0, 0.03)`).
4. **Noise (Layer 4) :** Texture SVG `fractalNoise` à `0.04` d'opacité.
5. **Content (Layer 10) :** Conteneur principal.

## 📦 Composants
* **Titres (h1) :** Gradient texte `linear-gradient(135deg, #1e3a8a, #4299e1)` avec `-webkit-background-clip: text`.
* **Boutons Primary :** `background: linear-gradient(135deg, #3182ce, #2b6cb0)`. Shadow au survol.
* **Inputs :** `background: rgba(255, 255, 255, 0.6)`. Focus avec `box-shadow: 0 0 0 4px rgba(49, 130, 206, 0.1)`.
* **Modales :** Overlay `blur(15px)` et fond sombre léger `rgba(0, 0, 0, 0.2)`.

## 🎬 Animations & Courbes
* **Entrée :** `fadeUp` (40px vers 0) sur 1s avec `cubic-bezier(0.16, 1, 0.3, 1)`.
* **Hover :** Transition de `box-shadow` et `border-color` sur `0.5s`.
* **Scale :** Légère augmentation de taille (`1.02`) sur les boutons au survol.