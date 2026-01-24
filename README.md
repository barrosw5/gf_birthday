# Birthday Celebration Web Application

A responsive, interactive web application designed as a time-sensitive digital gift. This project utilizes vanilla JavaScript, CSS3 animations, and SVG manipulation to render a countdown timer or a celebratory animation sequence depending on the current system date.

## Project Overview

The application operates on a dual-state logic system:

1.  **Countdown Mode:** If the current date does not match the target birth date, the application calculates the remaining days and displays a countdown interface.
2.  **Celebration Mode:** On the target date, the application renders a procedural flower garden animation, a celebratory message, and an interactive button that triggers an infinite-scrolling photo gallery.

## Key Features

* **Time-Sensitive Rendering:** Automatic state switching based on client-side system time.
* **Procedural Animation:** The flower garden is generated dynamically using JavaScript, creating unique variations in height, position, and sway angle for every session.
* **Responsive Design:** Mobile-first approach with distinct layouts for desktop (vertical split columns) and mobile (horizontal top banner).
* **Glassmorphism UI:** Utilizes CSS backdrop-filters and semi-transparent backgrounds for a modern aesthetic.
* **Infinite Marquee Gallery:** CSS-based infinite scrolling for image galleries, utilizing content duplication to ensure seamless looping.

## Technical Architecture

The project is built using a single-file architecture (`index.html`) containing the HTML structure, CSS styling, and JavaScript logic to ensure portability and ease of deployment.

### 1. State Management
The core logic resides in the `checkDate()` function. It compares `new Date()` with a hardcoded `birthDate` constant.
* **Logic:** Compares the current month and day against the target constants.
* **Output:** Triggers either `renderBirthdayMode()` or `renderCountdownMode()`.

### 2. Procedural Garden Generation
The `growGarden()` function dynamically injects DOM elements to create the background animation.
* **SVG Manipulation:** Utilizes SVG paths to draw tulip shapes.
* **Randomization:** `Math.random()` is used to determine horizontal position, stem height, rotation angle (simulating wind), and animation delays.

### 3. Infinite Scroll Gallery
The photo gallery uses a CSS-based marquee effect, distinct from standard slideshow libraries.
* **Implementation:** The `setupGalleries()` function duplicates the image array to ensure the scroll container is filled without visual gaps.
* **Animation:** CSS Keyframes (`@keyframes scrollUp`, `scrollDown`, `scrollLeft`) translate the container continuously.
* **Responsiveness:**
    * **Desktop:** Two vertical columns on the sides (one scrolling up, one scrolling down).
    * **Mobile:** A single horizontal row at the top scrolling left.

### 4. Styling and Animations
* **Fade Transitions:** CSS transitions are used for the `opacity` property to create a slow-fade effect (5 seconds) when revealing the gallery via the `slowFadeIn` keyframe.
* **Polaroid Effect:** Images are styled with varying borders and rotations to simulate physical photographs.
* **Variables:** CSS Variables (`:root`) are used for global color management.

## Configuration

To customize this project for a different recipient or date, modify the Settings section in the JavaScript block within `index.html`.

# Birthday Celebration Web Application

A responsive, interactive web application designed as a time-sensitive digital gift. This project utilizes vanilla JavaScript, CSS3 animations, and SVG manipulation to render a countdown timer or a celebratory animation sequence depending on the current system date.

## Project Overview

The application operates on a dual-state logic system:

1.  **Countdown Mode:** If the current date does not match the target birth date, the application calculates the remaining days and displays a countdown interface.
2.  **Celebration Mode:** On the target date, the application renders a procedural flower garden animation, a celebratory message, and an interactive button that triggers an infinite-scrolling photo gallery.

## Key Features

* **Time-Sensitive Rendering:** Automatic state switching based on client-side system time.
* **Procedural Animation:** The flower garden is generated dynamically using JavaScript, creating unique variations in height, position, and sway angle for every session.
* **Responsive Design:** Mobile-first approach with distinct layouts for desktop (vertical split columns) and mobile (horizontal top banner).
* **Glassmorphism UI:** Utilizes CSS backdrop-filters and semi-transparent backgrounds for a modern aesthetic.
* **Infinite Marquee Gallery:** CSS-based infinite scrolling for image galleries, utilizing content duplication to ensure seamless looping.

## Technical Architecture

The project is built using a single-file architecture (`index.html`) containing the HTML structure, CSS styling, and JavaScript logic to ensure portability and ease of deployment.

### 1. State Management
The core logic resides in the `checkDate()` function. It compares `new Date()` with a hardcoded `birthDate` constant.
* **Logic:** Compares the current month and day against the target constants.
* **Output:** Triggers either `renderBirthdayMode()` or `renderCountdownMode()`.

### 2. Procedural Garden Generation
The `growGarden()` function dynamically injects DOM elements to create the background animation.
* **SVG Manipulation:** Utilizes SVG paths to draw tulip shapes.
* **Randomization:** `Math.random()` is used to determine horizontal position, stem height, rotation angle (simulating wind), and animation delays.

### 3. Infinite Scroll Gallery
The photo gallery uses a CSS-based marquee effect, distinct from standard slideshow libraries.
* **Implementation:** The `setupGalleries()` function duplicates the image array to ensure the scroll container is filled without visual gaps.
* **Animation:** CSS Keyframes (`@keyframes scrollUp`, `scrollDown`, `scrollLeft`) translate the container continuously.
* **Responsiveness:**
    * **Desktop:** Two vertical columns on the sides (one scrolling up, one scrolling down).
    * **Mobile:** A single horizontal row at the top scrolling left.

### 4. Styling and Animations
* **Fade Transitions:** CSS transitions are used for the `opacity` property to create a slow-fade effect (5 seconds) when revealing the gallery via the `slowFadeIn` keyframe.
* **Polaroid Effect:** Images are styled with varying borders and rotations to simulate physical photographs.
* **Variables:** CSS Variables (`:root`) are used for global color management.

## Configuration

To customize this project for a different recipient or date, modify the Settings section in the JavaScript block within `index.html`.


## License

This project is open source and available under the [MIT License](LICENSE).
