Afin de déclencher toutes les fonctions JavaScript que tu as écrites, tu pourrais utiliser **events**.

Les événements peuvent être déclenchés par l'utilisateur ou le navigateur.

- Évènements utilisateur :
  - Événements de la souris (clic, double clic, souris)
  - Événements du clavier (appui sur une touche, enfoncement d'une touche, relâchement d'une touche)
  - Événements tactiles (touchstart, touchmove, touchend)

- Événements du navigateur :
  - Événements de chargement de page (chargement, déchargement)
  - Evénements de la fenêtre (redimensionnement, défilement)
  - Événements temporels (setInterval, setTimeout)

La façon la plus simple de le faire est de créer un bouton et d'y ajouter un attribut `onclick`.

Dans le projet **Personnage de Comics**, tu as utilisé un bouton pour déclencher une fonction qui affichait un résumé du personnage de l'utilisateur.

Ajoute un élément `<button>` avec l'événement `onclick="displaySummary()"`.

Ajoute le texte 'Créer' au `<button>`, afin que l'utilisateur sache ce que fait le bouton.

--- code ---
---
language: html
filename:
line_numbers: false
---

<button onclick="displaySummary()">Créer</button>

--- /code ---

**Astuce :** change la fonction pour n'importe quelle fonction que tu veux utiliser lorsque l'utilisateur clique sur ton bouton. Mets aussi à jour le texte pour que l'utilisateur sache ce que le bouton fera.

**Utiliser d'autres événements**

Dans **Personnage de Comics** tu as également utilisé l'événement `DOMContentLoaded` pour déclencher du code lors du chargement de la page.

Utilise `.addEventListener` comme ceci :

--- code ---
---
language: js
filename: 
line_numbers: false
line_number_start: 
line_highlights: 
---
   
element.addEventListener(eventType, callbackFunction);

--- /code ---

- element : l'élément HTML auquel tu veux attacher l'event listener
- eventType : le type d'événement que tu veux recevoir l'entrée (par exemple "click", "keydown", "DOMContentLoaded")
- callbackFunction : la fonction à exécuter lorsque l'événement se produit

--- code ---
---
language: js
filename: scripts.js
line_numbers: true
line_number_start: 65
line_highlights: 69
---

// Vérifier le stockage local
document.addEventListener("DOMContentLoaded", function () {    
  
  if (localStorage.getItem("lightMode") == "true") {
    document.body.classList.toggle("light-mode");
  }

});
  
--- /code ---
