# Banner source

`banner.html` is the self-contained source of `../banner-light.png` and `../banner-dark.png`. One file holds both themes; the dark theme is a `prefers-color-scheme: dark` media query. It loads Inter and JetBrains Mono from Google Fonts and uses the system Georgia.

Re-render with headless Chromium at a 1600 × 520 viewport and a device scale factor of 2, once with the light and once with the dark color scheme. With Playwright:

```js
const page = await browser.newPage({ viewport: { width: 1600, height: 520 }, deviceScaleFactor: 2, colorScheme: 'dark' });
await page.goto('file://' + path.resolve('.github/assets/source/banner.html'));
await page.evaluate(() => document.fonts.ready);
await page.screenshot({ path: '.github/assets/banner-dark.png' });
```

Notes for agents: keep this banner in step with the portfolio's identity (mihirkavi/Portfolio, `.github/assets/source/banner.html`), and keep the URLs in it true to what `index.html` and `404.html` do.
