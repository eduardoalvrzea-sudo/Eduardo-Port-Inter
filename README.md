# Eduardo Alvarez — Mechanical Engineering Portfolio

A complete, responsive portfolio based on the supplied Eduardo-Alvarez-Resume.pdf. It includes a full-width introduction, personal summary, alternating experience timeline, image-led Formula SAE project gallery, technical skills, education, contact links, and a downloadable copy of the résumé.

**Nothing has been uploaded or published.** Follow the GitHub steps below when you are ready to make it public.

## Open the site locally

Extract the ZIP, then double-click `index.html` inside `eduardo-portfolio`. It works directly in a browser without installation, JavaScript, a build process, or an internet connection. Email and LinkedIn links open external applications or sites.

## Files

```text
eduardo-portfolio/
├── index.html                  All portfolio text, links, and sections
├── assets/
│   ├── styles.css              Layout, colors, and responsive styles
│   ├── Eduardo-Alvarez-Resume.pdf
│   └── images/
│       ├── formula-sae-placeholder.svg
│       ├── suspension-placeholder.svg
│       ├── tire-analysis-placeholder.svg
│       └── manufacturing-placeholder.svg
├── .nojekyll                   Serves the site as plain static files
├── .gitignore
└── README.md
```

## Exact GitHub Pages deployment steps

These are actions for you to perform. Creating a public repository makes its uploaded files public; enabling Pages publishes the website. Use a new repository so that you do not overwrite an existing site.

1. Sign in to [GitHub](https://github.com), click **+** at the upper right, then **New repository**.
2. Enter **portfolio** as the repository name. Choose **Public** for GitHub Free. Turn **Add README** on, then click **Create repository**.
3. In the repository’s **Code** tab, choose **Add file → Upload files**.
4. Open the extracted `eduardo-portfolio` folder. Drag its **contents** into the upload area: `index.html`, `assets`, `README.md`, `.nojekyll`, and `.gitignore`. Upload the contents, not the enclosing folder or ZIP. Keep the `assets` folder structure intact.
5. Enter **Add mechanical engineering portfolio** as the commit message. Select **Commit directly to the main branch**, then click **Commit changes**.
6. Verify `index.html` and `.nojekyll` appear in the repository’s top-level file list alongside `assets`. If `.nojekyll` was omitted by your file picker, use **Add file → Create new file**, name it `.nojekyll`, enter one blank line, and commit it to `main`.
7. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
8. Under **Branch**, select **main** and **/ (root)**, then click **Save**. This is the step that enables website publishing.
9. Check the repository’s **Actions** tab for the Pages build/deployment to finish. Return to **Settings → Pages → Visit site**. Changes can take up to 10 minutes to appear.
10. Your address will be `https://YOUR-GITHUB-USERNAME.github.io/portfolio/`. Replace `YOUR-GITHUB-USERNAME` with your actual account username. Test the résumé, contact links, project details, and mobile layout.

For a homepage without `/portfolio/`, use a new repository named **YOUR-GITHUB-USERNAME.github.io** instead, with the exact account username. Its site address is `https://YOUR-GITHUB-USERNAME.github.io/`. Do not use this name if you already have a site in that repository unless you intend to replace it. All asset links in this project are relative, so either option works without code changes.

No custom workflow or build command is required. Keep Pages set to **Deploy from a branch**, not **GitHub Actions**.

### Update the published site

Edit the local files, then upload the changed files to the same paths and commit them to `main`. Once Pages is enabled, those commits automatically update the website. To edit a single file on GitHub, open it, use the pencil button, and commit the change.

### If the site does not load

- **404 at the site address:** Verify Pages uses `main` and `/ (root)`, and `index.html` is at the root, not inside another `eduardo-portfolio` folder.
- **Missing styling, résumé, or images:** Verify the `assets` folder was uploaded and capitalization matches the HTML exactly. GitHub paths are case-sensitive.
- **Old content:** Wait for the latest Pages deployment to finish, then refresh the browser without its cached files (Ctrl+Shift+R on Windows).
- **Pages setting unavailable:** Check that this is a public repository and that your account can administer it.

Instructions checked against [GitHub’s publishing-source guide](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site), [site creation guide](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site), and [Pages quickstart](https://docs.github.com/en/pages/quickstart).

## Add your project photos and CAD renders

The four image areas are deliberately labeled placeholders; none represents an actual vehicle, CAD model, or test result.

| Area | Current image in `assets/images/` | Suggested replacement |
| --- | --- | --- |
| Full-width hero / Formula SAE | `formula-sae-placeholder.svg` | Wide vehicle or workshop photo, ideally 2:1; keep the subject away from the centered title |
| Suspension project | `suspension-placeholder.svg` | SolidWorks assembly render, landscape 4:3 |
| Tire-analysis project | `tire-analysis-placeholder.svg` | Your MATLAB plot, landscape 4:3 |
| Manufacturing project | `manufacturing-placeholder.svg` | Machined parts or workshop photo, landscape 4:3 |

1. Save your own image in `assets/images/`, for example `suspension-cad.webp`. JPG and PNG also work. Use lowercase filenames with hyphens. Aim for 1,200–1,600 pixels wide and under about 500 KB when practical; retain legibility for plots.
2. In `index.html`, find the relevant placeholder filename and change only its `src` path to the new file. For example:

   ```html
   <img src="assets/images/suspension-cad.webp"
        alt="Describe the actual suspension assembly and what this view shows"
        width="800" height="600" loading="lazy">
   ```

3. Write specific alternative text describing the real image. Replace the accompanying “coming soon” caption with a short factual caption. For the hero image, edit the `.image-status` text near the bottom of the hero in `index.html`. Remove the obsolete placeholder comment if present.
4. Preview locally and upload both the edited HTML and the new image when ready.

The hero photograph fills a responsive banner and is cropped on smaller screens; use a wide shot and check both desktop and mobile after replacing it. A dark overlay keeps the title readable. The default hero is an original abstract grid, visibly labeled as a photo placeholder.

For a technical plot or CAD drawing that should remain fully visible, add `class="contain-image"` to its `<img>` element. That style preserves the whole image instead of cropping it to fill the frame. For photos, the default crop usually works well.

## Edit the content

- **Text and links:** Edit `index.html`. Every section is ordinary HTML; the three expandable project descriptions use native `<details>` elements.
- **Résumé:** Replace `assets/Eduardo-Alvarez-Resume.pdf` with a new PDF using the same filename. The download links will keep working.
- **Color:** Change the `--blue` value near the top of `assets/styles.css`; also update the theme color and embedded favicon in the HTML if changing the brand color.
- **Contact:** Email and LinkedIn were copied from the supplied résumé. The downloadable PDF is the original and includes its contact information, including phone number. Replace that file if you prefer a different public résumé.
- **Dates:** Employment dates and “Present” reflect the supplied résumé. Confirm they are current before publishing; expected graduation is May 2028.
- **Project detail:** Add measured outcomes, dimensions, constraints, FEA results, and captions only when you have supporting information. The current site does not invent performance gains, safety-factor values, competition results, or tolerances.

## Content source

The source is the supplied Eduardo-Alvarez-Resume.pdf. The three project highlights organize different aspects of the same Husker Motorsports role; they are not presented as three separate employers or independently documented projects. Role titles, tools, education, contact information, and date ranges come from that résumé. Descriptions have been edited for clarity. The two numeric experience highlights (1,000+ students/families weekly and landscaping projects up to $100,000) are stated in the source.

The site includes no tracking, third-party fonts, forms, cookies, external image services, or build dependencies. GitHub Pages hosts the static files; email uses your visitor’s configured mail application.

## Layout direction

The layout takes inspiration from the broad structure of [Thanh Tran’s portfolio](https://thanhvtran.com/): a full-width introduction, summary, experience timeline, and project gallery. Eduardo’s typography, navy-and-blue color system, gallery arrangement, initials, placeholders, and writing are original to this project. No photographs, video, employer logos, or biographical claims were copied from that site.
