# Changelog

All notable changes to the iOS Homescreen project are documented here.

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
