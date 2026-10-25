# Let's Dive — Shark ScrollWorld

A scroll-driven watercolor journey from a sunlit reef into the deep ocean.

<!-- TODO: add a screenshot or GIF at assets/readme/preview.gif (the image does not exist yet). -->
![Preview of Let's Dive](assets/readme/preview.gif)

**[Live demo](https://sharkscrollworld.vercel.app/)**

## About

- A mostly wordless story. Scroll down to dive, scroll up to go back.
- You put on a diving mask and meet sharks as the water grows darker.
- At the bottom you find a megalodon fossil that sparks a brief ancient vision.
- Originally built for Dev Assignment 2 at Thomas More University of Applied Sciences.

**Story order:** diving mask and dive → blacktip reef shark → whale sharks → hammerheads → great white (including its feeding among the fish) → top-view sixgill → fossil tooth → megalodon mouth → the fossil pulls back as a giant shape passes → fin.

## Features

- **Reversible scroll story.** Animation clips are JPEG frames painted onto a canvas that follows scroll position in both directions. Scrolling back never flashes or glitches.
- **Smooth motion.** A short scroll glide and eased watercolor dissolves.
- **Entry gate.** A frosted pane with the title, rising bubbles, a loading bar and two choices: "Dive in with sound" or "Dive in quietly". It opens anyway after 12 seconds, so it never traps a visitor.
- **Chapter links.** Surface, Reef, Open water, The deep, The ancient, Fin. They jump to that point and highlight the current chapter.
- **Depth gauge.** A live "story depth" down the right edge, from 0 m to 4,000 m. The depths belong to the story; they are not measurements.
- **Back-to-surface button.** A closing section says thank you and returns the visitor to the top.
- **Layered sound (opt-in).** A sunlit score that gives way to an eerie deep score, two ambience loops and one-shot effects. Sound starts only when the visitor chooses it.
- **Reduced motion.** Three still views replace the animation, and the gate opens right away.
- **Works offline.** Falls back to native scroll progress when the GSAP CDN scripts are unavailable.

## Built with

- HTML, CSS and JavaScript (no build step)
- [GSAP](https://gsap.com/) and ScrollTrigger (loaded from a CDN)
- Canvas frame playback
- HTML Audio elements for the sound layers

## My role

<!-- TODO: Yuki, please check and edit this list. -->

- Concept and story
- Storyboard
- Art direction
- Scroll and animation code: GSAP ScrollTrigger, canvas frame playback
- UI: entry gate, chapter links, depth gauge, back-to-surface button
- Accessibility: reduced motion, opt-in sound

## Process

- [Storyboard](docs/storyboard.md): the intended shots, from the mask to the fin.
- [Production notes](docs/production-notes.md): prompts, timings, continuity rules and sound design.
- [Intro art prompts](docs/intro-art-prompts.md): visual and scroll decisions for the diving-mask intro.
- [Research and making (PDF)](docs/Lets-Dive-research-and-making.pdf): the illustrated research book.
- [Magnific ScrollWorld skill](.agents/skills/magnific-scrollworld/SKILL.md): the workflow notes used to review and produce shark transitions.

## Run locally

No build step, no Python.

1. Clone the repository.
2. Open `index.html` in a browser, or use the VS Code Live Server extension.
3. Scroll down and back up.

Where to look:

- `index.html`: scene layers and page chrome
- `css/style.css`: appearance
- `js/app.js`: scroll timing, animation frames, optional sound
- `js/site.js`: entry gate, chapter links, depth gauge, back-to-surface button
- `assets/`: images, video, frames and audio

If the project sits in an iCloud-synced folder (Desktop, Documents), macOS can create duplicate copies such as `frame-001 2.jpg`. They are not used by the page and `.gitignore` keeps them out of commits. They are safe to delete.

## Credits & licences

**My own work**

- Concept, story and storyboard
- Art direction and prompt writing
- All code in `index.html`, `css/` and `js/`
- Editing, sequencing and integration of all assets

**AI-generated assets**

- **Illustrations and key art:** made with the built-in image tool in Codex (OpenAI).
- **Video clips and sound effects:** made with Magnific. Some clips were produced with a Seedance continuation. <!-- TODO: confirm which clips were made in Magnific and which were made by you outside it. -->
- **Music (2 tracks) and sound effects:** generated with ElevenLabs (Music v2 and Text to Sound v2) through Magnific's Music Generator and Sound Effect Generator.

**Music usage restrictions**

- Magnific's terms say generated music may not be shared on music streaming platforms (Spotify, Apple Music and similar). Other restrictions on outputs and inputs also apply.
- This site uses the music only as its own background score.
- Read Magnific's AI Products Terms and ElevenLabs' terms before using the tracks anywhere else.

**Libraries**

- GSAP and ScrollTrigger, used under GSAP's own licence.

**Licence**

- The code (`index.html`, `css/`, `js/`) is released under the [MIT licence](LICENSE).
- The MIT licence does **not** cover the art, video, frames or audio in `assets/` or `docs/`. Those are AI-generated or third-party-restricted (see above) and are not licensed for reuse.
