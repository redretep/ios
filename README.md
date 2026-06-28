# iOS Homescreen Remake

A high-fidelity replica of the modern iOS Homescreen, built using vanilla HTML, CSS, and JavaScript.

## Features

- **iOS Springboard Grid**: Strict 4x6 layout grid with pixel-accurate safe area spacing, notch, status bar, page indicators, and bottom home indicator.
- **Interactive Widgets Page (Page 0)**: Displays weather, battery, music, and stocks widgets.
- **App Library (Last Page)**: Categorized folder quadrants, search filter with real-time A-Z scroll scrubber, and full-screen folder overlay views.
- **Wiggle Mode (Home Screen Edit)**: Long press or right-click to enter edit mode, allowing you to drag-and-drop apps to rearrange pages, set custom wallpaper backgrounds, and delete custom apps.
- **Custom Web Apps Modal**: Add new web apps using custom URLs, uploaded HTML files, or entire webapp folders (automatically compiled into standalone, self-contained documents).
- **iTunes Search API Integration**: Autocomplete app titles and search the official App Store to fetch high-resolution (`512x512`) icons.
- **Standalone Settings App**: A separate `settings.html` application styled after iOS Dark Mode, featuring:
  - Guest Profile Card
  - Airplane Mode & Connectivity Toggle
  - Custom Wallpaper Manager (supporting presets, URLs, and image uploads)
  - Full Backup Export & Import (JSON configuration format)
- **Dynamic Dock Alignment**: Dock apps are dynamically centered vertically and horizontally with uniform gap spacing. Supports dragging apps in and out of the dock.

## Architecture

- **`index.html`**: The main entry point rendering the physical phone viewport, home indicator bar, page-swiping transitions, and dynamically populated pages.
- **`settings.html`**: A standalone settings utility embedded via `iframe` inside the main launcher. Uses `postMessage` calls to coordinate system settings.
- **Data Persistence**: Uses `localStorage` to save all custom apps, layouts, dock state, custom wallpaper URLs/images, and system preferences.

## Getting Started

1. Open `index.html` directly in any modern browser or check it out live at [redretep.github.io/ios](https://redretep.github.io/ios)
2. Long-press on the homescreen background (or right-click) to trigger the context menu and edit/customization modes.
