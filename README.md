# Splendor Frontend


## Overview
This repository contains the frontend implementation for the Splendor board game.

* **Backend Repository:** [Alexander-Engelrelst/splendor-backend](https://github.com/Alexander-Engelrelst/splendor-backend)
* **Live Demo:** [Watch a demo of a piece of the game](https://www.loom.com/share/d156d120143a4d4a81d36eae74e5b5ba)
## Credits
* **Team:** Developed by
  * [Alexander Engelrelst](https://github.com/Alexander-Engelrelst)
  * [Tim Pirotte](https://github.com/Tim-Pirotte)
  * [Tristan Joos](https://github.com/TristanJoos)
  * [Niels Clarysse](https://github.com/ItsClaryPro)
  * [Arne Persyn](https://github.com/arpe18)
  * [Niels Ryserhove](https://github.com/mobley84)

### Special Mention
Both the card collection system and the animation system must in its entirety be credited to **Tim Pirotte**.

## Usage
To use this project the following must be done:
1. run the backend implementation of the game as described in the backend repository.
2. open the `index.html` file in a browser to start the game.

The configuration of the game can be changed in the `config.js` file. Currently it is set to work out of the box when the backend is running locally on port 8080.
<

## Key Highlights
- **Game State Machine:** Clean flow control managing client-side game states: [state-machine.js](src/assets/js/board-component/state-machine/state-machine.js)
- **FLIP Animation Engine:** Custom library built to handle complex smooth state transitions using FLIP principles: [animation-handler.js](src/assets/js/board-component/animation-component/animation-handler.js)
- **Animation Template Engine:** Lightweight template renderer for dynamic variable and function injection into UI animations: [template-renderer.js](src/assets/js/board-component/animation-component/template-renderer.js)
- **Tree-Structured Card Storage:** Memory-optimized tree data structure used to manage collected player cards: [card-collection.js](src/assets/js/card-collection-component/card-collection.js)
- **Centralized API Client:** Unified abstraction layer for server communication: [api.js](src/assets/js/api.js)
- **Multifunctional Action Interface:** Context-aware UI button handling dynamic player actions: [game-status-interface.js](src/assets/js/board-component/game-status-interface.js)
- **Custom Cryptography & Utilities:** Synchronous SHA-256 hash utility ([crypto.js](src/assets/js/utils/crypto.js)) and dynamic lobby invite link generator ([handler.js](src/assets/js/lobby-component/handler.js)).
- **Audio Engine:** Custom sound effects subsystem: [sound.js](src/assets/js/sound-component/sound.js)
- **Code Quality & Style:** Configured ESLint rules for codebase consistency: [eslint.config.mjs](eslint.config.mjs)

All assets are custom-made with inspiration drawn from the internet.

## Known Limitations & Design Compromises
Due to project constraints the frontend relies heavily on DOM `dataset` attributes for state management.

## Quality Assurance & API Testing
* **Reference API Bug Report:** Discovered and formally documented a server-side bug vulnerability in the course reference server used during development of this frontend. View the **[Formal Bug Report](./src/docs/BUG_REPORT_SPEC_SERVER.md)**.