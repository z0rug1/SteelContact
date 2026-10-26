# Steel Contact 2.0

Top-down 3D tank battles in the browser: armor angles and ricochets, bush sight lines and sound triangulation, artillery stun, a garage with upgrades, and peer-to-peer squad multiplayer. Runs on phones, tablets and computers. No install, no server to run.

## Put it on GitHub Pages (about 5 minutes, no coding)

1. Sign in at github.com and click **New repository** (the **+** at the top right).
2. Name it, for example `steel-contact`. Set it to **Public**. Click **Create repository**.
3. On the new repository page, click **uploading an existing file**.
4. Unzip `steel-contact-web.zip` on your computer. Open the folder, select **everything inside it** (including the `fonts` folder) and drag it into the upload area. The files must sit at the top level of the repository, not inside another folder.
5. Click **Commit changes**.
6. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, **Branch** to `main` and the folder to `/ (root)`. Click **Save**.
7. Wait a minute and refresh the Pages settings. Your game is live at
   `https://YOUR-USERNAME.github.io/steel-contact/`

Send that link to friends. It works in Chrome, Edge, Firefox and Safari on any OS. On phones, use **Add to Home Screen** to get an app icon that opens fullscreen.

To update the game later, upload the new files to the same repository; Pages redeploys on its own.

## Playing together

1. One player opens **Squad → Host room** and reads out the 5-character code.
2. Everyone else opens **Squad**, types the code and taps **Join**.
3. Each player picks a tank in their own **Garage**. The host picks map, mode and bot skill in **Battle**, chooses **Co-op vs bots** or **Versus**, then taps **Deploy squad**.

- Up to 7 players in co-op and 14 in versus. Bots fill every empty seat.
- The host's device runs the battle, so the player with the strongest device and connection should host.
- Rooms connect players directly (WebRTC). The free PeerJS service is only used to find each other. Some strict mobile or corporate networks block direct connections; if a friend can't join, try another network or let someone else host.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole game |
| `three.min.js` | 3D engine (three.js r128) |
| `peerjs.min.js` | Peer-to-peer connections (PeerJS 1.5.4) |
| `fonts/` | Saira Stencil One and Chakra Petch |
| `icon-*.png`, `manifest.webmanifest` | Home-screen icon and app manifest |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Run it on your own computer

From this folder run `python3 -m http.server 8000` and open `http://localhost:8000`. Opening `index.html` directly from disk works for single player, but multiplayer needs to be served over http(s).
