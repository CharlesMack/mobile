# mobile
Mobile

P.O.P.S. (Professional Production Mobile) is a single-page, web-based mobile interface designed to streamline professional production workflows through a highly customizable, visually engaging, and touch-optimized platform. The interface mimics a mobile operating system, providing a home screen with app tiles, a dock for quick access, draggable and resizable app panels, an app switcher for multitasking, and a settings panel for theme customization.


P.O.P.S. — Professional Production Mobile
Overview
P.O.P.S. (Professional Production Mobile) is a sleek, single-page web application designed to streamline professional production workflows through a mobile-optimized interface. Built with HTML, CSS, and JavaScript, P.O.P.S. mimics a mobile operating system, offering a customizable home screen with app tiles, a dynamic dock, draggable and resizable app panels, an app switcher for multitasking, and a settings panel for theme personalization. It serves as a centralized hub for launching AppDrops, a collection of web-based tools tailored for media production, event planning, creative workflows, and more.
Hosted at http://charlesmack.github.io/mobile, P.O.P.S. provides a responsive, touch-friendly experience that runs in any modern browser, making it ideal for professionals working on the go in fields like film, music, events, or development.
Features

Home Screen Grid: Displays a customizable grid of AppDrop tiles, each with an emoji icon and name (e.g., Atlas 🌍, Charles5 M 🎬). Supports drag-and-drop reorganization in edit mode and alphabetical sorting.
AppDock: A fixed footer with quick-access icons for Home (🏠), Communications (📞), App Switcher (📱), and Settings (⚙️). Dynamically adds icons for open AppDrops.
AppDrop Panels: Draggable, resizable panels that load web-based AppDrops in iframes, with minimize, new tab, and close controls. Supports multitasking with multiple open panels.
App Switcher: A full-screen view to manage open apps, allowing users to switch between or close AppDrops.
Settings Panel: Customize the theme color using predefined swatches or a color picker, with changes persisting via localStorage. Includes a reset to default option.
Responsive Design: Optimized for mobile devices with safe-area insets, touch gestures, and a glassmorphic UI featuring gradients, glow effects, and animations.
AppDrops Catalog: Includes 33 production-focused apps, such as:
Media Production: Charles5 series, FiveSeconds Cine, Hearsay Cinema
Event Planning: Magifico Stage, Strobe HUD
Creative Tools: Dev Editor, DJ Drop, Scratchpad
Planning: Planner Gemini, Planner Lite
Emergency/Reference: First Aid, Survivors Compass
Communication: Tap Talk, Hearsay



Demo
Explore P.O.P.S. live at http://charlesmack.github.io/mobile.
Installation
P.O.P.S. is a web-based application that requires no installation for end users. To run or develop locally, follow these steps:
Prerequisites

A modern web browser (e.g., Chrome, Safari, Firefox).
A local web server (e.g., live-server, Python's http.server, or Node.js) for development to handle CORS and local testing.
Git for cloning the repository.

Steps

Clone the Repository:
git clone https://github.com/charlesmack/mobile.git
cd mobile


Serve the Application:

Using Node.js with live-server:npm install -g live-server
live-server


Using Python:python -m http.server 8000


Open your browser to http://localhost:8000 (or the port provided by your server).


Verify CORS for AppDrops:

AppDrops load from external URLs (e.g., https://charlesmack.github.io/OnePagerMiniOS/appdrops/...). Ensure these URLs are accessible and configured for CORS to load in iframes.



Usage

Launch P.O.P.S.:

Open the application in a browser via the live demo or local server.
The home screen displays a grid of AppDrop tiles.


Interact with AppDrops:

Tap a tile (e.g., DJ Drop 🎧) to open it in a draggable, resizable panel.
Use the dock or app switcher (📱) to navigate between open apps.
Minimize (–) or close (✕) panels, or open apps in a new tab (↗️).


Customize the Interface:

Enter edit mode by long-pressing a tile or right-clicking to drag and reorder apps.
Click "A→Z Sort" in edit mode to alphabetize tiles.
Open the Settings panel (⚙️) to change the theme color via swatches or the color picker. Click "Reset to Default" to revert to the green theme (#00ff7f).


Multitask:

Open multiple AppDrops and use the app switcher to switch between or close them.
Drag panels to reposition them on the screen.



Project Structure
mobile/
├── index.html       # Main HTML file with structure and JavaScript logic
├── README.md        # This file
└── (AppDrop assets) # External AppDrops hosted at https://charlesmack.github.io/OnePagerMiniOS/appdrops/


index.html: Contains the HTML, CSS, and JavaScript for the entire interface, including the home screen, dock, panels, app switcher, and settings.
CSS: Uses custom properties (--accent, --accent-light, etc.) for theming, with glassmorphic effects, animations, and responsive design.
JavaScript: Manages app launching, drag-and-drop, multitasking, and theme customization. Stores user preferences in localStorage.
AppDrops: External web apps loaded via iframes, hosted separately (e.g., https://charlesmack.github.io/OnePagerMiniOS/appdrops/).

Contributing
Contributions are welcome! To contribute to P.O.P.S., follow these steps:

Fork the Repository:

Click "Fork" on https://github.com/charlesmack/mobile.


Create a Branch:
git checkout -b feature/your-feature-name


Make Changes:

Add new AppDrops to the APPDROPS array in index.html.
Enhance UI/UX, add features (e.g., offline support, notifications), or fix bugs.
Ensure code follows the existing style (e.g., CSS custom properties, modular JavaScript).


Test Locally:

Verify changes work across browsers and devices.
Check CORS for any new AppDrop URLs.


Submit a Pull Request:

Push your branch and create a pull request with a clear description of changes.



Issues and Feedback
Report bugs or suggest features via the Issues tab. Include details like browser, device, and steps to reproduce for bugs.
Limitations

Internet Dependency: AppDrops require an internet connection. Offline support is not implemented (consider adding a Service Worker).
CORS: External AppDrop URLs must support CORS to load in iframes.
Accessibility: Limited keyboard navigation and ARIA support; enhancements are needed for screen readers.
Scalability: The grid may become crowded with many AppDrops; consider pagination or folders for future iterations.

Roadmap

Add offline support using Service Workers.
Implement notifications for AppDrop updates or alerts.
Enhance accessibility with ARIA labels and keyboard navigation.
Allow users to add custom AppDrops via a settings interface.
Optimize performance for low-end devices with metrics for iframe load times.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or collaboration, contact the maintainer via GitHub.


P.O.P.S. — Professional Production Mobile
P.O.P.S. (Professional Production Mobile) is a single-page, offline-first web interface designed for seamless, user-sovereign productivity on mobile devices. Built with a sleek, glassmorphic UI, it features draggable, resizable app panels, an AppDock for quick navigation, and an AppDrop catalog for extensible functionality. The system syncs with a command center to keep the AppDrop catalog up-to-date, ensuring a robust, production-ready environment for professionals.
The command center’s AppDrop catalog (/command/appdrops/index.html) serves as the central hub for discovering and syncing AppDrops, enabling users to expand their P.O.P.S. environment with new tools and applications.
Features

Offline-First Design: Works seamlessly without an internet connection, caching AppDrops and user preferences in localStorage.
User-Sovereign State: Persists app order, theme settings, and open panels across sessions.
Dynamic AppDrop Sync: Integrates with the command center to fetch and add new AppDrops when online, with real-time sync feedback.
Glassmorphic UI: Modern, visually appealing interface with draggable panels, animated tiles, and customizable themes.
AppDock & AppSwitcher: Quick access to core functions (Home, Communications, Settings) and multitasking with open apps.
Extensible AppDrop Catalog: Supports 33+ production-focused AppDrops, with easy integration of new apps via the command center.

Installation
Prerequisites

A GitHub account and repository access (e.g., charlesmack/OnePagerMiniOS).
GitHub Pages enabled for hosting the web interface.
A modern web browser (Chrome, Safari, Firefox, or Edge).

Setup

Clone the Repository:
git clone https://github.com/charlesmack/mobile.git
cd mobile


Verify Directory Structure:Ensure the following files are present:

index.html: The main P.O.P.S. interface.
command/appdrops/index.html: The command center’s AppDrop catalog.


Enable GitHub Pages:

Go to the repository’s Settings > Pages on GitHub.
Set the source to the main branch (or gh-pages if used).
Confirm the site is live at https://charlesmack.github.io/OnePagerMiniOS/ and the AppDrop catalog at https://charlesmack.github.io/command/appdrops/index.html.


Deploy Updates:

Make changes to index.html or command/appdrops/index.html.
Commit and push to the repository:git add .
git commit -m "Update P.O.P.S. interface and AppDrop catalog"
git push origin main





Usage

Access P.O.P.S.:

Open https://charlesmack.github.io/mobile/ in a web browser.
The home screen displays a grid of AppDrop tiles, each launchable into a resizable panel.


Navigate the Interface:

AppDock: Use the bottom dock to access:
🏠 Home: Return to the app grid.
📞 Communications: Launch communication apps (if available).
📱 App Switcher: View and manage open apps.
⚙️ Settings: Customize the theme and sync AppDrops.


Drag Tiles: Long-press a tile to enter edit mode and rearrange apps.
Open Apps: Tap a tile to launch an app in a draggable, resizable panel.
App Switcher: View open apps and close or switch between them.


Sync AppDrops:

Open the Settings panel (⚙️ icon).
Click Sync AppDrops when online to fetch the latest apps from https://charlesmack.github.io/command/appdrops/index.html.
Check the sync log for status updates (e.g., “Sync complete: 3 new AppDrops added”).
New apps appear in the home grid, persisted in localStorage for offline use.


Customize Theme:

In the Settings panel, select a predefined color swatch or use the color picker to set a custom theme.
Reset to the default color (#00ff7f) with the Reset to Default button.



AppDrop Catalog
The command center’s AppDrop catalog (/command/appdrops/index.html) lists all available AppDrops, including:

Atlas (🌍): Geospatial visualization tool.
Aurora (🌌): Creative design suite.
Bryce Holograms (😇): 3D holographic production app.
Camera Shop (🎥🏪): Camera equipment management.
Charles5 Series (🎬/📽️/🎥/🎞️/📺): Professional video production tools.
Dev Editor (💻): Code editor for developers.
DJ Drop (🎧): Audio mixing and DJ tools.
Encyclopedia (📚): Knowledge base and reference tool.
First Aid QuickRef (🩺): Quick-reference medical guide.
First Aid (🚑): Comprehensive first aid toolkit.
FiveSeconds Cine/Lite (🎬/🎥): Short-form video editing.
Hearsay/Cinema (🗣️/🎭): Audio and cinematic storytelling apps.
Magifico Room/Stage (🏠/🎤): Virtual room and stage production tools.
MPC Drop (🎮): Music production controller.
OnePagerMiniOS (💻): Mini OS interface.
Planner Gemini/Lite (📅/🗓️): Event and task planners.
POPS (🌟): Core P.O.P.S. app.
Retreat (🏕️): Wellness and productivity app.
Scratchpad (📝): Quick note-taking tool.
Strobe/HUD (✨/💡): Lighting control and HUD interfaces.
Survivors Compass (🧭): Navigation and survival guide.
Tap Talk (💬): Real-time communication tool.
Media World (🗺🕹): 3D media player and world explorer.
Viewria (👀): Visual media browser.

New AppDrops can be added to the catalog by updating command/appdrops/index.html with new <a> tags.
Contributing
We welcome contributions to enhance P.O.P.S. and its AppDrop ecosystem! To contribute:

Fork the Repository:
git clone https://github.com/charlesmack/mobile.git
cd mobile


Create a Branch:
git checkout -b feature/your-feature-name


Make Changes:

Add new AppDrops to command/appdrops/index.html with <a href="/path/to/appdrop/index.html">App Name</a>.
Enhance the P.O.P.S. interface (index.html) with new features or optimizations.
Ensure offline-first compatibility and localStorage persistence.


Test Locally:

Use a local server (e.g., npx serve) to test changes.
Verify sync functionality by pointing to a local or staged command/appdrops/index.html.


Submit a Pull Request:

Push your branch:git push origin feature/your-feature-name


Open a pull request on GitHub with a clear description of your changes.



Development Notes

Tech Stack: HTML, CSS, JavaScript (vanilla). No external frameworks for minimal footprint.
Offline Support: Uses localStorage for app state and AppDrop caching.
Sync Mechanism: Fetches AppDrops from command/appdrops/index.html when online, parsing <a> tags for app paths and names.
Design: Glassmorphic UI with customizable accent colors (default: #00ff7f).
Security: AppDrop iframes use sandbox attributes to restrict permissions.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or support, contact the maintainer at GitHub Issues or via the P.O.P.S. community on charlesmack.github.io.
