---
$title: Modifica di presentazione e layout
---

## Modifica della presentazione

Le pagine AMP sono pagine web; l’applicazione di stili alla pagina e ai suoi elementi viene effettuata tramite proprietà CSS comuni. Definisci gli stili degli elementi tramite selettori di classi o elementi in un foglio di stile incorporato nel tag `<head>`, denominato `<style amp-custom>`:

[sourcecode:html]
<style amp-custom>
  /* any custom style goes here */
  body {
    background-color: white;
  }
  amp-img {
    background-color: gray;
    border: 1px solid black;
  }
</style>
[/sourcecode]

Ciascuna pagina AMP può avere solamente un foglio di stile incorporato e l’uso di alcuni selettori non è consentito. [Scopri tutte le informazioni utili sullo stile](/it/docs/design/responsive/style_pages.html).

## Controllo del layout

AMP segue regole più severe per il layout degli elementi nella pagina. In una normale pagina HTML, per il layout degli elementi utilizzi quasi esclusivamente CSS. Tuttavia, per questioni legate alle prestazioni, AMP impone in partenza un limite esplicito per tutti gli elementi.

Scopri in che modo viene eseguito il rendering e il layout di una pagina in AMP e come fare per modificare il layout nella sezione [Come controllare il layout](/it/docs/design/responsive/control_layout.html).

<div class="prev-next-buttons">
  <a class="button prev-button" href="/it/docs/getting_started/create/include_image.html"><span class="arrow-prev">Precedente</span></a>
  <a class="button next-button" href="/it/docs/getting_started/create/preview_and_validate.html"><span class="arrow-next">Prossimo</span></a>
</div>
