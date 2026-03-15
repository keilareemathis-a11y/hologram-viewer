# hologram-viewer

A hologram character chatbot powered by [Three.js](https://threejs.org/) and the [OpenAI API](https://platform.openai.com/).

## Features

- **3D hologram scene** – renders a rotating GLTF character model (falls back to a cyan wireframe sphere if the model is missing).
- **Chat interface** – send messages to the hologram and receive AI-generated replies using `gpt-4o-mini`.
- **Accessible** – keyboard-navigable, ARIA-labelled, and screen-reader friendly.
- **API key stored locally** – your OpenAI API key is saved in `localStorage` and never sent anywhere except the OpenAI API.

## Usage

1. **Provide your character model** (optional): place a `character.glb` file in the same directory as `index.html`. If none is found, a wireframe sphere is displayed instead.
2. **Open `index.html`** in a browser (or serve the directory with a local HTTP server, e.g. `npx serve .`).
3. **Enter your OpenAI API key** in the top-right field and click **Save Key**.
4. Type a message in the chat input at the bottom and press **Send** (or hit Enter) to talk to the hologram.

## Getting an OpenAI API key

Visit [https://platform.openai.com/api-keys](https://platform.openai.com/api-keys) to create an API key. You will be charged according to OpenAI's usage pricing.

## Local development

```bash
npx serve .
# then open http://localhost:3000
```

## Accessibility

- All interactive elements are keyboard-accessible and have visible focus indicators.
- The chat log uses `role="log"` and `aria-live="polite"` so screen readers announce new messages.
- Status messages (e.g. "Hologram is thinking…") are announced via `aria-live`.

