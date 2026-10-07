# Wisdom David — Solutions Architect portfolio

A responsive, standalone HTML/CSS/JavaScript portfolio. No framework, account integration, build command, package installation, or external fonts required. All paths are relative, so it works at both a GitHub user-site URL and a project-site URL. Open `index.html` in your browser to preview it locally.

## Files

```text
wisdom-david-portfolio/
  index.html                       All visible content and editing comments
  styles.css                       Base layout and responsive rules
  design.css                       Refreshed visual theme and overrides
  ASSET-SOURCES.md                  Badge/logo provenance
  script.js                        Accessible mobile navigation
  .nojekyll                        Keeps GitHub Pages serving static files
  README.md                        These instructions
  assets/
    profile.jpg                    Portrait extracted from the supplied CV
    wisdom-david-cv.pdf             Public downloadable CV
    favicon.svg                    Browser tab icon
    profile-placeholder.svg        Replace with your portrait
    certification-placeholder.svg  Replace with actual credential images
    project-placeholder.svg        Replace with your architecture diagram
```

## Positioning and source material

The portfolio leads with **AWS Solutions Architect**, supported by **Cloud & DevOps Engineer**. This is professional positioning; the employment timeline preserves the actual title **AWS Cloud/DevOps Engineer** at ALLUVIUM (2024–Present). It does not claim a senior title or an AWS DevOps Engineer certification.

The supplied `WISDOM_DAVID_FlowCV_Resume_2026-10-07.pdf` is the source for all three certifications, five courses, three employment entries, education, technical skills, and the four professional project summaries. A public copy of the CV, with the referee section removed, is included as `assets/wisdom-david-cv.pdf`. Its embedded portrait is extracted as `assets/profile.jpg`.

Included certifications:
- AWS Certified Solutions Architect – Associate
- KCNA: Kubernetes and Cloud Native Associate
- AWS Certified Cloud Practitioner

Included courses:
- Professional Development Skills — ALX Africa, 2025
- AWS and DevOps Engineering — SolaviseTech, 2024
- ALX Cloud Practitioner Program — ALX Africa, 2025
- AI Literacy — IBM (no year supplied)
- Cloud Migration Technical Delivery — Atlassian, 2024

The three certification links and IBM AI Literacy badge link come directly from the PDF. No credential issue/expiry dates or current status have been inferred. Other course links in the CV point to the same shared Google Doc rather than distinct credential records; they have not been used as individual verification links. Add direct course evidence when available.

The earlier interview architecture assessment is retained as secondary work, separately labeled. Project screenshots, original deployment diagrams, and repositories were not provided. The site now uses explicitly labelled SVG illustrations based on the CV, and downloaded badge images from the supplied credential pages. No deployment-scale or performance figures were invented. Kubernetes appears as certification-backed foundational knowledge, not an invented production responsibility.

The publicly downloadable CV omits the referee section and its private contact details. The supplied original remains unchanged in Downloads. The current LinkedIn URL was supplied in chat. The GitHub connection identified the account as `wisdomdavidtech`; both profiles are linked.

## Publish on GitHub Pages — browser-only steps

1. Sign in to GitHub and note your exact username.
2. Create a new repository. For your main personal site, name it **YOUR-USERNAME.github.io**, replacing `YOUR-USERNAME` with your actual GitHub username. Your connected account is `wisdomdavidtech`, so the recommended repository is **wisdomdavidtech.github.io**. Alternatively, name a project repository **solutions-architecture-portfolio**.
3. Choose **Public** for the simplest GitHub Free setup. Create the repository with a README so the `main` branch exists.
4. Extract this project ZIP on your computer. Open the `wisdom-david-portfolio` folder.
5. In the repository, choose **Add file → Upload files**. Upload the **contents** of that folder, including the `assets` folder. Do not upload the ZIP or an extra enclosing project folder. Replace the starter README with this one. Commit to `main`.
6. Confirm `index.html`, `styles.css`, `script.js`, `assets`, and `.nojekyll` appear at the repository root. If the hidden `.nojekyll` file was not uploaded, choose **Add file → Create new file**, name it `.nojekyll`, add an empty line, and commit it.
7. Open **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**. Select **main** and **/(root)**, then click **Save**.
8. Wait for publishing to complete. Check the repository's **Actions** tab if necessary. Return to **Settings → Pages** and click **Visit site**.
9. A user repository is served at `https://YOUR-USERNAME.github.io/`. A project repository is served at `https://YOUR-USERNAME.github.io/solutions-architecture-portfolio/`. Updates can take up to 10 minutes to appear.

No custom workflow, Node.js, build output folder, or GitHub secret is needed. Future commits to `main` publish updates automatically. If you see a 404, check the selected branch/folder and that the lowercase file `index.html` is directly inside that folder. File names are case-sensitive on the deployed site.

Official instructions checked when preparing this project:
- [Create a GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- [Configure the publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

## Edit text

Open `index.html` in a plain-text editor such as VS Code or Notepad. Search for the visible sentence or a section ID: `about`, `focus`, `work`, `skills`, `credentials`, `courses`, `experience`, or `contact`. Change text between the HTML tags and save. Keep the tags and IDs intact. Refresh the browser to see changes. The entire page remains readable with JavaScript disabled.

To change text online, open `index.html` on GitHub, click the pencil icon, edit, and commit to `main`. For color changes, edit the variables at the top of `design.css` (it overrides the base theme in `styles.css`); `--accent` controls the rust accent, `--paper` the background, and `--ink` the primary text. Keep adequate contrast. The title and search description are near the top of `index.html`.

## Update your profile photo

Your photo from the CV is already included as `assets/profile.jpg` in the hero section. Replace that file with a new portrait (ideally a square image around 900 × 900 pixels, under 500 KB) and refresh the site. Keep the filename, or update the `src` in `index.html`. Keep the `alt` text accurate. The original placeholder asset is retained as an optional fallback.

## Add or update certifications and courses

All three certifications and all five courses from your CV are included. AWS, KCNA, and IBM images are bundled locally. ALX and Atlassian courses use provider logos; SolaviseTech uses a simple text label. Each entry can be replaced with an actual certificate image. See `ASSET-SOURCES.md`.

1. Save badge/certificate images in `assets` using clear names, such as `aws-solutions-architect.png`, `kcna.png`, `aws-cloud-practitioner.png`, or `alx-professional-development.png`.
2. Find the relevant `cert-card` or `course-card` in `index.html`. Replace its current image `src` with the new path, and update its `alt` text. Small square badge images fit best. A certificate scan can also be linked at full size.
3. Existing credential links are already populated from your CV. Add a missing course evidence link beneath its heading using this pattern, replacing the entire example URL:

```html
<a class="text-link" href="PASTE-YOUR-ACTUAL-CERTIFICATE-URL">View certificate ↗</a>
```

4. For a new professional certification, duplicate a complete `<article class="cert-card">...</article>` inside `cert-grid`. For a new course, duplicate a `<article class="course-card">...</article>` inside `course-grid`. Update the title, provider, optional year, image, and link. Update the counts `03` / `05` and introductory sentence too.
5. Keep courses and professional certifications separate. Add issue/expiry dates only from actual credential records, and do not add a year to IBM AI Literacy until confirmed.

## Add project screenshots, architecture diagrams, and case studies

Save a shareable screenshot/diagram as `assets/project-architecture.webp` (PNG also works; around 1400 pixels wide). Find the image within the relevant `project` or `work-card` article in `index.html` and replace its current SVG path and `alt`. Each professional project has its own slot. For a detailed diagram, consider adding a link to its full-resolution file. Remove the note about missing artifacts when they have been added.

The expandable project and assessment sections use native HTML `<details>` and work without JavaScript. Edit their paragraphs to document the actual problem, constraints, decisions, alternatives, and supported results. Add proposal or presentation PDFs to `assets` and link with relative paths such as `assets/architecture-proposal.pdf`. Share only material you are permitted to publish; remove private customer information. Do not imply the assessment was deployed or attach invented results.

To add a project, copy a complete `<article class="work-card">...</article>` inside `work-grid`, then replace the content and image. The grid automatically adapts. The lead ECS project uses the larger `project` layout.

## Update employment and education

The `experience` section contains ALLUVIUM, Tinuola International College, EduPoint, and OND & HND Computer Science at Yaba College of Technology. Edit or duplicate timeline articles as roles change. Preserve actual job titles and only use supported outcomes. Education dates were not supplied, so none have been added.

## Update the CV download

The download button is now enabled and points to the public CV PDF at `assets/wisdom-david-cv.pdf`. Replace that file with your next CV using the same filename. Update the visible revision date in the contact card. Click the button to confirm the correct PDF opens or downloads; browser behavior varies.

The public PDF preserves the supplied CV except for removing the referee section; its headline remains AWS Cloud/DevOps Engineer. For a future architecture-focused CV revision, use an architecture-first headline and reorder your existing AWS design, Terraform, delivery, observability, and security evidence. Keep the actual employment title unchanged.

## Contact and social links

The email link opens the visitor's email application; there is no contact form or backend. To change it, update both the `mailto:` value and visible address. Your GitHub link is `https://github.com/wisdomdavidtech`; LinkedIn is `https://www.linkedin.com/in/wisdom-david-a96471435/`. If you rename LinkedIn, update both copies in `index.html` (hero and contact). The website cannot change account usernames for you.

## Before sharing

- Replace images or retain their honest placeholder labels.
- Check the assessment summary, certification titles/status, employment entries, and contact address against your own records.
- Keep the included CV and credential links current, and add permitted project artifacts as available.
- Try the navigation, mobile menu, case-study expansion, email link, and CV download.
- Test at phone and desktop widths. The design honors reduced-motion preferences and has keyboard focus styles and a skip link.
- Keep filenames lowercase without spaces, and keep relative paths such as `assets/photo.jpg` (without a leading slash) so project-repository deployment works.

The ZIP is a deliverable, not a published site. Follow the steps above to put it online under your GitHub account.


## Design revision

The latest visual pass introduces a prominent portrait, blue/navy palette, contrasting italic headline, credential ribbon, real badge artwork, distinct engineering illustrations, and direct LinkedIn/GitHub links. All three certifications and five courses remain visible; JavaScript is still limited to the mobile menu. No framework or external font was added.

The file browser refused automated access to the local-file page. This revision was checked through source structure, asset validation, image inspection, and link checks; a fresh browser rendering has not been verified. Open `index.html` and refresh your existing tab to see it.
