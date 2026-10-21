# Field Ops — Construction Works

A standalone, browser-based 3D construction simulator built for touch screens and desktop.

## Current playable foundation

- Three-dimensional site with roads, terrain, trees, a marked foundation work zone, and a follow camera.
- Three selectable machines: excavator, wheel loader, and dump truck.
- Touch-friendly drive controls and contract-specific work actions.
- A four-stage starter contract chain: excavate the foundation, haul spoil, spread gravel, and place concrete.
- Site visuals change as work is completed; cash, rank, rewards, and contract progress update during play.
- Built with Three.js 0.160.0 from a browser ES module. No build step is required.

## Run it

Open `index.html` through a static web server or GitHub Pages. Because it imports Three.js as an ES module, opening the file directly from a local filesystem may not work in every browser.

## Controls

- Direction pad: drive and turn the current machine.
- **Machine**: cycle between the available machines.
- **Perform Work**: advance the active contract when using the required machine and close enough to the work zone.
- **Contracts / Pause**: review the contract chain and return to the site.

## Project direction

This is a separate new-work branch, not a replacement for the existing BuildWorks / Chatdemo project. The goal is a less repetitive construction game with varied contracts, persistent site changes, realistic machine interactions, multiple sites, progression, and phone-friendly controls.

## Current build limitations

This is an early playable foundation, not a finished simulator. Machine physics, true material loading/transport, save persistence, richer terrain deformation, audio, and multiple fully playable sites remain planned work. The current work button advances task stages with visible site changes; it does not yet simulate full excavation or vehicle physics.

## Deployment

The repository includes a GitHub Actions workflow for GitHub Pages. After Pages is enabled for this repository with **GitHub Actions** as its build/deployment source, pushes to `main` or `field-ops-foundation` can publish the site.
