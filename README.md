# Github Underline Nuker

A lightweight Chrome extension that automatically removes underlines from links on GitHub pages where `[data-a11y-link-underlines=true]` is present.

## Features

- Removes underlines from links on GitHub pages
- No UI, no popups — install and it just works
- Minimal permissions required

## Installation

1. Download or clone this repository
2. Open Chrome and navigate to `chrome://extensions/`
3. Enable "Developer mode" in the top right
4. Click "Load unpacked" and select the extension directory
5. The extension is now active on GitHub pages

## How It Works

The extension injects a small CSS snippet that overrides the `text-decoration: underline` style on elements that have the `data-a11y-link-underlines=true` attribute.

```css
[data-a11y-link-underlines="true"] a,
[data-a11y-link-underlines="true"] a:hover {
  text-decoration: none !important;
}
```

## Permissions

- **activeTab**: To apply the CSS only to the current tab

There is no tracking, analytics, or background scripts in this extension.
