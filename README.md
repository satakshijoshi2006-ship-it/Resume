# Shatakshi Joshi — Portfolio

A responsive, dependency-free portfolio in HTML, CSS, and JavaScript. White, charcoal, and restrained teal styling; project detail dialogs; local document assets; keyboard navigation; reduced-motion support.

## Preview locally

From this folder, run:

```sh
python -m http.server 8000 --directory dist
```

Then visit http://localhost:8000. You can also open `dist/index.html` directly in a browser.

## Deploy with GitHub Actions (GitHub Pages)

1. Unzip this package.
2. Create a **public** repository named `portfolio` in your GitHub account. Choose `main` as the default branch.
3. Place the **contents** of the `portfolio` folder at the repository root. The repository must contain `dist/`, `.github/workflows/deploy.yml`, and this README. Do not upload the ZIP itself. The `.github` folder may be hidden in your file manager; ensure it is included.
4. Open the repository's **Settings → Pages**. Under **Build and deployment**, set **Source → GitHub Actions**.
5. Commit/push the files to `main`. If they were uploaded before changing the Pages setting, open **Actions → Deploy portfolio to GitHub Pages → Run workflow → main**.
6. Wait for the workflow to show a green check. Open its deployment URL, also shown in **Settings → Pages**.
7. For your account and a repository named `portfolio`, the expected URL is:
   `https://satakshijoshi2006-ship-it.github.io/portfolio/`
   This URL becomes available only after a successful deployment.

Every future push to `main` redeploys the website. No Node.js installation, build command, paid hosting, or secret token is required. The included workflow grants the scoped Pages permissions it needs.

### If you prefer a root URL

Name the repository `satakshijoshi2006-ship-it.github.io` instead. The expected URL will be `https://satakshijoshi2006-ship-it.github.io/`. All local asset paths are relative and work with either setup.

### Command-line upload option

Run inside the extracted `portfolio` folder after creating an empty GitHub repository:

```sh
git init
git add .
git commit -m "Add portfolio website"
git branch -M main
git remote add origin https://github.com/satakshijoshi2006-ship-it/portfolio.git
git push -u origin main
```

Authenticate with GitHub when prompted. Set Pages source to GitHub Actions as above.

### Troubleshooting

- **404 / missing site:** confirm Settings → Pages uses GitHub Actions and the workflow is green.
- **Workflow missing:** confirm `.github/workflows/deploy.yml` is at the repository root, not inside another `portfolio` folder.
- **Photos/PDFs missing:** upload the complete `dist/assets/` folder, preserving filenames and case.
- **Workflow not triggered:** the included workflow uses `main`; change it if your default branch has another name.
- **Pages environment approval:** if your repository has deployment protections, approve the run or configure its `github-pages` environment.

Official reference: https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages

## Academic summary

- ICSE Class X (2021): 518/600 = **86.33%**, using all six subject totals: 75, 94, 90, 84, 84, 91.
- ISC Class XII (2023): 387/500 = **77.40%**, using all five subjects: 87, 68, 71, 70, 91.
- BE Computer Science Engineering: **7.83/10 CGPA**, **128 credits earned**, currently Year 4 / Semester 7, as shown in the supplied profile.

The school summaries use all-subject averages, not a best-five/best-four calculation. CGPA uses its own 10-point graph and is not converted to a percentage. The latest academic profile takes precedence over the older resume's rounded CGPA of 8.0. Only the requested summary is displayed; the Results PDF and individual subject/semester records are not included in the public website.

## GitHub runner used

The included workflow runs entirely on GitHub Actions with `runs-on: ubuntu-latest`, a **GitHub-hosted runner**. GitHub provisions and disposes of the runner for each deployment. You do not need to install or register a runner on your computer, EC2, or another server. Since this is a static website, the runner checks out the repository, configures Pages, uploads `dist`, and deploys it directly.

## Content and edits

- `dist/index.html`: biography, internship, certifications, achievements, and contact information.
- `dist/app.js`: six projects, repository links, live links, screenshot/report resources, and dialogs.
- `dist/styles.css`: visual design and responsive breakpoints.
- `dist/assets/`: resume, project screenshot, project reports, training material, certificates, and certificate thumbnails.
- `.github/workflows/deploy.yml`: automated deployment.

### Intentionally awaiting your input

- Academics are included as a summary with percentage/CGPA graphs; raw marksheets are not published.
- Personal photo: omitted until you provide it. The hero uses your full name in plain, single-color text and a concise profile overview.
- Kubernetes certificate: the supplied temporary URL expired on 8 October 2026. Credential ID is included; please provide the PDF or a permanent verification URL to enable a certificate link.

### Source details

- The internship starts in September 2026 according to the offer letter. The resume lists August 2026; the site uses the formal start date of 7 September 2026.
- The document named `Dexaminds weekly standup.pdf` contains a Docker expense-tracker report. It is labeled by its contents on the website.
- The AWS link opens a course resource; it is not labeled a personal credential-verification link.
- The Java/Maven project uses the supplied screenshot; no public live URL was provided. The expense tracker was deployed locally; localhost is not presented as a public demo.
- Certificate 1: Travel Quest MERN project presentation, 29 November 2025.
- Certificate 3: NGIT Project Expo 2.0 winner, 23 July 2025.
- Certificate 4: Techgyan AI Hackathon participation, 8–9 February 2025.
- TechTonic, Hackfinity, and declamation achievements are taken from the resume. The attached certificates are not misrepresented as evidence for those different events.
- Expense tracker is credited as an adaptation of the open-source project by hakiKhuva; the described contribution is containerization and deployment.
- Other project descriptions stay limited to supplied information. You can provide richer descriptions, technology details, and additional screenshots later.

## Verification

JavaScript syntax, academic graph values, deployment workflow configuration, and local asset paths were checked. Six project dialogs handlers were checked using a simulated DOM; this does not verify browser rendering or native dialog focus behavior. A graphical browser was unavailable in this environment, so rendered desktop/mobile visual review is still recommended before public deployment. Open the page locally, check each project's two choices, resume/certificate/report links,.

Final presentation changes: footer, introductory sentence, section eyebrow labels Experience/Learning/Education, At a glance label, and custom site icon removed.
