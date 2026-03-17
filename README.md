# Danika Singh — Portfolio Site

## Deploying to GitHub Pages (step by step)

### 1. Create a GitHub account
If you don't have one, sign up at https://github.com.

### 2. Create a new repository
1. Click the **+** icon (top right) → **New repository**.
2. Name it exactly: `your-username.github.io` (replace `your-username` with your actual GitHub username, e.g. `danikasingh.github.io`).
3. Set it to **Public**.
4. Leave "Add a README" **unchecked** (you already have one).
5. Click **Create repository**.

### 3. Install Git (if not already installed)
Download from https://git-scm.com and install with default settings.

### 4. Open a terminal in your project folder
In VS Code, open the Terminal (`` Ctrl+` ``) and make sure you are in the portfolio folder:
```
cd "C:\Users\danik\.vscode\danika-portfolio"
```

### 5. Initialise Git and push your files
Run these commands one by one:
```
git init
git add .
git commit -m "Initial portfolio deploy"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```
> Replace `your-username` with your actual GitHub username in the URL above.

### 6. Enable GitHub Pages
1. Go to your repository on GitHub.
2. Click **Settings** → **Pages** (left sidebar).
3. Under **Source**, select **Deploy from a branch**.
4. Set branch to `main`, folder to `/ (root)`.
5. Click **Save**.

### 7. Your site is live
After about 1–2 minutes your portfolio will be live at:
```
https://your-username.github.io
```

---

## Updating the site after changes
Whenever you make changes locally, run:
```
git add .
git commit -m "describe your change"
git push
```
GitHub Pages will automatically redeploy within a minute.

---

## Adding or updating certificates

1. Add your PDF file into the `certs/` folder, e.g. `certs/my-cert.pdf`.
2. Open `certs.json` and add an entry:
   ```json
   {
     "name": "My Certificate Name",
     "file": "certs/my-cert.pdf"
   }
   ```
3. Save, then push your changes (see **Updating the site** above).

> Certificate files must be committed to the repo so they are publicly accessible. The **Certificates** button on the site reads `certs.json` and links directly to the PDFs.
