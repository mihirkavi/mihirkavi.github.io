# mihirkavi.github.io

Redirects the GitHub Pages user site `https://mihirkavi.github.io` to Mihir Kavishwar's portfolio at **[www.mihirkavishwar.com](https://www.mihirkavishwar.com)**, so old links and bookmarks still reach the current site.

## How it works

- `index.html` sends the root URL to `https://www.mihirkavishwar.com/` using an immediate meta refresh plus a JavaScript `location.replace`.
- `404.html` handles every other path that doesn't match a file here, forwarding it to the same path on mihirkavishwar.com (for example `/about` → `https://www.mihirkavishwar.com/about`).
- No `CNAME` is set on purpose. A custom domain on the user site would also move project sites such as `mihirkavi.github.io/PixelRoot/` onto that domain, where they are not hosted.

## Status and limitations

- GitHub Pages cannot send HTTP 301 redirects, so this uses client-side redirects. Browsers follow them immediately; some crawlers may not.
- Project Pages sites (`mihirkavi.github.io/<repo>/`) keep working and are not redirected.
- The portfolio itself lives in a separate repository.

## License

No license file is included. This repository only contains redirect pages.
