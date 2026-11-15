# asap-legal

Sitio público de Asap, servido como sitio estático vía GitHub Pages.

- `index.html` — homepage de la app: qué es Asap, cómo funciona, para qué usa
  los datos de Gmail y botones a ambos documentos legales. Esta es la URL que
  va en el campo *Application home page* de la pantalla de consentimiento de
  OAuth en Google Cloud Console (la verificación de Google rechaza una página
  que sea solo un login o solo un índice de documentos).
- `privacy-policy.html` / `terms-of-service.html` — las páginas públicas.
- `PRIVACY_POLICY.md` / `TERMS_OF_SERVICE.md` — fuente editable en Markdown;
  si se edita el contenido, actualizar también el `.html` correspondiente
  (no se regeneran automáticamente).
- `asap-logo.svg` — logo de la app (copia de `src/assets/svgs/ASAPLogo.svg`
  del repo principal, con el `fill` en blanco para el header).

## Publicar cambios

1. Editar el `.md` correspondiente en el repo principal de Asap
   (`legal/`) y/o directamente el `.html` acá.
2. `git add . && git commit -m "..." && git push`
3. GitHub Pages redeploya solo en cada push a la rama configurada — no
   hace falta ningún paso manual adicional.

## URLs públicas

Siempre con `https://` — GitHub Pages redirige `http://` con un 301, pero los
formularios de Google y Play Console deben llevar la URL `https` directa.

- Homepage de la app: `https://omarbonillav3.github.io/asap-legal/`
- Política de Privacidad: `https://omarbonillav3.github.io/asap-legal/privacy-policy.html`
- Términos de Servicio: `https://omarbonillav3.github.io/asap-legal/terms-of-service.html`

Estas son las URLs que van en Play Console (Data Safety) y en la pantalla
de consentimiento de OAuth de Google Cloud Console.
