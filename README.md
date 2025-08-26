# Bingo Musical 🎵

Para mi cumpleaños se me ocurrió armar alguna actividad y esta fue una de ellas: un bingo musical. La idea entonces fue armar en forma programática $N$ cartones con $M$ canciones (15 en este caso) provenientes de una playlist de spotify que armé. 

> Ideal para eventos, reuniones o simplemente para disfrutar con amigos 😀.

## Requisitos para armar el pdf de salida

1. **Clonar el repositorio**  
2. **Crear la playlist**: crea una playlist en Spotify (asegurate de tener suficientes canciones, se van a repetir entre cartones obviamente, pero está armado para usar en forma exhaustiva al menos una vez todas). Luego obtené la url de la playlist.
3. **Configurar variables de entorno**: para obtener las keys de la API de Spotify, necesitás crear una aplicació
    - En el [Dashboard de Spotify para Desarrolladores](https://developer.spotify.com/dashboard/applications) creá una nueva aplicación y colocá como `redirect URI`=`https://localhost:8888/callback`. Guardá el `Client ID` y `Client Secret`.
   - Crear un archivo `.env` en la raíz del proyecto con las siguientes variables:  
   ```
    SPOTIFY_CLIENT_ID=<...>
    SPOTIFY_CLIENT_SECRET=<...>
    SPOTIFY_PLAYLIST_URL=<...>
    SPOTIPY_REDIRECT_URI=http://localhost:8888/callback
   ```
4. **Instalar dependencias**: hay que tener [uv](https://docs.astral.sh/uv/) instalado. Luego se puede ejectura el sync para crear el environment virtual y descargar las dependencias. 
   ```bash
   uv sync
   ```
5. Abir la notebook y usar el .venv creado para poder correrla.
6. Disfrutar 🎶
