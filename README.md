# Stranger-things
stranger Things — The Upside Down Messenger  A 3D interactive room where you can communicate with Will Byers through Christmas lights.
 Preview
A fully interactive 3D recreation of Joyce Byers' living room from Stranger Things — complete with floral wallpaper, Christmas lights, alphabet wall, and a synthesized Stranger Things score. Ask Will anything and watch the lights spell out his cryptic response.

🚀 Quick Start
live demo : https://savewill.netlify.app

✨ Features
🏠 3D Room

Full Three.js perspective room — back wall, side walls, floor, ceiling
Floral wallpaper — authentic 80s pattern with dark wood wainscoting panel
Three rows of Christmas lights strung on drooping wire curves above the alphabet
Sofa with cushions and a draped blanket
Coffee table with scattered books and papers
Flickering candles, floor lamp

💡 Light System

Bulbs twinkle randomly in the background at all times — the room always breathes
When you ask Will something → all lights cut → flicker sequence → spells the answer letter by letter with colored bulbs
Each lit bulb emits colored point light that washes the wall (red, green, yellow, blue, orange, purple)
Idle twinkle fires randomly every 100ms across all 26 alphabet bulbs

🎵 Synthesized Stranger Things Score
Built entirely with the Web Audio API — no files, no CDN, works offline:
LayerDescriptionBass padsTwo detuned sawtooth oscillators at 55Hz + 55.7HzMelodyE minor arpeggio — same intervals as the actual ST themeChord padsEm → Am → Gm triangle wave sustains underneathShimmerSine waves at 880Hz + 1108HzRain textureLowpass-filtered white noise
Click ♪ MUTE (top-right) to toggle audio.
🤖 AI Responses — Pollinations AI
Powered by Pollinations AI — Will responds in character:

"RUN - DONT STOP"
"THEY ARE WATCHING"
"CLOSE EYES - RUN"

Falls back to built-in cryptic phrases if the API is unavailable.
🌑 Upside Down Mode
Type RUNWILL to enter The Upside Down:

Red fog sphere fills the room
3D vines crawl in from the ceiling
All lights turn blood red
Synthesizer drones drop in pitch
Will's responses become more desperate and fragmented
Type RUNWILL again to return

👻 Return Visitor Detection
Uses localStorage — if you've visited before, the lights automatically spell:

"YOU CAME BACK. I KNEW YOU WOULD."

🖱️ Mouse Parallax
Camera subtly floats as you move your mouse — makes the room feel alive.

🎮 How to Use
ActionWhat happensClick / press any keyStarts audioType a question → press Enter or SENDWill responds through the lightsType RUNWILLToggle Upside Down modeMove mouseCamera parallax floatsClick ♪ MUTEToggle synthesized music

🛠️ Tech Stack
TechnologyUsageThree.js r1283D scene, room geometry, lighting, materialsWeb Audio APISynthesized music, click sounds, flicker SFXCanvas APIProcedural textures (floral wallpaper, wood floor, ceiling)Pollinations AIFree AI text generation for Will's responsesCSS AnimationsVine overlays, loading screen, return message flickerlocalStorageReturn visitor detection
Zero npm. Zero build. Zero server. Everything runs in a single .html file.

📁 Project Structure
stranger-things-messenger/
│
├── stranger-things.html     # The entire project — open this
└── README.md
That's it. The whole thing is one self-contained HTML file (~800 lines).

🎨 Scene Details
Alphabet Wall

Letters A–Z painted in Permanent Marker font, dark paint on floral wallpaper
3 rows: ABCDEFGH / IJKLMNOPQ / RSTUVWXYZ
Each letter has its own Christmas bulb above it
Bulbs: red, yellow, green, blue, orange, purple, cyan, pink

⚙️ Configuration
All tweakable values are near the top of the <script> block:
javascript// Spelling speed (ms per letter)
await sleep(520);           // ← increase for slower, decrease for faster

// Hold time after spelling
await sleep(5500);          // ← how long letters stay lit

// Bulb brightness when lit
bl.intensity = 3.0;         // ← alphabet bulb intensity

// Camera height (eye level)
const camBase = new THREE.Vector3(0, 1.55, 5.2);

// Fog density
scene.fog = new THREE.FogExp2(0x180a02, 0.022);

// Renderer exposure
renderer.toneMappingExposure = 1.4;



Note: Audio requires a user gesture (click or keypress) to start due to browser autoplay policies.


📜 License
This project is a fan-made creative tribute to Stranger Things. It is not affiliated with or endorsed by Netflix or the Duffer Brothers.

Three.js — MIT License
Pollinations AI — Free API
Fonts (Permanent Marker, Special Elite) — Google Fonts Open Font License


🙏 Credits

Stranger Things created by Matt & Ross Duffer (The Duffer Brothers)
Kyle Dixon & Michael Stein — original Stranger Things score (inspiration for the synthesized music)
Three.js by Mr.doob and contributors
Pollinations AI for free generative text API


"She's trying to talk to us... I can feel it." — Joyce Byers
