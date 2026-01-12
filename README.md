# MobileCoder — Mobile VS Code-like IDE (Expo + React Native)

MobileCoder is a public demo: a mobile IDE-like web app (Expo web) with Monaco editor in a WebView for editing HTML/CSS/JS, live preview, and a Chat panel that can send content to an OpenAI serverless endpoint (opt-in consent).

Quick start

Prerequisites:
- Node.js 16+
- Yarn or npm
- Expo CLI: `npm install -g expo-cli` (optional)
- EAS CLI for builds: `npm install -g eas-cli` (optional)

Install and run:
```bash
yarn install
npx expo start
```
Open the project on your phone with Expo Go or in the browser via `expo start --web`.

What’s included
- App.tsx — entry
- src/screens/MainScreen.tsx — responsive layout (Editor / Preview / Chat)
- src/components/EditorWebView.tsx — Monaco editor in WebView
- src/components/PreviewWebView.tsx — Live HTML preview
- src/components/ChatPanel.tsx — Chat UI stub with consent toggle
- src/adapters/openaiAdapter.ts — server-side OpenAI adapter (used by serverless function)
- src/sandbox/sandboxStub.ts — placeholder for run/snippet (demo)
- api/openai.ts — serverless proxy endpoint for OpenAI (Vercel)
- .github/workflows/deploy-openai.yml — CI / build example
- .env.example — example env vars

Notes & Privacy
- The OpenAI API key is never included in client-side code. If you enable OpenAI in the demo, set the secret OPENAI_API_KEY in Vercel/host environment.
- The Chat panel requires user consent before sending any workspace content to the serverless OpenAI endpoint.

Credits
- Generated and assembled by MobileCoder assistant.