# Open in Browser

A lightweight **Open in Browser / Open in App-style landing page** for links shared through in-app browsers such as Instagram, Facebook, or other social apps.

When a visitor opens a link inside an in-app browser, this page explains that the destination works best in a full browser and provides a button that attempts to open the destination in **Google Chrome on Android**.

> This is a browser handoff page, not a way to force every app or device to open an external browser. In-app browsers and operating systems control whether the handoff is allowed.

## How it works

1. A visitor opens this landing page from an in-app browser.
2. The page displays a simple prompt to continue in a browser.
3. Tapping **Open in Browser** launches an Android Chrome intent for the configured destination URL.
4. If the app or browser blocks the intent, the visitor may need to use the app's menu and choose **Open in browser** manually.

## Configure the destination

Open `index.html` and change the URL inside `openBrowser()`:

```js
const url = "https://your-destination.example/";
```

Use the complete URL, including `https://`. This destination is where the visitor should continue after tapping the button.

## Run locally

No build tools or dependencies are required.

- Open `index.html` directly in a browser, or
- Serve the folder using any static web server.

## Deploy

Deploy this repository as a static site using Vercel, Netlify, GitHub Pages, or another static hosting provider. No environment variables or backend are required.

After deployment, share the landing-page URL instead of the destination URL when you want visitors to see the browser handoff prompt first.

## Compatibility and limitations

- **Android:** Uses an Android intent targeting Google Chrome.
- **iPhone/iPad:** This implementation does not currently provide an iOS-specific browser handoff. Users may need to open the in-app browser menu and select an external browser.
- **Other browsers:** Intent handling varies by app and browser.
- **No forced redirect:** A website cannot guarantee that every app opens Chrome or another external browser. A manual fallback is important.
- **Privacy:** The page has no analytics, database, or tracking code by default.

## Tech stack

- HTML
- CSS
- Vanilla JavaScript

## Project structure

```text
frontend-experiment/
├── index.html   # Landing page, styling, and browser handoff logic
└── README.md    # Project documentation
```

## Author

**Mayank Yadav**

- Email: [rao.mynkk@gmail.com](mailto:rao.mynkk@gmail.com)
- GitHub: [@MayanKiz](https://github.com/MayanKiz)
- LinkedIn: [Mayank Yadav](https://www.linkedin.com/in/mayank-yadav-2803202a5/)

Suggestions, bug reports, and collaboration ideas are welcome.