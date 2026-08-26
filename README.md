# AURA Data Intelligence Website

A complete static public website for AURA Data Intelligence. It uses only HTML, CSS, and vanilla JavaScript. There is no build step, backend, database, framework, or paid dependency.

The site works by opening `index.html` directly and is compatible with GitHub Pages when the full folder structure is preserved.

## Project structure

```text
aura-website/
|
|-- index.html
|-- privacy.html
|-- terms.html
|-- data-deletion.html
|-- contact.html
|-- meta-integration.html
|
|-- css/
|   `-- styles.css
|
|-- js/
|   `-- main.js
|
|-- assets/
|   `-- README.txt
|
`-- README.md
```

## Important: customize before launch

Search the entire project for `yourdomain.com` and `[INSERT` and replace every placeholder with accurate information.

Replace:

- `support@yourdomain.com` with your monitored product-support email.
- `privacy@yourdomain.com` with your monitored privacy and deletion-request email.
- `contact@yourdomain.com` with your monitored business-inquiries email.
- `[INSERT DATE]` with the effective date of each legal document.
- `[INSERT LEGAL NAME]` with the registered company or operator name.
- `[INSERT YOUR DELETION TIMEFRAME]` with a processing period your team can actually meet.
- `[INSERT LIABILITY CAP OR APPLICABLE FORMULATION]` after qualified legal review.
- `[INSERT GOVERNING JURISDICTION]` and `[INSERT VENUE / DISPUTE TERMS]` after qualified legal review.

The legal pages are practical starting points, not a substitute for advice from a qualified lawyer familiar with your business and the laws that apply to it.

## Preview locally

### Fastest option

Double-click `index.html`. The site has no backend and works directly from the file system.

### Recommended local server

Open a terminal in the `aura-website` folder, then run one of these commands:

```bash
python -m http.server 8000
```

If your system uses `python3`:

```bash
python3 -m http.server 8000
```

Open this address in your browser:

```text
http://localhost:8000/
```

Stop the preview server by returning to the terminal and pressing `Ctrl+C`.

## Deploy free with GitHub Pages

### Step 1 — Create a GitHub account

Go to [GitHub](https://github.com/) and sign in or create an account.

### Step 2 — Create the repository

1. On GitHub, create a new repository.
2. Name it `aura-website`.
3. Set visibility to **Public**.
4. Create the repository.

### Step 3 — Upload the files

Choose either browser upload or Git.

#### Option A — Browser upload

1. Open the new `aura-website` repository.
2. Click **Add file**.
3. Click **Upload files**.
4. Upload all files and folders inside this project, preserving the `css`, `js`, and `assets` folders.
5. Enter a commit message and click **Commit changes**.

Make sure `index.html` is at the repository root—not inside an extra nested folder.

#### Option B — Git

Open a terminal in the `aura-website` folder and run:

```bash
git init
git add .
git commit -m "Initial AURA website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/aura-website.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username. If Git asks you to authenticate, follow GitHub's sign-in instructions.

### Step 4 — Enable GitHub Pages

1. Open the repository on GitHub.
2. Click **Settings**.
3. Select **Pages** in the sidebar.
4. Under **Build and deployment**, choose **Deploy from a branch** as the source.
5. Select the `main` branch.
6. Select the `/(root)` folder.
7. Click **Save**.

After GitHub finishes publishing, the site URL should look like:

```text
https://YOUR_USERNAME.github.io/aura-website/
```

GitHub Pages publishing may take a few minutes after the first setup or a new commit.

### Step 5 — Test the public legal URLs

Open each URL and confirm that the page loads:

```text
https://YOUR_USERNAME.github.io/aura-website/privacy.html
https://YOUR_USERNAME.github.io/aura-website/terms.html
https://YOUR_USERNAME.github.io/aura-website/data-deletion.html
https://YOUR_USERNAME.github.io/aura-website/meta-integration.html
```

Where appropriate, these public URLs may later be entered in Meta Developer settings:

- Privacy Policy URL: `https://YOUR_USERNAME.github.io/aura-website/privacy.html`
- Terms of Service URL: `https://YOUR_USERNAME.github.io/aura-website/terms.html`
- User Data Deletion URL: `https://YOUR_USERNAME.github.io/aura-website/data-deletion.html`
- Meta integration information: `https://YOUR_USERNAME.github.io/aura-website/meta-integration.html`

Always verify the current requirements in your Meta Developer dashboard before submitting an app for review.

## Connect a custom domain later

You can later use a domain such as:

```text
https://auradataintelligence.com
```

At a high level:

1. Buy a domain from a domain registrar.
2. Open the GitHub repository.
3. Go to **Settings**, then **Pages**.
4. Enter the domain under **Custom domain**.
5. Add the required DNS records with your domain provider.
6. After DNS is configured and verified, enable **Enforce HTTPS** when available.

DNS records can change by domain type and GitHub configuration. Follow the current [GitHub Pages custom-domain documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) instead of copying unverified DNS values.

After connecting a domain, update any URLs entered in third-party developer dashboards if you want them to use the custom domain.

## Security requirements

Never commit any of the following to this website or another public repository:

- Meta App Secret
- Facebook password
- Cookies or session cookies
- Access tokens or long-lived tokens
- Database passwords
- API secret keys
- Private credentials of any kind

**Anything committed to a public GitHub repository should be considered public.**

This static site does not contain or need credentials. Authentication, token exchange, secret storage, and webhook verification belong in a secure backend—not in browser JavaScript or public HTML.

If you add a backend in a separate future project, create a `.gitignore` before the first commit. At minimum, exclude environment and secret files such as:

```gitignore
.env
.env.*
!.env.example
*.pem
*.key
secrets/
```

Do not rely on `.gitignore` to protect a secret after it has already been committed. Rotate any exposed credential immediately and remove it from repository history using an appropriate security process.

## Updating the site

- Edit page content in the corresponding `.html` file.
- Change colors, spacing, and components in `css/styles.css`.
- Keep interactive behavior in `js/main.js`.
- Use relative links such as `privacy.html`, `css/styles.css`, and `js/main.js`.
- Do not change project links to paths beginning with `/`; root-relative paths can break when the site is hosted under `/aura-website/`.
- This version intentionally includes no trackers, Meta Pixel, Google Analytics, server-side forms, secrets, or authentication logic.

