# Game Asset Studio

A browser-first game asset editor and asset pipeline built for real production workflows.

## Research-driven architecture

- Fabric.js 7.4.0 for the editable scene graph, object transforms, text, filters, JSON and SVG/PNG export.
- Transformers.js 4.3.0 + Xenova/MODNet for local browser background removal.
- IndexedDB for local asset/document persistence.
- GitHub Contents API for versioned asset publishing.
- GitHub Pages + service worker for static hosting/PWA behavior.
- Agent Bridge command protocol so an external agent can execute editor operations through a controlled command file.

## Core capabilities in this first production foundation

- Multi-object canvas editor
- Text, rectangle, circle, line and free-draw tools
- Image upload and asset vault
- Local persistent asset storage
- Layer list with reorder / visibility / lock
- Object alignment, duplication and deletion
- Zoom / fit / grid / snap
- Document presets for game sprites, UI and general design
- Image filters: brightness, contrast, saturation, blur
- Background removal with local AI
- Image crop workflow
- Sprite-sheet generation from selected raster assets
- Project save/load using JSON
- PNG / SVG / JSON export
- GitHub asset publishing from the browser
- Agent command console
- Remote Agent Bridge polling from GitHub
- PWA shell

## Commercial-use note

The editor libraries used here are permissively licensed. The bundled background-removal model is Xenova/MODNet under Apache-2.0. This avoids the non-commercial-only licensing of BRIA RMBG-2.0 for the default local pipeline.

## Agent Bridge

When enabled, the application polls a configured GitHub JSON command path. An external agent can commit a command object to that path; the open editor executes the command and can optionally publish a result JSON through the user's GitHub token.

See `AGENT_PROTOCOL.md`.

## Live app

After GitHub Pages is enabled for this repository, the application is available at:

https://venom3-byte.github.io/Repository/

