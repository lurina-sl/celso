# Fluxer Music Bot

Bot modular e pronto para Fluxer com camada de reprodução, fila por servidor, armazenamento SQLite e suporte a várias fontes de áudio.

## Requisitos

- Node.js 20+
- npm
- Token do bot Fluxer
- Fluxer API e Gateway válidos
- (Opcional) servidor de áudio compatível com LiveKit / NodeLink / Lavalink
- FFmpeg instalado caso você queira converter ou normalizar arquivos de áudio

## Observação importante sobre Fluxer

A documentação oficial do Fluxer ainda está evoluindo, especialmente nas áreas de autenticação, gateway, voice e LiveKit. Esta base foi montada com arquitetura modular para facilitar a adaptação à SDK e ao ambiente real do Fluxer, sem inventar endpoints ou eventos.

## Estrutura do projeto

```text
fluxer-music-bot/
├── src/
│   ├── app.ts
│   ├── index.ts
│   ├── bot/
│   │   ├── client.ts
│   │   └── commandRegistry.ts
│   ├── commands/
│   │   └── music.ts
│   ├── config/
│   │   └── env.ts
│   ├── database/
│   │   ├── database.ts
│   │   ├── models/
│   │   │   └── serverSettings.ts
│   │   └── repositories/
│   │       └── serverSettingsRepository.ts
│   ├── music/
│   │   ├── Player.ts
│   │   ├── PlayerManager.ts
│   │   ├── Queue.ts
│   │   ├── Track.ts
│   │   ├── types.ts
│   │   ├── resolver/
│   │   │   └── TrackResolver.ts
│   │   └── sources/
│   │       ├── AudioSource.ts
│   │       ├── DirectUrlSource.ts
│   │       ├── SoundCloudSource.ts
│   │       ├── YouTubeSource.ts
│   │       └── index.ts
│   ├── types/
│   │   └── fluxer.ts
│   ├── utils/
│   │   ├── errors.ts
│   │   ├── logger.ts
│   │   └── validators.ts
│   └── voice/
│       ├── ConnectionManager.ts
│       └── VoiceManager.ts
├── .env.example
├── .gitignore
├── package.json
├── tsconfig.json
├── README.md
└── LICENSE
