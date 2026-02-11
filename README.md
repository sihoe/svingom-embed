# SvingOm – Embed av sykkelruter (kart + høydeprofil)

Dette repoet hoster en enkel embed-side via GitHub Pages som viser:
- kart med rute og POI-er
- nøkkelinformasjon (lengde, stigning/fall, høyeste/laveste punkt)
- høydeprofil (med underlagsfarger)
- SvingOm-logo som lenker til den aktuelle rutesiden på svingom.no

Embed-siden er laget for partnere uten teknisk kompetanse: de skal kun lime inn en ferdig iframe-kode.

---

## 1) URL-format (det eneste partneren trenger)

Partneren skal bruke denne URL-en (bytt ut route-id):

**Base:**
https://sihoe.github.io/svingom-embed/?route=ROUTE_ID

**Eksempel:**
https://sihoe.github.io/svingom-embed/?route=smadoldalen-rundt

> `route` må være identisk med `id` i `routes402.json`.

---

## 2) Iframe-kode (lim inn hos partner)

### Anbefalt (responsiv, fungerer i de fleste CMS)
Kopier og lim inn:

```html
<div style="position:relative;width:100%;padding-top:75%;overflow:hidden;border-radius:14px;">
  <iframe
    src="https://sihoe.github.io/svingom-embed/?route=smadoldalen-rundt"
    style="position:absolute;inset:0;width:100%;height:100%;border:0;"
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade"
    allowfullscreen>
  </iframe>
</div>

Hvis partner trenger fast høyde (enklere, men mindre fleksibelt)
<iframe
  src="https://sihoe.github.io/svingom-embed/?route=smadoldalen-rundt"
  style="width:100%;height:900px;border:0;border-radius:14px;overflow:hidden;"
  loading="lazy"
  allowfullscreen>
</iframe>



