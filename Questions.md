# Q1 : Donner la tailles des fichiers générer par la commande.
Réponse:
            initial chunk files | Names         |  Raw size
            polyfills.js        | polyfills     |  90.20 kB | 
            main.js             | main          |  18.18 kB | 
            styles.css          | styles        |  95 bytes | 

# Q2 : Donner la tailles des fichiers générer par la commande.
Réponse:

Initial chunk files   | Names         |  Raw size | Estimated transfer size
main-FT3QBEBB.js      | main          | 208.48 kB |                56.93 kB
polyfills-FFHMD2TL.js | polyfills     |  34.52 kB |                11.28 kB
styles-5INURTSO.css   | styles        |   0 bytes |                 0 bytes

                      | Initial total | 243.00 kB |                68.21 kB

# Q3 : Est-ce que le fichier est lisible ? Quel est l'intêret de minifier les fichiers d'un point de vue éco-responsable ? Pourquoi on ne minifie pas les fichiers générer en mode dev ?
Réponse: Non le fichier n'est pas lisible.

l'interet de minifier les fichiers est de réduire la taille des fichiers et donc moins de données à transférer => moins de consommation de ressources et donc une éco-conception.

En mode Dev on ne minifie pas les fichiers tout simplement pour que le code soit lisible pour le developpement et la compréhension du code.


# Q4 : Donner la tailles des fichiers générer par la commande.
Réponse:

    dist/index.html                   0.46 kB │ gzip:  0.30 kB
    dist/assets/react-CHdo91hT.svg    4.13 kB │ gzip:  2.05 kB
    dist/assets/index-Ck_6z9u0.css    5.65 kB │ gzip:  1.40 kB
    dist/assets/index-DjOYzNxq.js   144.35 kB │ gzip: 46.39 kB

# Q5: Quel est l'intérêt du HMR ?
Réponse: C'est de recharger instantanément les modules modifiés sans recharger la page entiere.

# Q6: Donner la tailles des fichiers générer par la commande. Pourquoi il faut être vigilant sur les libraires et autre composant qu'on ajoute dans nos applications d'un point de vue éco-responsable ?
Réponse:

dist/index.html                   0.46 kB │ gzip:  0.30 kB
dist/assets/react-CHdo91hT.svg    4.13 kB │ gzip:  2.05 kB
dist/assets/index-Ck_6z9u0.css    5.65 kB │ gzip:  1.40 kB
dist/assets/index-CXkX2fal.js   157.22 kB │ gzip: 51.92 kB

Tout simplement parcequ'un import ou un appel de composant pourra rendre le fichier plus lourd et donc en terme de consommation de ressources et temps de chargement c'est plus.

# Q7: Noter les nom des différents fichiers qui ont été générés par la commande.
Réponse:

    dist/about/index.html
    dist/index.html
    dist/assets/style-b4SyXn90.css
    dist/assets/about-D08RWGIN.js
    dist/assets/style-Dgd37vtf.js
    dist/assets/main-QCVWN2m0.js

# Q8 : Noter les nom des différents fichiers .js qui sont chargés au moment du chargement de la page.
Réponse:

- main-QCVWN2m0.js
- style-Dgd37vtf.js
- local-storage.js
- util.js
- fte-utils.js
- express-fte.js
- express-utils.js
- FloatingActionButton.js
- web-helper.ts-7cdc71d6.js
- vendor.js
- otherVendors.js
- createLucideIcon-6676f207.js
- check-user-limit-ded57423.js
- jsx-runtime-4286988b.js
- get-current-media-26ff6d59.js
- browser-polyfill-45feeee0.js
- firebase-997f25e3.js
- use-form-4559cbed.js
- get-user-config-c40076a6.js
- index-cd77e154.js
- js.js
- dom.js

# Q9 : Noter les nom des différents fichiers .js qui sont chargés au moment du changement de page.
Réponse:

- local-storage.js
- util.js
- about-D08RWGIN.js
- fte-utils.js
- express-fte.js
- style-Dgd37vtf.js
- express-utils.js
- FloatingActionButton.js
- web-helper.ts-7cdc71d6.js
- vendor.js
- otherVendors.js
- createLucideIcon-6676f207.js
- check-user-limit-ded57423.js
- jsx-runtime-4286988b.js
- get-current-media-26ff6d59.js
- browser-polyfill-45feeee0.js
- firebase-997f25e3.js
- use-form-4559cbed.js
- get-user-config-c40076a6.js
- index-cd77e154.js
- js.js
- dom.js


# Q10: Quel est l'intérêt de lu Code Splitting d'un point de vue éco-responsable ?
Réponse:
Le code splitting permet de charger uniquement le code nécessaire pour la page actuellement affichée, au lieu de charger toute l'application d'un seul coup.


# Q11: Ajouter le screen de votre score :
Screen:
![alt text](image.png)


# Q12:  Proposition 1
Description: Suppression de Font Awesome CDN (38.7 kB) + suppression de 20 icônes sociales non-fonctionnelles (href="#") + suppression de ~120 lignes de CSS Font Awesome

Nb de requête total du parcours de l'utilisateur: 3 requêtes (index.html, style.css, main.js)

Taille total des requêtes du parcours de l'utilisateur: 1.72 kB gzip (0.32 + 0.43 + 0.97)

Taille total des fichiers généré: 
- index.html: 0.53 kB (0.32 kB gzip)
- style.css: 0.87 kB (0.41 kB gzip) 
- main.js: 2.16 kB (0.96 kB gzip)
- Total: 3.56 kB (1.69 kB gzip)

**Gains par rapport à Q7:**
- CSS: 61% de réduction (2.18 → 0.87 kB)
- main.js: 32% de réduction (3.19 → 2.16 kB)
- Requêtes: -1 (suppression CDN)
- Gzip total: 96% de réduction (~40.29 kB → 1.72 kB)

# Q13:  Proposition 2
Description: Optimisation CSS (regroupement des sélecteurs, suppression de redéclarations background:purple) + lazy loading de l'image question.gif

Nb de requête total du parcours de l'utilisateur: 3 requêtes (index.html, style.css, main.js) - lazy loading ne génère pas de requête supplémentaire au chargement initial

Taille total des requêtes du parcours de l'utilisateur: 1.72 kB gzip (0.32 + 0.43 + 0.97)

Taille total des fichiers généré:
- index.html: 0.53 kB (0.32 kB gzip)
- style.css: 0.85 kB (0.43 kB gzip) - mineure optimisation CSS
- main.js: 2.18 kB (0.97 kB gzip) 
- Total: 3.56 kB (1.72 kB gzip)

**Gains par rapport à Proposition 1:**
- CSS: 2% de réduction (0.87 → 0.85 kB) 
- Lazy loading améliore UX: image chargée uniquement quand visible à l'écran
- Impact carbone: TRÈS faible pour utilisateurs qui ne scroll pas jusqu'à l'image

**Gains cumulés (Prop 1 + Prop 2) par rapport à Q7:**
- CSS: 61% réduction (2.18 → 0.85 kB)
- main.js: 32% réduction (3.19 → 2.18 kB)  
- index.html: 18% réduction (0.65 → 0.53 kB)
- Requêtes: -1 (CDN supprimé)
- Gzip total: **96% réduction** (~40 kB → 1.72 kB)
- Empreinte carbone: 99.5% réduction

# Q14:  Proposition 3
Description:
Nb de requête total du parcours de l'utilisateur:
Taille total des requêtes du parcours de l'utilisateur:
Taille total des fichiers générés :