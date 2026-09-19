# Edit your project pages

Open `index.html` in your browser and click any project card. It opens a separate page in the same tab. **Back to projects** returns to the homepage. The pages also work on GitHub Pages without any extra setup.

## Which file to edit

| What you want to change | File |
| --- | --- |
| Homepage project summaries and links | `index.html` |
| Suspension project text and gallery | `projects/suspension.html` |
| Tire-analysis project text and gallery | `projects/tire-analysis.html` |
| Manufacturing project text and gallery | `projects/manufacturing.html` |
| Detail-page layout and card links | `assets/project-pages.css` |
| Images used by any page | `assets/images/` |

Open the project HTML file in your editor. Search for `OVERVIEW`, `YOUR CONTRIBUTION`, `ENGINEERING PROCESS`, or `GALLERY` to find the part you want to change. These labels are comments and do not show on the website. Save the file, then refresh your browser.

## Alternating image-and-text rows

After the project overview, each page has two rows: an image on the left beside **My contribution**, then an image on the right beside **Engineering process**. On phones, each image sits above its description. Additional rows automatically switch sides.

To change one of these images, open the project HTML file and search for `CONTRIBUTION IMAGE` or `PROCESS IMAGE`. Change the filename in both the nearby `href` and `src`, then update the `alt` description and the caption. The main image at the top and the gallery images have their own separate paths.

For the tire-analysis process image, search for `ROW IMAGE PLACEHOLDER`. Replace the entire `<div class="case-story-placeholder"> ... </div>` with:

```html
<a href="../assets/images/tire-comparison.png"
   target="_blank" rel="noopener"
   aria-label="Open tire comparison figure in a new tab">
  <img src="../assets/images/tire-comparison.png"
       alt="Describe the actual comparison shown in your plot"
       loading="lazy">
</a>
```

Save your real image as `assets/images/tire-comparison.png` first, or use your own filename in both places. Edit the existing `<figcaption>` below it to describe the image.

To add another alternating row, copy an entire `<section class="case-story-row"> ... </section>` **inside the `<div class="case-stories">`**, after the previous row. Replace its image and text. Give its heading a unique ID and use that same ID in the section's `aria-labelledby`. The row's position determines which side its image appears on; no CSS edits are needed.

## Add more text

Inside a `<div class="case-prose">`, add one paragraph at a time:

```html
<p>Write your project description here.</p>
<p>Write another paragraph here.</p>
```

Inside a contribution list, add another complete list item:

```html
<li>Describe another part of your contribution.</li>
```

Keep every opening and closing tag together. Add a new paragraph after `</p>`, not inside an existing paragraph. Write `&amp;` when you want to display an ampersand.

## Add a photo, CAD render, or analysis figure

1. Save your image in `assets/images/`. For example: `inboard-closeup.jpg`.
2. Open the relevant file in `projects/` and search for `GALLERY`.
3. Replace a complete placeholder `<div class="gallery-item gallery-placeholder"> ... </div>` with the figure below. Or paste it after another figure's closing `</figure>` and before the gallery's closing `</div>`.
4. Change the filename in **both** places, then update the alternative text and caption. Match the filename's capitalization exactly, including `.png` versus `.PNG`.

```html
<figure class="gallery-item">
  <a href="../assets/images/inboard-closeup.jpg"
     target="_blank" rel="noopener"
     aria-label="Open inboard actuation image in a new tab">
    <img src="../assets/images/inboard-closeup.jpg"
         alt="Describe the actual components visible in this image"
         loading="lazy">
  </a>
  <figcaption>
    <strong>Inboard actuation close-up</strong>
    Explain what this view shows and why it matters to your project.
  </figcaption>
</figure>
```

The gallery automatically lays out additional images. Images fit inside their boxes without being cropped. Clicking an image opens the original at full size.

**Why `../`?** These project pages are inside the `projects` folder. `../assets/images/` goes up one folder to find your images. Image paths in the homepage still start with `assets/images/`.

## Add a Results or Lessons learned section

Inside `<div class="case-sections container">`, after a complete `</section>`, add:

```html
<section class="case-section" aria-labelledby="results-title">
  <div>
    <p class="eyebrow">Results</p>
    <h2 id="results-title">Results &amp; lessons learned</h2>
  </div>
  <div class="case-prose">
    <p>Describe a result you measured or a design decision you made.</p>
    <p>Explain what you learned and what you would improve next.</p>
  </div>
</section>
```

Each heading ID must be unique on that page. If you add another section, give it a different ID and use the same value in its `aria-labelledby` attribute.

The starter descriptions use your existing project information. Add your actual constraints, methods, measured results, and lessons learned. No performance gains or numerical test results have been invented. The tire gallery has labeled spaces because additional analysis images have not been supplied yet.

## Add a completely new project later

1. Copy a file inside `projects/`, such as `suspension.html`, and rename the copy to `new-project.html`.
2. Replace the title, description, project facts, text, images, captions, and next-project link. Update the `<title>` and description tags near the top too.
3. In `index.html`, copy an entire `<article class="project" ...> ... </article>` inside the project grid. Give it a unique ID, replace its content, and set its `project-open` link to `projects/new-project.html`.
4. Keep exactly one link inside each homepage project card. That link already covers the card; extra nested links or expandable controls would conflict with it.

## When you choose to publish

Nothing was published by this update. When you upload these changes yourself, include the `projects` folder, the updated `index.html`, and `assets/project-pages.css`, along with the existing assets. Preserve the folder structure. See `README.md` for the GitHub Pages steps.
