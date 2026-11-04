# Registro de cortes — Barbería

App web para registrar cortes, cobros (efectivo / Mercado Pago), estadísticas, objetivos y pagos por barbero. Se puede instalar en el celular o la computadora como una aplicación (PWA).

Los datos se guardan en la nube (Firebase) y se sincronizan entre dispositivos. Cada cuenta tiene su propio espacio, con su propio nombre y logo (se editan en **⚙ Editables → Nombre y logo de la barbería**).

## Archivos del proyecto

Todos tienen que estar en la raíz del repositorio de GitHub:

- `index.html` — la app
- `manifest.webmanifest` — datos para instalarla como app (nombre, colores, íconos)
- `sw.js` — service worker (hace que abra rápido y trae siempre la versión nueva)
- `icons/` — íconos de la app: `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png`
- `README.md` — este archivo

## Cómo instalarla como app

- **iPhone**: abrir el link en **Safari** → botón Compartir → "Agregar a pantalla de inicio". Conviene hacerlo con la sesión ya iniciada, así queda con el nombre de la barbería.
- **Android (Chrome)**: aparece un aviso "Instalar" arriba, o menú ⋮ → "Instalar app".
- **Windows (Chrome / Edge)**: ícono de instalar en la barra de direcciones.

## Cómo actualizar la app

1. Entrá al repositorio en GitHub.
2. "Add file → Upload files" y arrastrá los archivos que cambiaron (si cambiaron los íconos, arrastrá también la carpeta `icons`).
3. Confirmá los cambios ("Commit changes").
4. Esperá uno o dos minutos — GitHub Pages se actualiza solo. La app instalada toma la versión nueva la próxima vez que se abre con internet.

## Notas

- La app necesita internet para iniciar sesión y sincronizar los datos. Sin conexión puede abrir, pero no carga los cortes.
- Para sumar otra barbería hay que crear un usuario nuevo en Firebase Authentication; al entrar por primera vez arranca como "Mi barbería" y se personaliza en Editables.
