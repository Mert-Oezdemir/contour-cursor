# Contour Cursor

An interactive SVG map of fictional terrain. Open `index.html` in a current browser. The app runs offline and uses no dependencies.

- Choose a terrain and adjust the contour density and probe influence.
- Move the mouse or tap the map to reshape the nearby lines. Focus the map and use the arrow keys to move the probe. Hold Shift for larger steps.
- With reduced motion enabled, click or tap to place the probe. The map stays still between actions.
- Save the current map as a standalone SVG.

The interface, mathematical shapes, artwork, and code were created independently. [Concept reference](https://github.com/YildizDikme/SVG-Animation-Mousemove)

## Local server and agent connection

Install Node 22 or newer and Git. From this repository run:

```sh
npm ci
npm start
```

Open the loopback URL printed by the command. The runtime is pinned to a specific revision of [Project Agent Bridge](https://github.com/Mert-Oezdemir/project-agent-bridge).

To connect an MCP-compatible agent, run `npm run mcp:config --silent` and add its `mcpServers` entry to your host. Run `npm run doctor` to see local project and account configuration.

Chrome or Edge is needed for agent browser controls. You can set `CHROME` in `.env`, or run `npx playwright install chromium` to install a browser.

Copy `.env.example` to `.env` before adding account settings. Keep `.env` local. Restart the runtime after changing it.
