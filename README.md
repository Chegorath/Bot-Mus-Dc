# Bot-Mus-Dc

Bot de música para Discord basado en **discord.js v14** y **Lavalink v4**. Reproduce audio desde YouTube, SoundCloud, Twitch y más en canales de voz.

## Requisitos

- **Node.js** 18+
- **Java** 17+ (para Lavalink)
- Un bot de Discord con token (https://discord.com/developers/applications)

## Estructura

```
App/          → Bot de Node.js (TypeScript)
Server/       → Servidor de audio Lavalink (Java)
```

## Configuración

### 1. Token de Discord

Copia `App/.env.example` a `App/.env` y completa:

```env
DISCORD_TOKEN=tu_token_aqui
LAVALINK_HOST=localhost
LAVALINK_PORT=8080
LAVALINK_PASSWORD=youshallnotpass
```

### 2. Lavalink (Servidor de audio)

```bash
cd Server
java -jar Lavalink.jar
```

Espera a que aparezca `"Started Launcher"`.

### 3. Bot

En otra terminal:

```bash
cd App
npm install
npm run dev
```

## Comandos

| Comando   | Descripción                     |
|-----------|---------------------------------|
| `/play`   | Busca y reproduce una canción   |
| `/skip`   | Salta a la siguiente canción    |
| `/pause`  | Pausa la reproducción           |
| `/resume` | Reanuda la reproducción         |
| `/stop`   | Detiene y limpia la cola        |
| `/queue`  | Muestra la cola de reproducción |

## Producción

```bash
cd App
npm run build
npm start
```
