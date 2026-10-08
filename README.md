# Helvetica Vitrine — page publique pour l'écran boutique
Page animée (taux en direct, or, messages) servie par GitHub Pages.
Contenu 100 % public : taux déjà publiés sur helveticaexchange.ch. Aucun secret ici.

## Versions
| Dossier | Rôle | URL lecteur LED (576×576) |
|---|---|---|
| `v4/` | **Production dès validation** — « Horlogerie » (08.10.2026) | `https://helveticaexchange-commits.github.io/helvetica-vitrine/v4/?px=576` |
| `v3/` | Ancienne production « Laboratoire » (22.08.2026), conservée pour retour arrière | `…/v3/?px=576` |
| `v2/` | Variante « Panneau » (21.08.2026) | `…/v2/?px=576` |
| `index.html` | v1 « LED Edition » (20.08.2026) | `…/?px=576` |

## v4 — ce qui change
- **Données 100 % VPS** (`api.daric.app`) : devises, or, argent, historique intraday, références de la veille,
  mémoire d'or 7 jours. Plus aucune valeur de secours codée en dur (fin du « 117.40 »).
- **États visibles** : point or qui bat = live · anneau creux + « DERNIERS TAUX · hh:mm » = données retenues
  (> 20 min) · « COURS AU COMPTOIR » = rien de fiable (> 36 h ou jamais reçu, pages or retirées de la boucle).
- **Séquence** : Taux → 2 scènes → Taux → 2 scènes → Taux → Poinçon (la page des taux revient toutes les 2 scènes).
- **Entête** : l'heure et la date sont mesurées et ne débordent jamais du cadre (3 paliers de repli).
- **Page Taux** : odomètre (les chiffres roulent dans le sens du mouvement), flèches vs la grille affichée
  hier 19 h (photo locale, repli VPS), badge « pour 100 / per 100 », entêtes FR/EN. Sous chaque devise : le filet
  droit seulement (la courbe de fond suffit).
- **Polices embarquées** (Playfair Display, même origine) → même rendu sur le lecteur que sur le Mac.
- **Mouvement** : Motion (moteur vanilla de Framer Motion) auto-hébergé dans `v4/vendor/`, repli CSS automatique.
- **Hygiène** : `version.json` vérifié toutes les 30 min (rechargement automatique après un déploiement),
  rechargement quotidien 05h10, chien de garde 6 h sans VPS.

## Paramètres d'URL (v4)
`?px=576` mode LED (obligatoire sur le lecteur) · `?fx=hi` tous les effets · `?motion=0` sans Motion ·
`?seq=classic` ancienne séquence · `?diag=1` grille de calibration.

## Retour arrière
Remettre l'URL du lecteur sur `…/v3/?px=576` (la v3 n'a pas été modifiée), ou `git checkout` du commit « v3.10 ».
