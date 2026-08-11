# pasoapaso-doget

Material de clase — **Escencial Consultora · Área de Innovación y Desarrollo**.

Guía paso a paso + panel de administración que **lee** los comprobantes desde una
Google Sheet usando `doGet`, con la metodología del backend completo
(`doPost` + `doGet`) en un solo pegado, por si se arma todo junto.

## Contenido

- **`index.html`** — Guía paso a paso (arma el prompt en vivo). 6 pasos:
  contexto/marca → backend completo `doPost`+`doGet` → publicar y link →
  caché en `localStorage` → login → informe mensual + PDF.
- **`comprobantes-panel-admin.html`** — El panel funcionando: login, KPIs,
  gráficos (Chart.js), comparación mes a mes e informe mensual exportable a PDF
  (jsPDF + autotable). Cachea los datos en el navegador (`localStorage`).
- **`assets/doPost-doGet.txt`** — El backend completo listo para pegar en Apps Script.
- **`assets/`** — Logo, fondo y tipografías de marca. En `assets/capturas/` van las
  capturas de los pasos.

## Cómo usarlo

1. Abrí `index.html` y seguí los pasos marcándolos: el prompt se arma solo.
2. Pegá el backend de `assets/doPost-doGet.txt` en tu Google Sheet
   (**Extensiones → Apps Script**), cambiá el nombre de la hoja y publicalo como
   aplicación web (**Ejecutar como: Yo** · **Quién tiene acceso: Cualquier usuario**).
3. En `comprobantes-panel-admin.html`, editá el bloque `CONFIG` de arriba:
   usuario, contraseña, nombre de la hoja y la URL del Web App (`.../exec`).
4. Abrí el panel con doble clic, iniciá sesión y verificá que aparecen tus comprobantes.

> El login es una puerta simple del lado del navegador (frena accesos casuales, no
> reemplaza seguridad real). Para datos muy sensibles, usá un backend con
> autenticación real.

## Nota

Este repo es **independiente** del proyecto de carga original (doPost). No comparte
archivos ni links con él: se puede usar por separado.
