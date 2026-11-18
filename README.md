# EM Tool — prototype

A prototype of EM Tool, the campaign thumbnail tool: Photopea-style layout editor, per-SKU editing with **Apply to…**, optional toolbox, rulers and guides, image upload, and export to JPEG / PNG / WebP (single file or ZIP).

It is one static page (`index.html`). There is no server and no build step. Everything runs in the browser, and work is saved in that browser only (Ctrl+S).

## Put it online with GitHub + Vercel

1. On GitHub, create a new repository called `em-tool`. Private is fine.
2. Click **Add file → Upload files**, drag in `index.html` and this `README.md`, and click **Commit changes**.
3. On vercel.com, sign in with GitHub, click **Add New… → Project**, and import the `em-tool` repository.
4. Leave every setting as it is (Framework Preset: **Other**, no build command) and click **Deploy**.
5. Vercel gives you a link like `em-tool.vercel.app`. Open it in Chrome or Edge.

To update it later, upload a new `index.html` to the repository; Vercel redeploys automatically.

## Notes

- Needs internet: it loads the Konva and JSZip libraries and the Inter font from public CDNs.
- Ctrl+T is kept by the browser, so free transform is **Ctrl+Alt+T**. Press **?** for every shortcut.
- The layout and products are sample data. This prototype has no PSD import and does not use your brand fonts yet.
