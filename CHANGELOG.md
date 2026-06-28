# Changelog

All notable changes to the iOS Homescreen project are documented here.

## [1.3.1] - 2026-06-28
### Fixed
- **Mobile Page Swiping**: Added `touch-action: none` on the screen scroller container to prevent mobile browsers from intercepting drag gestures, enabling 100% fluid horizontal page changes.
- **Mobile Tap Highlight**: Disabled the browser-default blue highlight overlay on tap clicks via CSS `-webkit-tap-highlight-color: transparent`.

## [1.3.0] - 2026-06-28
### Added
- **Spotlight Search Overlay**: Pulling down on any grid page reveals a translucent, blurred Apple-style search box that filters apps in real-time.
- **App Library Swipe-Down to Search**: Swiping down from the top of the App Library scrollview automatically focuses the search input.
- **Organic Snap-Back Animations**: Invalid drag-and-drop actions animate the app icon gliding smoothly back to its source position.
- **Customizable Spotify Widget**: Replaced Battery+Music widgets with a wider Spotify iframe player widget (`344x152`) where users can customize the loaded playlist link.
- **XML RSS Google News Feed**: Fetches real-time headlines securely through the user's custom proxy server, parsing XML natively on the client.
- **Weather City Customizer**: Added location edit buttons to weather widgets to request and fetch real temperature updates dynamically.
- **Spring Entrance Animations**: Added keyframe slide-down springs for the edit control bar and bounce entries for buttons.

## [1.2.0] - 2026-06-28
### Added
- **iTunes Search API Integration**: In the "Add Web App" modal, searching will fetch matching App Store metadata and auto-fill app names and high-resolution icons.
- **File & Folder Webapp Compiler**: Added the ability to upload a single `.html` file or select a full local webapp directory (index.html + CSS/JS/images) which is compiled client-side into a standalone, single-file bundle.
- **Standalone Settings App**: Moved the Settings UI into a dedicated, clean `settings.html` file embedded as an iframe.
- **iOS Settings Layout Redesign**: Re-styled settings to look exactly like the iOS settings layout with dark mode, a "Guest" account card, "Ready for Apple Intelligence" callout, colored connectivity rows, and a sticky bottom search capsule.
- **Wallpaper Manager Library**: Built a wallpaper gallery inside settings allowing users to add custom wallpapers (URLs or file uploads) and delete them.
- **Export & Import Backup**: Added a backup feature to save/restore the entire configuration layout, custom wallpapers, and preferences.

### Changed
- **Dynamic Dock Spacing**: Removed hardcoded coordinates and replaced with a dynamic centering algorithm that keeps spacing uniform regardless of the number of apps in the dock.
- **App Icons Spacing**: Squeezed text margins (`margin-top` changed from `14px` to `6px`) to pull labels closer to their icons.
- **Dock Drag-and-Drop**: Users can now drag apps from the homescreen pages directly into the Dock container's empty space to append them or swap them with the closest icon.

## [1.1.0] - 2026-06-28
### Added
- **PC & Laptop Support**: Added right-click context menus for screen backgrounds and icons to allow laptop/desktop users to trigger edit modes.
- **Wiggle Mode (Edit Mode)**: Wiggling animation added to icons during edit mode with functional minus deletion badges.
- **Custom App Add Modal**: Implemented URL, Upload, and Emoji icon modes, alongside embed URL and Paste HTML options.
- **App Library Scrubbing**: Added A-Z scrubber track inside App Library with jump-on-drag scrolling logic.
- **Wallpaper Prompt**: Added option to change homescreen wallpaper via background context menu.

## [1.0.0] - 2026-06-28
### Added
- Initial project release with iOS springboard grid rendering.
- Widgets page (Page 0) layout.
- Slide/Swipe transition scrolling pages.
- Default settings app modal framework.
