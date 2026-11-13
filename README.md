# Sam Howard – Portfolio

A single-page, static portfolio site for a videographer and photographer.
No build step, no dependencies, no JavaScript.

## Files
- `index.html` – the whole site (HTML + CSS in one file)

## Replace the placeholders
Each tonal green block is a placeholder (`<div class="frame ...">`).

Photo – swap the div for an image:
```html
<img class="frame a" src="images/photo-1.jpg" alt="Describe the photo" loading="lazy" style="object-fit:cover;width:100%;height:100%">
```

Film – embed a Vimeo or YouTube player inside a 16:9 frame:
```html
<div class="frame film"><iframe src="https://player.vimeo.com/video/YOUR_ID" style="position:absolute;inset:0;width:100%;height:100%;border:0" allow="fullscreen" title="Film title"></iframe></div>
```
Remove the `play` class from a film frame once it holds a real video.

## Deploy: GitHub + Cloudflare Pages
1. Create a GitHub repository and push this folder.
2. In Cloudflare: Workers & Pages > Create > Pages > Connect to Git, then pick the repository.
3. Framework preset: None. Build command: leave empty. Build output directory: `/`.
4. Save and deploy. The site is served over https automatically, and you can add a custom domain under Custom domains.
