# Portfolio Website Enhancement Walkthrough

The portfolio website for **Priyal Viroja** has been fully updated and enhanced. Below is a detailed summary of the bugs fixed, design upgrades applied, and validation results.

## 🛠️ Critical Bugs Fixed

### HTML Structure (`index.html`)
- **Fixed Malformed URLs:** Corrected corrupted Google Font link targets.
- **Fixed Tag Casing & Standard Syntax:** Standardized tags to lowercase and resolved classes with invalid bracket syntax (`class=" hero-title]"`).
- **Corrected Asset Paths:** Updated logo image path to match the correct case-sensitive folder (`image/logo.png`).
- **Fixed Broken URLs:** Resolved the malformed blog link (`https:// priyalviroja.in`).
- **Removed Shell Artifacts:** Removed trailing `'EOF' > ...` shell commands left at the bottom of the file.

### Stylesheet (`css/modern.css`)
- **Resolved Selector Syntax Errors:** Removed markdown-style asterisks (`**`), leading hyphens (`-`), and trailing brackets in selectors/values.
- **Restructured Classes:** Synced navbar selectors to match the corrected HTML elements.

### JavaScript Engines
- **Cleaned Corrupted Code:** Fixed corrupted arrow functions, stray parenthesis, and invalid timeout declarations in the animation script.
- **Removed Unused/Broken Libraries:** Replaced the broken `Ticker` class and legacy `jquery.lettering.min.js` + `jQuery 1.11` with lightweight, modern, error-free vanilla JS.

---

## 🎨 Immersive Hacker Aesthetics & Dramatic Features

### 1. Matrix Digital Rain Canvas Background
- Built a native HTML5 `<canvas>` matrix code rain engine. Fading green streams of Japanese Katakana and numbers trickle down behind content at `0.05` opacity to create a deep, moving visual texture without distracting from text readability.

### 2. CRT Screen FX (Toggleable)
- **Overlay:** Implemented a full-viewport scanline texture overlay (`.crt-overlay`) and a screen distortion gradient wrapper.
- **Flicker Simulation:** Programmed a subtle, high-frequency phosphorus brightness flicker animation (`.crt-flicker`) running on keyframes.
- **Interactive Toggle:** Added a `[CRT_FX]` interactive button in the navbar, allowing users to toggle the CRT monitor scanlines effect on/off dynamically.

### 3. Text Glitch & Decrypt Effects
- **CSS Text Glitch:** Created hover-triggered clip-path glitch animations on the hero title, reproducing red/cyan horizontal line offset anomalies. Updated pseudo-element backgrounds to `transparent` to avoid overlay clipping the canvas digital rain.
- **Javascript Decrypt Script:** Built a real-time character scrambler script that simulates decryption when hovering over skill cards or on page load. Optimized the script to trim original content values to ensure character math remains accurate.

### 4. Direct Console Access / Interactive Terminal
- Designed a fully functional interactive terminal widget simulating real cybersecurity workflows:
  - **`scan_network`**: Simulates port checking (`80`, `443`, `8080`) and directory traversal alerts on target.
  - **`run_payload_test`**: Runs a mock proof-of-concept DOM injection and opens a root prompt.
  - **`view_pgp_key`**: Prints your PGP public block directly into the window console box.
  - **`clear_console`**: Clears terminal history and prints the initial handshake.

---

## 🔍 Validation Results

### Dev Server Running
- Started local server on port `8080` to verify changes.
- Tested server health:
  ```bash
  curl -I http://localhost:8080
  # Returns: HTTP/1.0 200 OK
  ```
- Checked HTML formatting and styles via local compilation. All syntax validation checks are clean and console errors have been eliminated.
