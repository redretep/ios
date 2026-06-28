# iOS Web Recreation (Look & Feel + Interaction)

A client-side web recreation designed to replicate the visual language, physics, and interactions of the iOS Homescreen. This project pairs HTML5 and CSS structures with native JavaScript to simulate app library, page navigation, and responsive touch/click actions. External applications can be embedded directly within the UI frame using standard iframe sandboxing.

## 📱 Features

* **Device Wrapper & Environment:** Simulates a physical iPhone chassis (393px × 852px) featuring a custom Dynamic Island overlay.
* **Apple Grid Engine:** A strict 4-column CSS layout matching native icon distribution.
* **Glassmorphic Dock:** A persistent bottom action area utilizing CSS backdrop-filters (`blur()`) over alpha-translucent panels.
* **JavaScript State Management:** Lightweight handlers managing core system events, layout tracking, and app opening/closing sequences.
* **Web App Embeds:** Uses secure, sandboxed embedding wrappers to load live web applications natively inside app views without disrupting the master interface shell.

## 🛠️ Design & Architecture System

| Element | Specification | Technical Approach |
| :--- | :--- | :--- |
| **Typography** | SF Pro / System Fallbacks | `font-family: -apple-system, ...` |
| **Icon Curve** | Continuous Corner Radius | `border-radius: 14px;` (approximated squircle) |
| **Grid Spacing** | 4-Column Layout | `grid-template-columns: repeat(4, 1fr);` |
| **Dock Blur** | Native Backdrop Translucency | `backdrop-filter: blur(30px);` |
| **App Handling** | Embedded Web Apps | Sandboxed `<iframe>` tags with isolated context |
| **Transitions** | Native App Opening Scaling | CSS custom transforms driven by JS state triggers |

## 🚀 Getting Started

Because this project relies entirely on browser-native runtime engines (HTML5, CSS3, and Vanilla JavaScript), running it locally is straightforward and requires no build steps or bundlers.

### Prerequisites

* Any modern web browser supporting standard ES6 Javascript and CSS backdrop filters (Safari, Chrome, Firefox, or Edge).
* A local text editor if you plan to append custom embeds.

### Installation & Deployment

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/redretep/ios.git](https://github.com/redretep/ios.git)
   cd ios

```

2. **Launch the interface:**
Double-click the `index.html` file to view it directly via the `file://` protocol, or boot up a lightweight local static file server to handle embedded frame contexts reliably:
```bash
# Quick launch via Python's built-in module
python3 -m http.server 8000

```


Once running, open your web browser and navigate to `http://localhost:8000`.

## ⚙️ How Embeds & Logic Work

### 1. App Launch Mechanics (JavaScript)

The DOM structure uses `data-app` targets or event listeners assigned to individual `.app-item` containers. When clicked, JavaScript toggles active viewport states, scaling down the home screen grid while animating the target application view into full scale from the source icon coordinates.

### 2. Sandbox Embedding Configuration

External web tools, retro games, or standalone web apps are mapped via `<iframe>` nodes. They are configured with targeted sandbox rules to optimize security while rendering within the system mock framework:

```html
<iframe src="[https://example-app.com](https://example-app.com)" sandbox="allow-scripts allow-same-origin"></iframe>

```

## 📄 License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE).
