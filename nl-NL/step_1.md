You might want to use **events** to trigger any JavaScript functions you have written.

Events (gebeurtenissen) kunnen worden geactiveerd door de gebruiker of de browser.

- Gebruikers events:
  - Mouse events (click, double click, mouseover)
  - Keyboard events (keypress, keydown, keyup)
  - Touch events (touchstart, touchmove, touchend)

- Browser events:
  - Page load events (load, unload)
  - Window events (resize, scroll)
  - Time events (setInterval, setTimeout)

De eenvoudigste manier om dit te doen is door een knop te maken en er een `onclick`-attribuut aan toe te voegen.

In the **Comic character** project, you used a button to trigger a function that displayed a summary of the user's character.

Add a `<button>` element with the event `onclick="displaySummary()"`.

Voeg de tekst 'Maken' toe aan `<button>`, zodat de gebruiker weet wat de knop doet.

## --- code ---

language: html
filename:
line_numbers: false
--------------------------------------------------------

<button onclick="displaySummary()">Maken</button>

\--- /code ---

**Tip:** Change the function to whatever function you want to use when the user clicks your button. Also, update the text so the user knows what the button will do.

**Andere events gebruiken**

In **Comic character**, you also used the `DOMContentLoaded` event to trigger code when the page loads.

Gebruik `.addEventListener` zoals hier:

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

// Controleer lokale opslag
document.addEventListener("DOMContentLoaded", function () {

if (localStorage.getItem("lightMode") == "true") {
document.body.classList.toggle("light-mode");
}

});

\--- /code ---
