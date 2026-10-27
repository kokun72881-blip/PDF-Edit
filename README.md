# PDF Utility V6.5 True Offline Edition

Open `PDF_Utility_V6_5.html` from this folder. The page does not use a network connection. Copy the whole folder to a hard disk or USB drive and open the file there.

## Folder

```
PDF_Utility_V6_5.html
libs/pdf-lib.min.js
libs/fontkit.umd.min.js
libs/pdf.min.js
libs/pdf.worker.min.js
libs/xlsx.full.min.js
fonts/NotoSansTC-Regular.ttf
fonts/NotoSansTC-Regular.js
```

Keep these names and this layout. The page loads the scripts in `libs` and the font in `fonts` by relative path.

## Libraries

| File | Role |
| --- | --- |
| `libs/pdf-lib.min.js` | Split, merge, and PDF export |
| `libs/fontkit.umd.min.js` | Embeds Noto Sans TC so exported words stay real PDF text |
| `libs/pdf.min.js` | Preview, JPG, and reading PDF text for Excel |
| `libs/pdf.worker.min.js` | pdf.js worker. On a normal file open the page uses it in-page if the browser blocks a worker thread |
| `libs/xlsx.full.min.js` | Excel export, including Valuation Reconstruction |

## Font

| File | Role |
| --- | --- |
| `fonts/NotoSansTC-Regular.ttf` | Noto Sans TC Regular. On-screen text uses this file. It is the official Traditional Chinese subset (OpenType outlines) stored under this name so the page can find it |
| `fonts/NotoSansTC-Regular.js` | Same font, packed so a `file://` page can embed it. Browsers block reading the `.ttf` bytes directly from a file address |

When the font loads, export uses **Embedded Font Mode**: the words are real PDF text, so they can be searched and copied. When it cannot load, export uses **Compatibility Mode** and draws the same words as placed images. Export still completes.

## Check

Open the page and click **Run Offline Diagnostics**. A complete folder reports:

- Offline Mode Active
- pdf-lib Loaded
- pdf.js Loaded
- xlsx Loaded
- Worker Loaded
- Embedded Font Mode

## Tools

Split, Merge, Add Text, JPG, and Excel Valuation Reconstruction. Add Text still places words on the preview, and you drag, edit, rotate, and delete them there.
