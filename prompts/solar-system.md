# The "fly through the solar system" master prompt

This prompt rebuilds the solar-system experience from my "Can Claude do it? #2" reel. You fly a spaceship from Earth to Pluto at up to thousands of times the speed of light. The stars stretch as you speed up, and every planet and moon is there to fly past.

**How to use it:**
1. Open Claude Code (or Claude.ai with a high-effort model; I used Fable 5.2 on high).
2. Paste everything in the box below.
3. When it's done, open `index.html` in Chrome. If textures don't load, run `npx serve .` in the folder and open the link it prints.

---

```text
Build me a cinematic, interactive 3D solar system I can fly through in a spaceship. It runs in the browser, opens from a single index.html, and has no build step. Use three.js from a CDN (pin an exact version). Make it look like a film, not a school diagram.

THE EXPERIENCE
- It opens on a title screen: "SOL" in thin, widely spaced letters over a slow shot of Earth, with "Press any key to launch" underneath.
- Then I'm in a third-person chase camera behind a sleek white spaceship parked next to Earth. Earth shows real continents and a day/night side lit for today's date and time.
- I fly with the keyboard: W/S throttle, A/D and the arrow keys or mouse to steer, Shift to boost, H to show and hide a controls panel.
- Keys 1-9 and 0 auto-travel to the Sun, Mercury, Venus, Earth, Mars, Jupiter, Saturn, Uranus, Neptune and Pluto. The ship turns, accelerates to warp, cruises and slows down so it arrives in a nice framing next to the planet.

THE UNIVERSE
- The Sun, all 8 planets and Pluto, at their real relative sizes and real orbital positions for today's date (use simplified Keplerian orbital elements). Distances can be compressed so the trip is fun, but keep the order and the relative spacing believable.
- Planet looks: Mars with polar ice caps and craters, Jupiter with its bands and the Great Red Spot, Saturn with rings that cast a shadow, Uranus tilted on its side. Generate textures procedurally in canvas or shaders, or load public-domain NASA textures from a reliable CDN with a procedural fallback, so nothing breaks offline.
- The main moons: the Moon, Phobos and Deimos, the four Galilean moons, Titan, and Charon. Each one is cratered and lit from the Sun.
- The Sun is a glowing body with a corona, bloom and a lens flare that shows when it's in frame. It is the only light source, so the night sides of planets are dark.
- The background is a dense starfield with the Milky Way band, coloured stars of varied brightness, and soft nebula dust.

SPEED AND RELATIVITY (the money shot)
- Speed runs from km/s up to thousands of times the speed of light (at least 3,000× light).
- As I accelerate past light speed, the stars stretch into streaks toward the direction I'm flying. The streaks get longer with speed. Add subtle chromatic aberration at the edges, a slight vignette and a camera shake that scales with speed. The engines' blue exhaust grows brighter and longer.
- Starlight shifts subtly blue ahead and red behind as speed rises (stylised, not exact).
- Dropping out of warp is quick and satisfying: the streaks snap back into points.

THE HUD (clean, minimal, sci-fi; thin sans-serif type; small uppercase labels with wide letter spacing)
- Top left: "NEAREST BODY", the planet's name in large type, a one-line fact about it, and the altitude in km.
- Bottom left: "VELOCITY" as a big number with its unit (km/s, switching to "× light" above light speed), an orange throttle bar, and the throttle percentage.
- Bottom centre: a row of planet names (SUN MERCURY VENUS EARTH MARS JUPITER SATURN URANUS NEPTUNE PLUTO). The nearest one is highlighted and each is clickable to travel there.
- Bottom right: the simulated date and time in UTC.
- Faint labels float next to planets in the distance, so I can see where things are.

QUALITY BAR
- It runs at 60 fps on a laptop: use instancing for stars, a logarithmic depth buffer for the huge scale range, and floating-origin rebasing so nothing jitters far from the Sun.
- Post-processing: bloom, tone mapping and FXAA, all through three.js's examples addons.
- Nothing ever looks broken: no z-fighting, no flickering, no planet popping in, no textures that fail silently.
- Before you say it's done, open it in a browser, fly from Earth to Mars to Jupiter to Pluto, take screenshots along the way, and fix anything that looks wrong. Then tell me which keys to press for the best shots.
```

---

Made by [@official_arnavkapoor](https://www.instagram.com/official_arnavkapoor/). Follow for more "Can Claude do it?" episodes and free prompts.
