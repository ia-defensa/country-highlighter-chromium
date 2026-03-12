# IA Defensa Country Highlighter

A Chromium browser extension that highlights people and organizations as well as content from and about specific countries on social media platforms.

🔒 This extension saves no data. The source code is available for auditing. The extension is free for personal use—for commercial use, [purchase a license](https://payhip.com/iadefensa). Priority support and custom options available.

## Features

* **All countries included:** Pre-configured with all countries
* **Multi-language support:** Detects country names in English, German, French, Spanish, and other languages (more translations welcome)
* **Flag detection:** Automatically recognizes country flag emoji (🇩🇪, 🇺🇸, etc.)
* **Configurable highlighting:** Choose from three highlight levels:
  - **Subtle:** Underline matched terms
  - **Normal:** Yellow background on matched text (screen readers: polite announcement)
  - **Assertive:** Yellow background and page border (screen readers: assertive announcement)
* **Platform support:** Works on Twitter/X, Instagram, Facebook, LinkedIn, GitHub, Bluesky, and many Mastodon instances
* **Performance optimized:** Uses MutationObserver with debouncing for efficient dynamic content scanning

## Installation

1. [**Go to the IA Defensa Country Highlighter page**](https://chromewebstore.google.com/detail/ia-defensa-country-highli/jjhldkllehdfgipblabnojkpfoohcogi) in the Chrome Web Store
2. **Click “Add to Chrome”** (or equivalent for other Chromium browsers)

### Locally

1. **Download** or clone this repository
2. **Open Chrome** and navigate to `chrome://extensions/` (or equivalent in other Chromium browsers, like `edge://extensions/` or `vivaldi://extensions/`)
3. **Enable developer mode** (top right toggle)
4. **Click “Load unpacked”** and select the extension directory

Afterwards, configure the extension according to your preferences and consider pinning it to your toolbar for easy access.

Tip: Enable the extension in private mode (“Allow in Incognito”). The extension does not share any information with IA Defensa or third parties.

## Usage

### Quick Start

1. Click the extension icon in your toolbar
2. Ensure the toggle is enabled
3. Click “Open settings” to configure

### Configuration

**Options page** (right-click icon → “Options”):

* **Enable/disable extension:** Master on/off switch
* **Highlight style:** Choose subtle, normal, or assertive highlighting
* **Countries:** Select which countries to highlight (all enabled by default)
* **Platforms:** Choose which social media platforms to monitor

### Default Settings

* All countries enabled
* All platforms enabled
* Normal highlighting (yellow background)
* Extension enabled

## How It Works

1. Primary matching (fast): Scans for flag emoji first
2. Alias matching (thorough): Then checks for country names in multiple languages
3. Word boundary detection: Avoids false positives (e.g., “Germany” won’t match “many”)
4. Dynamic content: Monitors page changes with MutationObserver (300 ms debounce)
5. Performance: Only scans visible text nodes, skips scripts/styles

### Privacy

* No data collection: Extension operates entirely locally
* No network requests: All configuration files are bundled
* Chrome sync only: Settings synced via Chrome’s built-in sync (optional)

## Troubleshooting

**Highlighting not working:**

1. Check extension is enabled (click toolbar icon)
2. Verify current site is in platform list (“Options” → “Platforms”)
3. Ensure at least one country is selected (“Options” → “Countries”)
4. Try refreshing the page

**Performance issues:**

1. Reduce number of enabled countries
2. Switch to “subtle” highlighting mode
3. Disable on platforms you don’t use

**Settings not saving:**

1. Check Chrome/Edge sync is enabled
2. Try clearing extension storage (“Reset to defaults”)
3. Reload extension from `chrome://extensions/`

## Contributing

[Contributions are welcome.](CONTRIBUTING.md) They are subject to the [Contributor License Agreement](CLA.md).