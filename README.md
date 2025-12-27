# Pathway Consulting Group (Free 3-page website)

This folder contains a simple, conservative 3-page website:
- Home: `index.html`
- About: `about.html`
- Contact: `contact.html`

## Free hosting (recommended): GitHub Pages

### 1) Create a GitHub repo
1. Log into GitHub
2. Create a new repository named **pathwaycg.com** (or any name you want)
3. Upload the contents of this folder to the repo (keep files at the root)

### 2) Turn on GitHub Pages
1. Repo → **Settings** → **Pages**
2. Under **Build and deployment**, set:
   - Source: **Deploy from a branch**
   - Branch: **main** (or master) and **/(root)**
3. Save
4. Your site will publish at: `https://YOURGITHUBUSERNAME.github.io/REPO`

### 3) Set the custom domain to pathwaycg.com
In Repo → Settings → Pages:
1. In **Custom domain**, enter: `pathwaycg.com`
2. Check **Enforce HTTPS** (after it becomes available)

GitHub will create a `CNAME` file automatically. If not, create a file named `CNAME` containing:
```
pathwaycg.com
```

## Point GoDaddy DNS to GitHub Pages

In GoDaddy → Domain → DNS Management:

### A records (for apex/root domain)
Set these **A records** for **@** (root):
- 185.199.108.153
- 185.199.109.153
- 185.199.110.153
- 185.199.111.153

(You may need to delete existing A records first.)

### CNAME record (for www)
Set **CNAME**:
- Host: `www`
- Points to: `YOURGITHUBUSERNAME.github.io`

### Wait for DNS
DNS may take from minutes up to 24 hours. HTTPS may take a bit longer to fully enable.

## Activate the contact form (optional)
The contact form is set to a placeholder:

`action="YOUR_FORMSPREE_ENDPOINT"`

To enable:
1. Create a free form on Formspree (or similar)
2. Copy your form endpoint URL
3. Replace `YOUR_FORMSPREE_ENDPOINT` in `contact.html` with your URL
4. Commit/push changes

## Quick edits
- Colors and layout: `css/styles.css`
- Home hero text: `index.html`
- Address/phone/email appear in all pages (embedded in HTML for simplicity)

