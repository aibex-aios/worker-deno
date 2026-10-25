# worker-deno

Arbeitspferd von AIbex AIOS (Typ `worker`, Version 0.1.0): die JavaScript- und TypeScript-Laufzeit [deno](https://deno.com) 2.9.8, installiert aus den Wheels von PyPI. `yt-dlp` nutzt sie als JS-Runtime (`worker-yt-dlp`).

## Holen

**Voraussetzung:** AIbex AIOS v0.5 ist installiert und das Projekt aktiviert.

```bash
aios --fetch worker-deno
```

Der Plan zeigt das Paket `deno==2.9.8`; nach dem Ja richtet AIOS die Version einmal auf dem Rechner ein (`/opt/aios/workers/worker-deno/v0.1.0/`, sonst `~/.aios/workers/`). Aufruf über den Weiterleiter `~/.aios/bin/deno`; er nimmt die Version, die `lock.yaml` des nächsten Projekts der Kette sperrt.

## Plattformen

macOS arm64 und x86_64, Linux x86_64 und aarch64 mit glibc ab 2.27. `worker/requirements.lock` enthält die Hashes aller Wheels von PyPI.

## Lizenz

Das Paket steht unter der Apache License 2.0 (`LICENSE`, `NOTICE`). deno selbst steht unter der MIT-Lizenz.
