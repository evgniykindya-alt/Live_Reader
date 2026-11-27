GTA Live Translator 1.0 — PWA prototype

FILES
- index.html: application
- manifest.webmanifest: install metadata
- sw.js: basic offline shell cache

HOW TO RUN ON IPHONE
1. Host this folder on an HTTPS static host (GitHub Pages, Netlify, Cloudflare Pages, etc.).
2. Open the HTTPS address in Safari on iPhone.
3. Tap Share -> Add to Home Screen.
4. Launch the installed PWA, allow camera access, connect AirPods, then tap "Включить камеру".
5. Aim the rear camera at the TV. Adjust the green subtitle frame using the sliders.

IMPORTANT LIMITATIONS
- This is an OCR subtitle prototype, not audio speech recognition. It only translates visible English text.
- It uses the public MyMemory translation endpoint without an API key. Availability, speed, quotas, and privacy are not guaranteed.
- Browser speech synthesis uses voices provided by iOS. Voice routing to AirPods depends on iOS audio routing.
- Keep the PWA in the foreground. iOS may suspend camera and JavaScript when the app is backgrounded or the screen locks.
- First launch requires internet to load Tesseract.js and its English model.
- The public translation endpoint is called from the browser. Do not use this prototype for confidential text.
- Camera access requires HTTPS (or localhost); opening index.html directly from Files will not reliably work.
- OCR speed and accuracy depend on TV distance, focus, glare, subtitle size, contrast, and camera stability.

NEXT IMPROVEMENTS
- Replace public translation endpoint with a private server proxy and a configurable provider.
- Add crop positioning controls (left/right/width), image preprocessing, subtitle line stabilization, and better handling of two-line captions.
- Test actual iPhone Safari speech synthesis and AirPods routing.
