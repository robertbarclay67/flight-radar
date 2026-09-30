# Flight Radar website

The Flight Radar site: the display firmware page (promo video, features and a one-click
browser installer for the Waveshare ESP32-S3-Touch-LCD-7, firmware 4.0.5), and pages for the
Android and Windows apps (1.0.4).

```
index.html          the display page
android.html        the Android app page (tip jar, no affiliate links)
windows.html        the Windows app page (tip jar, no affiliate links)
style.css           styles for all three
media/              videos (MP4) and their posters, tip-jar QR codes
shots/              screenshots from the board
apps/               screenshots of the apps
download/           the Android APK and the Windows zip
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
folder is about 105 MB and every file is under 25 MB (GitHub's limit is 100 MB per file).

- **GitHub Pages:** create a repository, upload the contents of this folder, then
  Settings > Pages > Deploy from branch (main, root). The site appears at
  `https://<your-name>.github.io/<repository>/`.
- **Netlify Drop:** drag this folder onto https://app.netlify.com/drop.
- **Cloudflare Pages:** create a project and upload this folder.

## Updating the firmware

Replace the `.bin` in `firmware/`, update its file name and `version` in
`firmware/manifest.json`, and update the version shown in `index.html`.

## Updating the apps

Put the new APK and zip in `download/` (versioned names), delete the old ones, and update
the version and download links in `android.html` and `windows.html`.
