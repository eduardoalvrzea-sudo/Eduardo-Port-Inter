# Eduardo Alvarez — Mechanical Engineering Portfolio

A complete, responsive portfolio based on the supplied Eduardo-Alvarez-Resume.pdf. It includes a full-width introduction, personal summary, alternating experience timeline, image-led Formula SAE project gallery, technical skills, education, contact links, and a downloadable copy of the résumé.

**Nothing has been uploaded or published.** Follow the GitHub steps below when you are ready to make it public.

## Open the site locally

Extract the ZIP, then double-click `index.html` inside `eduardo-portfolio`. It works directly in a browser without installation, JavaScript, a build process, or an internet connection. Email and LinkedIn links open external applications or sites.

## Files

```text
eduardo-portfolio/
├── index.html                  Homepage and clickable project cards
├── projects/
│   ├── suspension.html         Suspension detail page
│   ├── tire-analysis.html      Tire-analysis detail page
│   └── manufacturing.html      Manufacturing detail page
├── assets/
│   ├── styles.css              Original portfolio layout and styles
│   ├── project-pages.css       Project detail pages and card links
│   ├── Eduardo-Alvarez-Resume.pdf
│   └── images/                 Your photos, CAD renders, plots, and logos
├── EDITING-PROJECTS.md         How to add text, images, and new projects
├── .nojekyll
├── .gitignore
└── README.md
```

## Project detail pages

Click any project card to open its full page in the same tab. Each page includes an overview, your contribution, an engineering-process section, a gallery, and links back to the homepage and onward to another project. Click a detail-page image to open the original at full size.

Read [EDITING-PROJECTS.md](EDITING-PROJECTS.md) for copy-and-paste examples for adding paragraphs, photos, results, and new project pages. The pages are plain HTML and work both locally and on GitHub Pages.

## Exact GitHub Pages deployment steps

These are actions for you to perform. Creating a public repository makes its uploaded files public; enabling Pages publishes the website. Use a new repository so that you do not overwrite an existing site.

1. Sign in to [GitHub](https://github.com), click **+** at the upper right, then **New repository**.
2. Enter **portfolio** as the repository name. Choose **Public** for GitHub Free. Turn **Add README** on, then click **Create repository**.
3. In the repository’s **Code** tab, choose **Add file → Upload files**.
4. Open the extracted `eduardo-portfolio` folder. Drag its **contents** into the upload area: `index.html`, `assets`, `projects`, `README.md`, `EDITING-PROJECTS.md`, `.nojekyll`, and `.gitignore`. Upload the contents, not the enclosing folder or ZIP. Keep the `assets` folder structure intact.
5. Enter **Add mechanical engineering portfolio** as the commit message. Select **Commit directly to the main branch**, then click **Commit changes**.
6. Verify `index.html` and `.nojekyll` appear in the repository’s top-level file list alongside `assets` and `projects`. If `.nojekyll` was omitted by your file picker, use **Add file → Create new file**, name it `.nojekyll`, enter one blank line, and commit it to `main`.
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

The homepage uses your Formula SAE track photo, suspension CAD assembly, tire-data plot, and component drawing. The detail pages reuse these assets and include labeled spaces for additional images you can add later.

| Area | Current file in `assets/images/` |
| --- | --- |
| Hero / Formula SAE track photo | `formula-sae-placeholder.jpg` |
| Suspension assembly | `Suspension Master Assembly.PNG` |
| Tire-data plot | `tire-analysis-polished.png` |
| Rear left upright drawing | `Hub Drawing.png` |

Save new images in `assets/images/`, then update the image paths in the relevant HTML file. Preserve filename capitalization exactly: GitHub Pages paths are case-sensitive. A detail-page image path starts with `../assets/images/`; a homepage image path starts with `assets/images/`.

The detail pages fit the whole image inside its frame without cropping. The hero uses a cropped background photo. For complete gallery examples and captions, see [EDITING-PROJECTS.md](EDITING-PROJECTS.md).

## Edit the content

- **Text and links:** Edit `index.html` for the homepage, or the corresponding file in `projects/` for an in-depth project page. Each homepage card opens its detail page through a normal link.
- **Résumé:** Replace `assets/Eduardo-Alvarez-Resume.pdf` with a new PDF using the same filename. The download links will keep working.
- **Color:** Change the `--blue` value near the top of `assets/styles.css`; also update the theme color and embedded favicon in the HTML if changing the brand color.
- **Contact:** Email and LinkedIn were copied from the supplied résumé. The downloadable PDF is the original and includes its contact information, including phone number. Replace that file if you prefer a different public résumé.
- **Dates:** Employment dates and “Present” reflect the supplied résumé. Confirm they are current before publishing; expected graduation is May 2028.
- **Project detail:** Add measured outcomes, dimensions, constraints, FEA results, and captions only when you have supporting information. The current site does not invent performance gains, safety-factor values, competition results, or tolerances.

## Content source

The original source is the supplied Eduardo-Alvarez-Resume.pdf, with subsequent text and image edits supplied by Eduardo. The three project highlights organize different aspects of the same Husker Motorsports role; they are not presented as three separate employers or independently documented projects. Role titles, tools, education, contact information, and date ranges come from that résumé. Descriptions have been edited for clarity. The two numeric experience highlights (1,000+ students/families weekly and landscaping projects up to $100,000) are stated in the source.

The site includes no tracking, third-party fonts, forms, cookies, external image services, or build dependencies. GitHub Pages hosts the static files; email uses your visitor’s configured mail application.

