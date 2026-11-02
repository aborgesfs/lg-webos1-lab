# Capacidades do navegador (LG 47LB6500, webOS 1.4)

Medido com o app `apps/hello`, que roda dentro da TV.

| Item | Resultado |
|---|---|
| userAgent | Mozilla/5.0 (WebOS; Linux/SmartTV) AppleWebKit/537.41 (KHTML, like Gecko) Large Screen WebAppManager Safari/537.41 |
| Tela | 1920x1080 |
| fetch | undefined |
| Promise | undefined |
| WebSocket | object |
| localStorage | object |
| MediaSource | undefined |
| canvas | true |
| video/mp4 avc1.42E01E (H.264 baseline) | probably |
| video/mp4 avc1.640028 (H.264 high) | probably |
| video/webm vp8 | não |
| video/webm vp9 | não |
| video/mp4 hev1 (HEVC) | probably |
| application/vnd.apple.mpegurl (HLS) | maybe |
| audio/mpeg | maybe |
| audio/mp4 mp4a.40.2 (AAC) | probably |

`canPlayType` é só uma indicação: a reprodução real precisa ser testada.

## Conclusões
- Escrever JavaScript ES5, usar XMLHttpRequest (sem fetch nem Promise).
- Sem MediaSource, players web adaptativos (DASH, hls.js) e players web de streaming com DRM não funcionam.
- Netflix: erro NW-4-7. O servidor usa uma autoridade certificadora própria de 2024 que a TV não conhece, e a TV não tem as peças de que um player web moderno precisa. O app nativo provavelmente não tem mais suporte.
