## 🛠 Tech Rules
* **Code :** Zéro commentaire à l'interieur du code. Nommage sémantique uniquement.
* **Responsivité :** Mobile-first, sauf si app pour PC. Sidebar fixe (70px) masquée sur mobile (`max-width: 768px`).
* **UX :** Interdiction de scroll (`overflow: hidden !important` sur `body`) quand une modale ou le menu mobile est ouvert.
* **Animations :** Transitions douces (0.2s - 0.45s). Burger → Croix via `translateY` et `rotate`.

## 🎨 Palette & Style (Dark-first Néo-glassmorphism)
| Élément | Dark (Base) | Light (Miroir) |
| :--- | :--- | :--- |
| **Fond Page** | `#0e0e0e` | `#f8f8f8` |
| **Texte Principal** | `#f1f1f1` | `#181a20` |
| **Texte Secondaire**| `#999`, `#888`, `#666` | `#555`, `#333` |
| **Accent (Spotify)**| `#1db954` | `#4caf50` |
| **Danger** | `#ff4d4f` | idem |

* **Gradients Overlay :**
    * *Dark :* `linear-gradient(135deg, #0e0e0e 0%, #1a1a1a 100%)`.
    * *Light :* `linear-gradient(135deg, #ffffff 0%, #f5f5f5 100%)`.
* **Effets :** `backdrop-filter: blur(10px)`. Bordures fines semi-transparentes.
* **Radii :** 8px, 10px, 16px, 20px, 24px (cards), 999px (pills).

## 🧱 Composants & Navigation
* **Cards (.ac-card, .service-card) :**
    * *Dark :* Gradient 180° `rgba(255,255,255,0.04)` vers `0.02`. Bordure `rgba(255,255,255,0.07)`.
    * *Light :* Gradient 180° `rgba(0,0,0,0.02)` vers `0.05`. Bordure `rgba(0,0,0,0.08)`. Ombre portée légère.
* **Mobile Menu (Standardisé) :**
    * **Overlay :** Plein écran, opacité transition (0.4s).
    * **Items :** Style "Glass card" (fond alpha + blur), radius 16px. `translateX(10px)` au hover.
    * **Z-index :** Burger (1002), Contenu (1001), Overlay (1000).
* **Gradients Titres (H1) :**
    * *Dark :* `linear-gradient(90deg, #fff, #bbb)`.
    * *Light :* `linear-gradient(90deg, #111, #444)`.