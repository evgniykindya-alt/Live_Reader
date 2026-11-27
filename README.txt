GTA LIVE TRANSLATOR 1.1 — iPhone PWA

WHAT'S INCLUDED
- Movable subtitle selection rectangle: drag inside the green frame.
- Resizable selection rectangle: drag the green bottom-right handle.
- Saves selection position on the device.
- Rear camera capture.
- Tesseract.js OCR, English model, contrast preprocessing.
- Text stabilization (2 or 3 matching scans) before translation.
- MyMemory English-to-Russian translation with segment length handling.
- iOS speech synthesis, voice selection when Russian voices are exposed.
- Manual translation + voice test, history, status and error messages.
- PWA manifest and service worker shell.

IMPORTANT
This is a camera/OCR subtitle translator. It does NOT listen to the game's audio and cannot translate dialogue that has no visible subtitles.
PWA must remain in foreground with screen awake. iOS may suspend camera/JavaScript if the app is backgrounded or locked.
Connect AirPods to iPhone before starting. The browser cannot force a specific output route; iOS routes speech to the currently selected audio output.
First launch needs internet to load Tesseract.js and its English model. Every new subtitle also needs internet for MyMemory.
MyMemory anonymous limit is 5,000 characters/day according to its published limit page; service availability and translation quality are not guaranteed.
Do not use this prototype for confidential text. The translation text is sent to MyMemory.
Camera permission requires HTTPS. Opening index.html directly from Files is not a reliable deployment method.
A free public API is used to avoid requiring the user to create an API key. For a stable production service, replace it with a private backend and a provider with a suitable SLA.

DEPLOY TO GITHUB PAGES (simple free option)
1. On a computer, create a GitHub repository (for example gta-live-translator).
2. Upload index.html, manifest.webmanifest, sw.js, icon.svg.
3. In repository Settings -> Pages, select Deploy from a branch, choose main and /(root), Save.
4. Wait for GitHub Pages to publish the HTTPS address.
5. On iPhone, open that HTTPS address in Safari.
6. Tap Share -> Add to Home Screen -> Add.
7. Open the installed app from Home Screen (not from a local file preview).

FIRST-RUN CHECKLIST
1. Pair AirPods in iOS Settings -> Bluetooth and select them as audio output in Control Center.
2. Open the PWA; keep screen awake (temporarily set Auto-Lock to Never if desired).
3. Tap "Проверить русский голос и AirPods". Confirm you hear Russian speech.
4. Enter an English sample in "Тест перевода без камеры", tap "Перевести и озвучить тест".
5. Tap "Запустить камеру" and grant camera permission.
6. Put iPhone on a stable stand facing the TV. Drag the green frame over the subtitle area. Resize using the bottom-right green handle.
7. In GTA, enable English subtitles and increase subtitle size if possible.
8. Wait for the same subtitle to be detected 2 or 3 times. Translation then appears and is spoken.
9. If the frame misses text, stop scanning, reposition, then tap "Проверить область".

TROUBLESHOOTING
- Camera doesn't start: verify HTTPS, Safari camera permission, and no other app is using camera.
- OCR library won't load: check internet, reload PWA; first-time OCR downloads large assets.
- No text: enlarge subtitles, improve lighting/focus, reduce glare, align frame exactly around subtitle lines.
- Translation fails: public MyMemory may be unavailable or quota-limited; try later. It has a daily anonymous quota.
- No voice: test the voice button first, check iPhone silent/focus/audio output/volume, select an available Russian voice. If no Russian voice is listed, install a Russian voice in iOS Accessibility -> Spoken Content -> Voices (menu names can vary).
- No sound in AirPods: connect AirPods before launching and choose them as output in Control Center. The app cannot independently route browser TTS to AirPods.
- App pauses when switching away: expected iOS PWA limitation; keep it foregrounded.
