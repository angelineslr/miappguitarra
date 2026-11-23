# Mi guitarra

App web para aprender guitarra: biblioteca de acordes con diagramas y sonido, práctica de cambios y de progresiones de 2 a 5 acordes, biblioteca de ritmos con vídeo, test, progreso diario y canciones con vídeo de YouTube.

No necesita instalar nada ni tiene servidor. Todo se guarda en el navegador de cada dispositivo.

## Publicarla en GitHub Pages

1. En GitHub, crea un repositorio nuevo (por ejemplo `guitarra`). Ponle un nombre que no incluya tu nombre real si quieres discreción.
2. Sube a la raíz del repositorio estos archivos: `index.html`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png`.
3. Ve a **Settings → Pages**. En *Build and deployment* elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`. Guarda.
4. Espera un par de minutos. La dirección será `https://TU-USUARIO.github.io/guitarra/`.
5. En el móvil, ábrela y elige **Añadir a pantalla de inicio** para usarla como una app.

Importante: con una cuenta gratuita, el repositorio de una página pública es público. La app no incluye letras ni acordes de canciones (las pegas tú y quedan en tu navegador), pero quien tenga la dirección podría abrirla. El archivo `index.html` lleva `noindex` para que los buscadores no la listen.

## Probarla en tu ordenador antes de subirla

Los vídeos de YouTube no se reproducen si abres `index.html` con doble clic (YouTube exige una dirección web). Para probar en local:

```
cd carpeta-de-la-app
python3 -m http.server 8000
```

y abre `http://localhost:8000`.

## Copias de seguridad

Tus canciones, marcas de tiempo y progreso viven en el navegador. En **Progreso → Copia de seguridad** puedes exportarlos a un archivo y volver a importarlos (por ejemplo, en el móvil).

## Cómo usar una canción con vídeo

1. **Canciones → Nueva canción.** Pega los acordes sobre la letra tal como aparecen en las webs de cifras, y el enlace del vídeo.
2. Abre la canción y pulsa **⏱ Sincronizar**. Pon el vídeo y pulsa el botón grande (o la barra espaciadora) justo cuando empiece cada acorde. Solo hay que hacerlo una vez.
3. Después, al reproducir, el acorde actual se resalta en la letra y ves el siguiente. Con **A / B / ↻** repites un fragmento, con **↻** junto a cada línea repites esa línea, y con el selector bajas la velocidad (0,5×, 0,75×).

## Progresiones y ritmos

- **Practicar → Progresiones:** elige 2, 3, 4 o 5 acordes, la tonalidad, una progresión habitual y un ritmo. La app marca el acorde actual, el siguiente y el patrón de golpes al compás.
- **Ritmos:** cinco patrones predefinidos y los que crees tú (toca cada casilla para cambiar el golpe). A cada ritmo le puedes asociar un vídeo de YouTube con el segundo en que empieza y termina el fragmento: la app salta ahí y lo repite en bucle, también a menos velocidad.
- Un ritmo se puede asignar a una canción (al editarla) y se practica con cualquier progresión.


## Novedades de la versión 3
- Interfaz nueva, clara y minimalista: barra lateral en el ordenador, navegación inferior en el móvil, modo oscuro automático.
- En una canción, el ordenador muestra vídeo/controles a la izquierda y la letra a la derecha.
- Sincronización «por líneas» (rápido) o «acorde a acorde» (preciso), ajuste de ±0,1 s, barra de posición y retroceso de 5 s.
- Audio propio: puedes elegir un archivo de audio en una canción; se guarda solo en ese dispositivo y sustituye al vídeo.
