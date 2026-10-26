<p align="center">
  <a href="https://www.mihirkavishwar.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset=".github/assets/banner-dark.png">
      <img alt="mihirkavi.github.io: old links, new home. Every mihirkavi.github.io link forwards to mihirkavishwar.com." src=".github/assets/banner-light.png" width="100%">
    </picture>
  </a>
</p>

<p align="center">
  <strong>Old links, new home.</strong><br>
  This GitHub Pages user site forwards every visitor to Mihir Kavishwar's portfolio, so old links and bookmarks keep working.
</p>

<p align="center">
  <a href="https://www.mihirkavishwar.com"><strong>Visit mihirkavishwar.com</strong></a> ·
  <a href="https://mihirkavi.github.io"><strong>Try the redirect</strong></a>
</p>

<p align="center">
  <img alt="Hosted on GitHub Pages" src="https://img.shields.io/badge/GitHub%20Pages-111111?style=flat-square">
  <img alt="Status: live" src="https://img.shields.io/badge/status-live-111111?style=flat-square">
  <img alt="Size: two HTML files" src="https://img.shields.io/badge/two%20HTML%20files-6b6b6b?style=flat-square">
</p>

## How it works

```text
mihirkavi.github.io/          ──►  index.html  ──►  www.mihirkavishwar.com/
mihirkavi.github.io/about     ──►  404.html    ──►  www.mihirkavishwar.com/about
mihirkavi.github.io/<repo>/   ──►  untouched: project Pages sites keep working
```

| File | What it does |
| --- | --- |
| `index.html` | Sends the root URL to `https://www.mihirkavishwar.com/` with an immediate meta refresh plus `location.replace`. |
| `404.html` | Catches every other path that has no file here and forwards it to the same path, query and hash on mihirkavishwar.com. |

No `CNAME` is set on purpose. A custom domain on the user site would also move project sites such as `mihirkavi.github.io/PixelRoot/` onto that domain, where they are not hosted.

## Honest status

- GitHub Pages cannot send HTTP 301 redirects, so these are client-side redirects. Browsers follow them immediately; some crawlers may not. Both pages are marked `noindex` with a canonical link to mihirkavishwar.com.
- Path forwarding needs JavaScript. Without it, the meta refresh in `404.html` sends visitors to the portfolio's home page instead of the matching path.
- The portfolio itself lives in a separate repository.

## License

No license file is included. This repository only contains redirect pages.

<p align="center">
  <br>
  <sub><strong>mihirkavi.github.io</strong> · Every link finds its way home.</sub>
</p>
