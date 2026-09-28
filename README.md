# Flight Radar website

A single-page site for Flight Radar 4.0.3: the promo video, features, and a one-click
browser installer for the Waveshare ESP32-S3-Touch-LCD-7.

```
index.html          the page
style.css           styles
media/              promo video (MP4) and its poster image
shots/              screenshots from the board
firmware/           manifest.json + firmware image for the installer, and the download zip
```

## Try it on your computer

In this folder, run:

```
python -m http.server 8770
```

Then open http://localhost:8770 in Chrome or Edge. The installer works from localhost.

## Put it online

The installer needs the page to be served over **https**. Any static host works; the whole
folder is about 25 MB and every file is under 15 MB.

- **GitHub Pages:** create a repository, upload the contents of this folder, then
  Settings > Pages > Deploy from branch (main, root). The site appears at
  `https://<your-name>.github.io/<repository>/`.
- **Netlify Drop:** drag this folder onto https://app.netlify.com/drop.
- **Cloudflare Pages:** create a project and upload this folder.

## Updating the firmware

Replace the `.bin` in `firmware/`, update its file name and `version` in
`firmware/manifest.json`, and update the version shown in `index.html`.
