<!--
  BORRADOR generado a partir del análisis real del código de Asap
  (arquitectura de datos, CLAUDE.md, NOTES.md, src/db, src/services).
  Antes de publicar: revisar con un abogado, sobre todo las secciones de
  responsabilidad y cumplimiento normativo de protección de datos según
  las jurisdicciones donde Asap tenga usuarios.
  Última revisión de contenido: 2026-08-07.
-->

# Política de Privacidad de Asap

**Fecha de entrada en vigencia:** 7 de agosto de 2026
**Última actualización:** 7 de agosto de 2026

## 1. Quiénes somos

Asap es una aplicación móvil que ayuda a sus usuarios a visualizar sus
gastos personales de forma rápida y consciente. Esta Política de
Privacidad explica qué datos accede Asap, cómo los procesa, dónde se
guardan y qué control tenés sobre ellos.

**Contacto:** omarbonilla.v3@gmail.com

## 2. Qué es Asap (y qué NO es)

Asap lee las notificaciones que los bancos envían por correo electrónico
(compras, cargos, movimientos) y las presenta de forma visual dentro de
la app, para que puedas ver en qué se te va el dinero.

**Asap no es una aplicación bancaria.** No mueve dinero, no realiza
transferencias ni ninguna operación transaccional. Es puramente una
herramienta de visualización y consciencia financiera.

## 3. Qué datos accedemos y por qué

Para funcionar, Asap solicita tu autorización para acceder a tu cuenta de
Gmail mediante el inicio de sesión de Google (OAuth), con el permiso de
**solo lectura** `gmail.readonly`. Esto significa que Asap:

- **Puede:** leer el contenido de tus correos para encontrar
  notificaciones bancarias.
- **No puede:** enviar correos en tu nombre, eliminar correos, ni
  modificar nada dentro de tu cuenta de Gmail.

Este permiso lo otorgás vos explícitamente en la pantalla de consentimiento
de Google, y podés revocarlo en cualquier momento (ver sección 9).

Adicionalmente, al iniciar sesión, la app lee tu nombre, tu correo y tu
foto de perfil de Google para mostrarlos en tu perfil dentro de la app —
esta información se muestra en vivo desde tu sesión de Google, Asap no
guarda una copia separada de tu nombre o tu foto.

## 4. Cómo procesamos los correos

De los correos que coinciden con los remitentes conocidos de bancos
soportados, Asap extrae únicamente los datos necesarios para reconstruir
una transacción: comercio, monto, moneda, fecha, banco, y los últimos 4
dígitos de la tarjeta involucrada (nunca el número completo). El resto de
tu bandeja de entrada nunca es leído ni descargado — el filtro de qué
correos traer se hace por remitente antes de bajar cualquier contenido.

Los correos que no logran procesarse (por ejemplo, un formato nuevo de un
banco) quedan guardados igual, para que puedan re-procesarse en el futuro
sin necesidad de volver a acceder a tu cuenta de Gmail.

## 5. Dónde se guardan tus datos

**Todo el procesamiento y almacenamiento ocurre en tu propio dispositivo.**
Asap guarda los correos bancarios procesados y las transacciones derivadas
en una base de datos local (SQLite) dentro de tu teléfono — no en un
servidor de Asap. Hoy, Asap **no tiene servidor propio** que reciba tus
correos, tus transacciones o tus montos.

Esto también significa que:

- Si desinstalás la app, todos tus datos financieros procesados (correos,
  transacciones, presupuestos, tarjetas, ingresos manuales) se eliminan
  junto con la app.
- Asap no puede ver, ni nosotros como equipo detrás de Asap, el contenido
  de tus correos o tus montos — no existe un panel ni una base de datos
  central donde consultarlos.

## 6. Qué NO recopilamos

Asap no usa redes publicitarias, no vende datos a terceros, y hoy no
utiliza herramientas de analítica de producto ni de rastreo de terceros.

## 7. Notificaciones

Las notificaciones de Asap (por ejemplo, avisos de que te estás acercando
al límite de una tarjeta o a un presupuesto) se generan y se muestran
localmente en tu dispositivo. No pasan por un servidor push de terceros —
se calculan con los datos que ya están guardados localmente y se
entregan directamente en tu teléfono.

## 8. Función futura: recuperar tus bancos conectados en un celular nuevo

**Esta función todavía no está disponible — se detalla acá para que sepas
qué va a cambiar cuando se active, no porque esté funcionando hoy.**

Hoy, la lista de bancos y correos que conectaste vive únicamente en la
base de datos local de tu dispositivo — si cambiás de celular, tenés que
volver a conectarlos manualmente. Estamos preparando una función para que,
al iniciar sesión en un dispositivo nuevo, puedas recuperar automáticamente
qué bancos tenías conectados anteriormente.

Cuando esta función se active, Asap va a guardar en un servidor de
respaldo (no en tu dispositivo) **únicamente**:

- Tu cuenta de Google (correo, para identificarte).
- La lista de qué bancos conectaste y con qué correo recibís sus
  notificaciones.

Esa copia de respaldo **nunca va a incluir** el contenido de tus correos,
tus transacciones, montos, ni ningún dato financiero — esos siguen
guardándose solo en tu dispositivo, igual que hoy. Esta política se va a
actualizar y se te va a notificar dentro de la app antes de que esta
función se active.

## 9. Con quién compartimos datos

Asap se comunica directamente con la API de Gmail de Google desde tu
propio dispositivo para leer tus correos — no existe hoy un servidor
intermediario de Asap por el que pasen tus correos. El manejo que Google
hace de tu cuenta está sujeto a la [Política de Privacidad de
Google](https://policies.google.com/privacy).

No compartimos, vendemos ni cedemos tus datos financieros a ningún
tercero.

## 10. Seguridad

Los tokens de acceso a tu cuenta de Google son gestionados directamente
por el SDK oficial de Google Sign-In — Asap nunca los guarda en
almacenamiento sin cifrar. Los datos financieros procesados quedan en la
base de datos local de tu dispositivo, protegida por los mismos mecanismos
de seguridad del sistema operativo (sandbox de la app).

## 11. Tus derechos y control sobre tus datos

Podés en cualquier momento:

- **Desconectar un banco** desde tu perfil en la app — Asap deja de leer
  correos de ese banco (las transacciones ya sincronizadas quedan
  guardadas localmente salvo que las borres vos manualmente).
- **Revocar el acceso de Asap a tu cuenta de Google** desde
  [myaccount.google.com/permissions](https://myaccount.google.com/permissions) —
  esto corta inmediatamente cualquier posibilidad de que la app siga
  leyendo tu Gmail.
- **Eliminar todos tus datos** desinstalando la app — al ser
  almacenamiento local, no queda ninguna copia en ningún servidor de Asap.

## 12. Menores de edad

Asap no está dirigida a menores de edad y no recopila conscientemente
datos de personas que no puedan otorgar consentimiento legal para el
tratamiento de sus datos según la legislación de su país.

## 13. Cambios a esta política

**Esta política puede cambiar en el futuro**, y es importante que lo
tengas en cuenta. Podemos actualizarla a medida que la app evoluciona —
por ejemplo, al activar la función descrita en la sección 8, o si en el
futuro Asap introduce funciones pagas o un plan de suscripción (ver los
[Términos de Servicio](./TERMS_OF_SERVICE.md)), lo cual podría implicar
el procesamiento de nuevos datos (ej. de facturación) que hoy la app no
maneja. Vamos a avisar dentro de la app cuando haya cambios importantes,
antes de que entren en vigencia.

## 14. Contacto

Si tenés preguntas sobre esta política o sobre cómo Asap maneja tus datos,
escribinos a omarbonilla.v3@gmail.com.
