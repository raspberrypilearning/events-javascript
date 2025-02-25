You might want to use **events** to trigger any JavaScript functions you have written.

Les événements peuvent être déclenchés par l'utilisateur ou le navigateur.

- Évènements utilisateur :
  - Mouse events (click, double click, mouseover)
  - Keyboard events (keypress, keydown, keyup)
  - Touch events (touchstart, touchmove, touchend)

- Événements du navigateur :
  - Page load events (load, unload)
  - Window events (resize, scroll)
  - Time events (setInterval, setTimeout)

La façon la plus simple de le faire est de créer un bouton et d'y ajouter un attribut `onclick`.

In the **Comic character** project, you used a button to trigger a function that displayed a summary of the user's character.

Add a `<button>` element with the event `onclick="displaySummary()"`.

Ajoute le texte 'Créer' au `<button>`, afin que l'utilisateur sache ce que fait le bouton.

## --- code ---

language: html
filename:
line_numbers: false
--------------------------------------------------------

<button onclick="displaySummary()">Créer</button>

\--- /code ---

**Tip:** Change the function to whatever function you want to use when the user clicks your button. Also, update the text so the user knows what the button will do.

**Utiliser d'autres événements**

In **Comic character**, you also used the `DOMContentLoaded` event to trigger code when the page loads.

Utilise `.addEventListener` comme ceci :

## --- code ---

language: js
filename:
line_numbers: false
line_number_start:
line_highlights:
-----------------------------------------------------

element.addEventListener(eventType, callbackFunction);

\--- /code ---

- element: The HTML element to which you want to attach the event listener
- eventType: The type of event you want to listen for (e.g. "click", "keydown", "DOMContentLoaded")
- callbackFunction: The function to be executed when the event happens

## --- code ---

language: js
filename: scripts.js
line_numbers: true
line_number_start: 65
line_highlights: 69
--------------------------------------------------------

// Vérifier le stockage local
document.addEventListener("DOMContentLoaded", function () {

if (localStorage.getItem("lightMode") == "true") {
document.body.classList.toggle("light-mode");
}

});

\--- /code ---
