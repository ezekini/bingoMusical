# Bingo Musical 🎵

Para mi cumpleaños se me ocurrió armar alguna actividad y esta fue una de ellas: un bingo musical. La idea entonces fue hacer en forma programática $N$ cartones con $M$ canciones (15 en este caso, pero se puede modificar) provenientes de una playlist de spotify.

> Ideal para eventos, reuniones o simplemente para disfrutar con amigos 😀.

## Requisitos para armar el pdf de salida

1. **Clonar el repositorio** y moverse a la carpeta del proyecto:
   ```bash
   git clone https://github.com/ezekini/bingoMusical.git
   cd bingoMusical
   ```
2. **Crear la playlist**: crea una playlist en Spotify (asegurate de tener suficientes canciones, se van a repetir entre cartones obviamente, pero está armado para usar en forma exhaustiva al menos una vez todas). Luego guardá la url de la playlist yendo a `share` -> `copy link to playlist`.

3. **Configurar variables de entorno**: para obtener las keys de la API de Spotify y poder traer los tracks, necesitás crear una aplicación
    - En el [Dashboard de Spotify para Desarrolladores](https://developer.spotify.com/dashboard/applications) creá una nueva aplicación, la mayoría de los campos son irrelevantes, pero es importante colocar como `redirect URI`=`http://127.0.0.1:8888/callback`. Guardá el `Client ID` y `Client Secret` que te devuelva.
   - Crear un archivo `.env` en la raíz del proyecto con las siguientes variables y completalo con los datos correspondientes:  
   ```
    SPOTIFY_CLIENT_ID=<...>
    SPOTIFY_CLIENT_SECRET=<...>
    SPOTIFY_PLAYLIST_URL=<...>
    SPOTIPY_REDIRECT_URI=http://127.0.0.1:8888/callback
   ```
4. **Instalar dependencias**: hay que tener [uv](https://docs.astral.sh/uv/) instalado. Luego se puede ejectura el sync para crear el ambiente virtual para instalar las dependencias. 
   ```bash
   uv sync
   ```
5. Abrir la notebook. `VScode` debería reconocer automáticamente el .venv creado para usarlo como kernel en la notebook, si usan otra IDE habrá que googlear, si usan jupyter nativo, hay que registrar el kernel, también googlear.
6. **Ejecutar la notebook**: correr todas las celdas de la notebook `bingo.ipynb`. Hay algunas cosas parametrizadas, como cantidad de cartones, cantidad de canciones por cartón, etc. También se puede modificar un diccionario para hacer algunos reemplazos de nombres. Al ir a buscar los tracks se debería abrir el navegador para autorizar ir a buscar las canciones de una playlist privada. Al finalizar se va a generar un archivo `.pdf` en la raíz del proyecto con los cartones generados listo para imprimir ♥️⁠╣⁠[⁠-⁠_⁠-⁠]⁠╠⁠♥️.

7. Disfrutar 🎶
