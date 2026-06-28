# Homescreen

> Trying to recreate iOS on the web one screen/gesture/animation at a time

<img src="https://github.com/user-attachments/assets/b3ffb760-8fef-4c7e-8b8b-f620bb35a0d8" width="100%" alt="Homescreen">

## Introduction

This is an experiment, a work in progress. The goal is to try and recreate the look and feel of Apple iOS on the web. It is not meant to be a production ready application but rather a showcase of techniques demonstrating how close we can get to a native feeling app just using HTML, CSS and JavaScript.

The app is intentionally restricted to running as a standalone web app that is added to the home screen on iOS devices. It does not concern itself with being responsive or working in other browsing contexts.

The rationale here is to narrow the scope and allow us as designer/developers to first and foremost focus on creating native feeling UI without having to worry about the myriad of different screen sizes, browser capabilities or input types other than touch.

The biggest challenge I see here is replicating native feeling gestures and animations.

## Architecture

Currently the implemenation is built uses:

- [Preact](https://github.com/preactjs/preact) for routing, importing and rendering components
- [Twind](https://github.com/tw-in-js/twind) for styling static screen and injecting CSS for animations
- [Vite](https://github.com/vitejs/vite) for transpiling and building the app in development and production

Other than that it mostly dependency free i.e. no animation libraries. That said, I am not opposed to using libraries if they can help us achieve the desired look and feel.

## Inspiration

This project has been inspired by the following wonderful projects:

- MacOS Web by [Puru Vijay](https://github.com/PuruVJ) – [App](macos-web.app) and [Repo](https://github.com/puruvj/macos-web)
- WhatPWACanDo by [Danny Moerkerke](https://github.com/DannyMoerkerke) – [App](https://whatpwacando.today/) and [Repo](https://github.com/DannyMoerkerke/whatpwacando.today)

## Getting Started

To get started with running the app locally:

1. Run `git clone https://github.com/lukejacksonn/homescreen.git` to clone the repository
2. Run `npm install` to install the dependencies
3. Run `npm start` to start the development server

You can then open the development server in a web browser and the app should appear wrapped in a faux iOS device. Alternatively you can install the [Homescreen VSCode Extension](https://marketplace.visualstudio.com/items?itemName=lukejacksonn.homescreen) and open the app there (requires https which the dever server is configured to use by default).

## Contributing

Obviously trying to recreate iOS is a massive undertaking. I have started with the Springboard and a few apps. I am not particularly precious about any of the existing implementations (a lot of this was just experimenting) and would welcome any improvements or additions.

The current state of the project is as follows:

### Springboard

- Widget screen: Currently just screenshots of widgets
- App grid screens: Swipe gesture and blur/scale on end screens
- App library screens: List apps and animated search input
- App launching: Launch and close animation with persisted app state

### Apps

- ⌚️ Clock: Mostly static screens with navbar
- 📷 Camera: Single static screen no functionality
- ⚙️ Settings: Single static screen no functionality
- 📱 App Store: Mostly static screens with navbar
- 🧮 Calculator: Single static screen no functionality
- 🖼️ Photos: Mostly static screens with navbar

### Components

- Device: A wrapper for the entire app that ensures a fullscreen device context
- Screen: Wraps the content of a screen and handles padding and gutters
- Launcher: Handles launching and closing animation of apps
- Popover: Handles the overlaying of a bottom drawer

Contribute to this project by adding more apps or improving the existing ones. The goal is to make the app as close to the native iOS experience as possible and highlight reusable components and patterns that can be used in other applications.

## License

MIT
