# asap-legal

Política de Privacidad y Términos de Servicio de Asap, servidos como sitio
estático vía GitHub Pages.

- `index.html` — landing con enlaces a ambos documentos.
- `privacy-policy.html` / `terms-of-service.html` — las páginas públicas.
- `PRIVACY_POLICY.md` / `TERMS_OF_SERVICE.md` — fuente editable en Markdown;
  si se edita el contenido, actualizar también el `.html` correspondiente
  (no se regeneran automáticamente).

## Publicar cambios

1. Editar el `.md` correspondiente en el repo principal de Asap
   (`legal/`) y/o directamente el `.html` acá.
2. `git add . && git commit -m "..." && git push`
3. GitHub Pages redeploya solo en cada push a la rama configurada — no
   hace falta ningún paso manual adicional.

## URLs (una vez publicado)

- Política de Privacidad: `https://<usuario>.github.io/asap-legal/privacy-policy.html`
- Términos de Servicio: `https://<usuario>.github.io/asap-legal/terms-of-service.html`

Estas son las URLs que van en Play Console (Data Safety) y en la pantalla
de consentimiento de OAuth de Google Cloud Console.
