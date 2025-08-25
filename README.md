# AI Summariser - Chrome Extension

## Overview

An intuitive Chrome extension that harnesses built-in AI to summarize highlighted text on web pages quickly and efficiently.

## Features

- **Easy Summaries**: Summarize any selected text with a single right-click.  
- **Built with AI**: Powered by Chrome's built-in [Summarizer API (Gemini Nano)](https://developer.chrome.com/docs/ai/summarizer-api) for fast in-browser summarization.  
- **Multiple Formats**: Support for key-points, TL;DR, teaser, or headline formats ([Summarizer API Docs](https://developer.chrome.com/docs/ai/summarizer-api)).  
- **Real-Time Feedback**: Create and analyze real-time Grafana dashboards (if extended for analytics) and monitor progress using streaming vs batch summarization modes ([Chrome AI Documentation](https://developer.chrome.com/docs/ai)).


## Installation and Set Up

1. Clone the repository:

   ```bash
   git clone 
   ```

2. Open Chrome and navigate to `chrome://extensions/`.

3. Enable **Developer mode** (toggle in the top-right corner).

4. Click **"Load unpacked"** and select the project folder.

5. The extension should now appear in your Chrome toolbar or context menu.

6. Now the extension opens as side panel and can be used to display the AI-generated summary (key points, TL;DR, etc.).


## How It Works

* **`manifest.json`**: Defines the extension's metadata, required permissions (e.g., `contextMenus`, `sidePanel`, `storage`), and side panel setup.
* **Background Service Worker**: Registers the "Summarize" context menu item, stores selected text, and triggers the side panel UI on command.
* **Side Panel UI**: A lightweight HTML panel that displays "Select text…", then invokes AI summarization once context is passed.
* **Summarization Logic**: Uses Chrome's Summarizer API to fetch a summary based on options like format and length, then renders it in the UI.

## References

* Chrome’s Summarizer API documentation on using Gemini Nano for various summary types and formats ([Amit Merchant Blog][1], [Chrome for Developers][2])
* Summary types: key-points, TL;DR, teaser, headline ([Amit Merchant Blog][1], [Chrome for Developers][2])
[1]: https://www.amitmerchant.com/chrome-ai-summarizer/?utm_source=chatgpt.com "Chrome now has an AI Summarizer API built right in - Amit Merchant"
[2]: https://developer.chrome.com/docs/ai/summarizer-api?utm_source=chatgpt.com "Summarize with built-in AI | AI on Chrome - Chrome for Developers"
