# Cailin Osborne — Art & Design Portfolio

A static portfolio with a plaid introduction, an artwork gallery with looping animations, a For fun photo carousel, and an About page. This export matches the version completed October 21, 2026.

## Put it on GitHub

1. Create a repository (suggested name: `cailin-portfolio`).
2. Unzip this download. Upload the CONTENTS of the extracted folder to the repository, preserving the `assets` folder. `index.html` must be at the top level. Do not upload only the ZIP file.
3. Commit the files to `main`.
4. To host the website, open Settings → Pages. Under Build and deployment, choose Deploy from a branch, select `main` and `/(root)`, then Save.
5. GitHub will show the published URL in the Pages settings after deployment. Hosting with Pages makes the website publicly accessible; you can store the source without enabling Pages.

No install, build command, database service, or API key is required. GitHub Pages setup: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Which files to edit

- `projects.json`: homepage artwork, titles, descriptions, images, and order. Titles appear when an image is opened.
- `fun.json`: images and order in the For fun carousel.
- `index.html`: homepage introduction, navigation, and contact copy.
- `about.html`: About page text.
- `for-fun.html`: For fun page text.
- `style.css`: typography, colors, layouts, borders, and textures.
- `app.js`: gallery and artwork viewer behavior.
- `carousel.js`: carousel behavior.
- `assets/`: images, videos, paper texture, and font files.

`sketchbook.html` redirects to For fun. `sketches.json` and `sketchbook.js` are retained from the earlier draft but are not used on the current pages.

## Add a project

Upload a new image to `assets/`. Add an object to `projects.json`, separating entries with commas:

```json
{
  "id": "new-project",
  "title": "Your title",
  "category": "Illustration",
  "description": "Your project description.",
  "image": "assets/your-image.jpg",
  "alt": "Describe what the image shows."
}
```

For a looping motion project, also add `"video": "assets/your-animation.mp4"`. The image is its poster. Videos autoplay muted and loop, subject to visitors' browser settings. Reorder the JSON objects to rearrange the gallery. Keep animation entries apart if you want still artwork between them.

For carousel photos, use the same image record structure in `fun.json` without a video field. Use normal JSON: double quotes, no comments, and no trailing commas.

## Preview on your computer

Run `python3 -m http.server 8000` in this folder and open http://localhost:8000. Serve through a web server rather than double-clicking the HTML, because the galleries load JSON files.

## Typography and ownership

Montserrat and Dawning of a New Day are bundled, with their font licenses in `assets/`. Avenir is requested as a system font; visitors without it use a fallback. The current artwork titles and some descriptive text were draft editorial labels and can be replaced with your preferred wording.

Artwork and photographs remain the property of their respective owners. No broad open-source license for your artwork is included. The uploaded plaid is included as supplied; its original rights are not established by this export.

## Hosting and syncing

This is a standalone copy, not a connection between your GitHub account and the current ChatGPT-hosted site. Edits committed on GitHub will not automatically update the ChatGPT-hosted version, or vice versa. The portfolio records are editable JSON files, not a live database or website-based content editor.
