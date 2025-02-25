Om JavaScript-functies te activeren die je geschreven hebt, kun je **events** gebruiken.

Events (gebeurtenissen) kunnen worden geactiveerd door de gebruiker of de browser.

- Gebruikers events:
  - Met de muis (klik, dubbele klik, muis eroverheen bewegen)
  - Met het toetsenbord (toetsaanslag, toetsomlaag, toetsomhoog)
  - Door aanrakingen (touchstart, touchmove, touchend)

- Browser events:
  - Het laden van de pagina (load, unload)
  - Venster gebeurtenissen (formaat wijzigen, scrollen)
  - Tijdgebeurtenissen (setInterval, setTimeout)

De eenvoudigste manier om dit te doen is door een knop te maken en er een `onclick`-attribuut aan toe te voegen.

In het project **Stripfiguur** gebruikte je een knop om een functie te activeren die een samenvatting van het personage van de gebruiker weergaf.

Voeg een `<button>`-element toe met de gebeurtenis `onclick="displaySummary()"`.

Voeg de tekst 'Maken' toe aan `<button>`, zodat de gebruiker weet wat de knop doet.

## --- code ---

language: html
filename:
line_numbers: false
--------------------------------------------------------

<button onclick="displaySummary()">Maken</button>

\--- /code ---

**Tip:** Wijzig de functie naar de functie die je wilt gebruiken wanneer de gebruiker op jouw knop klikt. Werk ook de tekst bij, zodat de gebruiker weet wat de knop doet.

**Andere events gebruiken**

In **Stripfiguurr** heb je ook de gebeurtenis `DOMContentLoaded` gebruikt om code te activeren wanneer de pagina wordt geladen.

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

- element: Het HTML-element waaraan je de event listener wilt koppelen
- eventType: Het type event waar je naar wilt luisteren (bijv. "click", "keydown", "DOMContentLoaded")
- callbackFunction: De functie die moet worden uitgevoerd wanneer de gebeurtenis plaatsvindt

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
