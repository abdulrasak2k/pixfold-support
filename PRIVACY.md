# Privacy Policy — PixFold

**Last updated: 7 November 2026**

## The short version

PixFold processes images locally and does not upload them or collect analytics. The right-click feature temporarily stores the selected image URL locally and requests that image from its original host.

## What PixFold does with your images

Every image you open is decoded, compressed and written back inside your own browser, using the browser's own built-in image encoders. There is no server, no account, no upload and no network request carrying image data — because there is no network code in the extension at all, other than the one case described below.

Images you add are held in memory for as long as the editor tab is open and are discarded when you close it or clear the queue. Nothing is written to disk unless you click Download, which saves the file where your browser normally saves downloads.

Re-encoding through the browser’s canvas removes source EXIF and GPS metadata. The browser may add output colour information. Orientation is applied to the pixels first so photos stay upright. Choosing “Keep original” downloads the original file unchanged, including any metadata.

Your colour theme preference is saved locally on this device. It is not transmitted.

## Data handled locally

PixFold handles images you choose and, for the right-click feature, the selected image URL. These correspond to website content and the selected resource URL (disclosed as web history in the store). This handling is limited to image editing and importing; PixFold does not monitor your browsing history. We do not receive or collect these images or URLs on our servers.

PixFold follows the Chrome Web Store User Data Policy, including its Limited Use requirements: this data is used only for the image-editing features you request, never for advertising, sale, unrelated purposes, creditworthiness or lending.

- No analytics, telemetry or crash reporting
- No cookies, accounts or identifiers
- No remote code: all scripts ship inside the extension and nothing is loaded from a CDN
- No advertising, and no sale or transfer of data to anyone

## Permissions, and why each exists

| Permission | Why it is needed |
|---|---|
| `contextMenus` | Adds the right-click entry "Compress this image with PixFold" |
| `storage` | Passes the address of a right-clicked image to the editor tab. The pending URL is removed when consumed by the editor. No image bytes or list of visited pages is stored |
| `<all_urls>` *(optional)* | Lets the editor fetch an image you explicitly right-clicked |

`<all_urls>` is **optional** and is **not** granted when you install PixFold. A fresh install has no access to any website. Chrome asks for it only if you use the right-click entry, and you can decline and keep using drag-and-drop, paste and the file picker. If you grant it, it is used for exactly one thing: fetching the single image you right-clicked. PixFold never reads page content, never injects scripts into pages, and never runs in the background on any site.

You can revoke it at any time at `chrome://extensions` → PixFold → Details → Site access.

When fetching a right-clicked image, its host receives a normal network request, including your IP address. No image is uploaded to PixFold or to a compression service. A pending image URL is removed when the editor consumes it; if the editor does not open successfully, it may remain in local extension storage until a later editor launch or extension removal.

## Children

PixFold collects no data from anyone, including children.

## Changes

Any change to this policy will be published with a new "last updated" date, and a version of the extension requiring new permissions will prompt you before it is installed.

## Contact

Questions about this policy: [abdurasak2k.projects@gmail.com](mailto:abdurasak2k.projects@gmail.com).
