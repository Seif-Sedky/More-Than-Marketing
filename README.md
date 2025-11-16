# MTM Static Website - Technical README

This repository contains the source code for a static, two-page marketing portfolio website. The project is built with HTML5, CSS3, and vanilla JavaScript for animations.

## Technical Stack

* **HTML5**: Used for page structure.
* **CSS3**: Used for all styling and layout. Styles are not shared between `index.html` and `our_work.html`.
* **Vanilla JavaScript (ES6+)**: Used inline via `<script>` tags for DOM manipulation.
* **Intersection Observer API**: Implemented in JavaScript to trigger CSS animations when elements enter the viewport.

## Project Structure
.
├── index.html
├── our_work.html
│
├── css/
│   ├── style.css           (Used by index.html)
│   └── our_work_style.css  (Used by our_work.html)
│
└── assets/
    └── images/
        ├── logo.png
        ├── founders.jpg
        ├── noja-1.png
        ├── cozeta-sleeve.jpg
        ├── widan-1.png
        ├── tv-frame.png
        ├── carousel-1.png
        ├── phone-frame.png
        ├── phone-1.mp4
        └── (all other .png, .jpg, and .mp4 files...)

## Page Overviews & Features

### `index.html` (Home Page)

* **Navigation**: Standard `nav` element with links to page sections and the `our_work.html` file.
* **Layout**: Composed of multiple `<section>` blocks (e.g., `.hero-section`, `.about-section`, `.services-section`).
* **Components**:
    * Services Grid: A CSS grid displaying services.
    * Process Timeline: A 4-step horizontal timeline visualization.
    * Footer: Contains `tel:` and `mailto:` links, plus an external link to Instagram.
* **Script**: An inline script uses `IntersectionObserver` to add a `.is-visible` class to sections as they are scrolled into view.

### `our_work.html` (Our Work Page)

* **Layout**: A vertical stack of project sections, each with the `.project-section` class.
* **Components**:
    * **Fashion Uchaf Project**: Implements a CSS-animated carousel.
        * An image carousel (`.carousel-track`) animates vertically within a container (`.tv-screen`).
        * The container is positioned absolutely on top of a TV frame image (`.tv-frame`).
        * Duplicate images are used at the end of the carousel to ensure a seamless loop.
    * **Social Media / Story Projects**:
        * Uses `<video>` elements with `autoplay`, `muted`, `loop`, and `playsinline` attributes.
        * Videos are placed inside a `.phone-screen` container, which is positioned on top of a phone frame image (`.phone-frame`).
* **Script**: An inline script uses `IntersectionObserver` to add a `.is-visible` class to elements with a `[data-animation]` attribute. It also supports a `[data-delay]` attribute to stagger animations.

## Local Setup

1.  Clone the repository.
2.  No build process or dependencies are required.
3.  Open `index.html` in any modern web browser.
    * **Note**: Running via a local server (like the VS Code "Live Server" extension) is recommended to ensure all file paths resolve correctly.
