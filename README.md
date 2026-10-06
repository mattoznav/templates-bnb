# B&B template

"Alder House", a website for a small bed & breakfast built around a 3D tour of the house. As visitors scroll, the roof lifts off and the camera walks through the house room by room, with photos, amenities and prices next to each room and a "Book" button that leads to the property's existing booking system.

| Folder | What it is | Stack | Runs on |
| --- | --- | --- | --- |
| [`website`](website) | Public website with the scroll-driven 3D tour, and the Blender script that builds the model | Astro, React Three Fiber, GSAP, Blender | `localhost:4324` |

Live demo of the website: [mattoznav.github.io/templates-bnb-website](https://mattoznav.github.io/templates-bnb-website/), published from the website repository with GitHub Pages.

The folder is a Git submodule with its own repository and its own README with more detail. There is no backend and no booking engine: bookings go through the links set in the site settings.

## Requirements

| Tool | Version | Needed for |
| --- | --- | --- |
| Git | any recent version | cloning the template with its submodule |
| Node.js and npm | Node 22.12 or newer | `website` |
| Blender and Python 3 | Blender 5.2 or newer | only to change the house and rebuild the model |

## Install and run

```bash
git clone --recurse-submodules https://github.com/mattoznav/templates-bnb.git
cd templates-bnb/website
npm install
npm run dev
```

Open `http://localhost:4324`. If you cloned without `--recurse-submodules`, run `git submodule update --init --recursive` first.

## What it shows

- A 3D model built from code and dressed with CC0 furniture, plants, trees and PBR textures, so every room, window and piece of furniture can be changed and rebuilt.
- Lighting computed once in Blender and stored in textures, so the scene looks rendered but is cheap enough for phones.
- A tour driven by the scroll, with the camera easing into each room and the text and floor plan staying in sync.
- A page that still works without WebGL: the content is plain HTML and the room photos stand in for the 3D.
- A "Getting here" section with an illustrated map of the village and the route for each way of arriving.

Every name and place in the template is fictional.
