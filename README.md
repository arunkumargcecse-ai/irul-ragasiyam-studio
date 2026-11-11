# IRUL RAGASIYAM Studio — v0.1

Offline-first, Android-friendly PWA foundation for producing Tamil mystery Shorts.

## Included
- Responsive mobile dashboard
- Local episode library (browser localStorage)
- Episode workspace for Tamil script, voice direction and visual prompts
- Production checklist
- Copyable AI production prompt and narrator direction
- JSON export/import backup
- PWA manifest, service worker and icon for install/offline use

## Run locally for development
A PWA service worker requires HTTPS or localhost. From this folder run:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080` on the development machine. For Android installation, deploy the folder to an HTTPS static host (for example, a GitHub Pages repository) and open the HTTPS URL in Chrome. Use Chrome menu → Add to Home screen / Install app.

## Important limitations of v0.1
- No AI model is connected yet; prompt generation is local and does not claim to generate content.
- No video rendering or YouTube upload yet.
- Data is stored in this browser on this device. Export JSON backups regularly. Clearing browser storage can erase episodes.
- Never put API keys in frontend JavaScript. Future online providers must be called through a secure backend or a local trusted bridge.

## Next phases
1. Provider-neutral backend/adapter interface.
2. Script generation provider and Tamil TTS adapter.
3. Image generation adapter and consistent character references.
4. Video assembly pipeline (FFmpeg where supported) and subtitle timing.
5. QC checks, YouTube OAuth upload and analytics.
