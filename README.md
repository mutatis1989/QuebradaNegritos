# Quebrada Negritos – Sitio de vigilancia comunitaria

Este directorio contiene una estructura mínima de sitio web estático para el proyecto **Quebrada&nbsp;Negritos**, que puedes desplegar en [Cloudflare Pages](https://pages.cloudflare.com/) o [GitHub Pages](https://pages.github.com/).

## Estructura de archivos

- `index.html`: Página de inicio con la transmisión en vivo, un resumen de la misión y accesos a las demás secciones.
- `about.html`: Historia y objetivos del proyecto.
- `guidelines.html`: Reglas de publicación y uso responsable.
- `report.html`: Instrucciones para denunciar incendios, tala, inundaciones u obras ilegales; incluye contactos.
- `upload.html`: Página que contiene el iframe de Google Forms para subir fotos y vídeos.
- `gallery/`: Contiene `index.html`, la galería donde se mostrarán las imágenes y vídeos aprobados.
- `styles.css`: Hoja de estilos simple para un diseño limpio y responsivo.
- `_headers` (opcional): Configuraciones de seguridad para Cloudflare Pages, como Content-Security-Policy.

## Cómo usar

1. **Clona** este repositorio en tu cuenta de GitHub.
2. Copia el contenido de este directorio (`quebradanegritos_site`) al raíz de tu repositorio.
3. Reemplaza `VIDEO_ID` en `index.html` por el ID de la transmisión en YouTube (aparece en la URL de tu stream). Ejemplo: si la URL es `https://www.youtube.com/watch?v=abc123`, entonces `VIDEO_ID` es `abc123`.
4. Crea un **Google Form** con la opción de carga de archivos y copia su ID en `upload.html` (`TU_FORM_ID`). Configura el formulario para que almacene las respuestas en una carpeta de Google Drive en modo revisión.
5. Personaliza el contenido de cada página según tus necesidades. Puedes añadir imágenes, logos y enlaces adicionales.
6. Sube los cambios a GitHub. Si usas Cloudflare Pages, vincula el repositorio y activa el dominio personalizado (`quebradanegritos.org`). Si prefieres GitHub Pages, ve a _Settings → Pages_ y selecciona la rama `main` y la carpeta raíz (`/`).

## Seguridad

Para proteger la cámara y la red local:

- No abras puertos ni actives UPnP en el router. Utiliza un servidor local para retransmitir a YouTube.
- Configura una VLAN separada para la cámara y limita la salida de red únicamente al servidor de streaming.
- Actualiza el firmware de la cámara Hikvision y usa contraseñas robustas.
- Habilita `https` y cabeceras de seguridad en el sitio (ver archivo `_headers`).

## Licencia

Este material se proporciona sin garantía, bajo una licencia de uso libre no comercial. Crédito al equipo comunitario de Quebrada&nbsp;Negritos.