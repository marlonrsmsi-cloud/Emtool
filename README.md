# EM Tool — prototype

A prototype of EM Tool, the campaign thumbnail tool: Home with campaigns and layouts, new campaigns from product photos or an Excel/CSV sheet, Photopea-style layout editor, per-SKU editing with **Apply to…**, optional toolbox, text options bar, AI background removal, rulers and guides, image upload, and export to JPEG / PNG / WebP (single file or ZIP).

It is a static site: `index.html` plus a `models` folder. There is no server and no build step. Everything runs in the browser and saves automatically in that browser (each person's browser keeps its own campaigns and layouts).

## Files

- `index.html` — the whole app
- `models/u2netp.onnx` — the AI model for **Remove background** (4.6 MB, Apache-2.0, see `models/NOTICE.md`)

## Put it online with GitHub + Vercel

1. On GitHub, open your `em-tool` repository (or create one; private is fine).
2. Click **Add file → Upload files**. Drag in `index.html`, `README.md` and the whole `models` folder (GitHub keeps the folder). Click **Commit changes**.
3. If the project isn't on Vercel yet: on vercel.com click **Add New… → Project**, import the repository, leave every setting as it is, and click **Deploy**. Project names must be lowercase, for example `em-tool-thumbnail`.
4. If it's already on Vercel, it redeploys by itself after the commit. Open your link after about a minute.

## Notes

- Needs internet: it loads Konva, JSZip, the ONNX runtime and web fonts from public CDNs.
- The first **Remove background** downloads the 4.6 MB model once; after that it's quick.
- Ctrl+T is kept by the browser, so free transform is **Ctrl+Alt+T**. Press **?** for every shortcut.
- The layout and products are sample data. No PSD import yet. Upload your brand fonts with **Upload font…** in the text bar; they're saved in that browser automatically (each teammate uploads their own copy).
