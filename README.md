# Portfolio Website

A responsive personal portfolio website built with HTML, CSS, and JavaScript.

This project is designed for simple static hosting (including GitHub Pages) and includes:

- Hero section with profile image and resume button
- About, Experience, Projects, Skills, Education, and Contact sections
- Mobile-friendly navigation with hamburger menu
- Scroll-based section reveal animation
- Certificate panel that loads certificate links from a JSON file

## Project Structure

```text
.
|-- index.html
|-- style.css
|-- certs.json
|-- index-template.html
|-- certs-template.json
|-- certs/
|-- images/
```

## Run Locally

Because certificates are loaded with `fetch`, run the site through a local server (not by opening the HTML file directly).

Option 1: VS Code Live Server

1. Install the Live Server extension.
2. Open the project folder in VS Code.
3. Right-click `index.html` and choose Start Live Server.

Option 2: Python simple server

```bash
python -m http.server 5500
```

Then open `http://localhost:5500`.

## Customize Content

Edit `index.html` and replace:

- Name, title, and profile image
- About text
- Experience entries
- Project details and links
- Skills categories and chips
- Education
- Contact details

Resume button:

- Place your PDF in the project root as `resume.pdf`, or
- Update the resume link in `index.html` to your preferred file path.

## Certificates

Certificate links are read from `certs.json`.

Example format:

```json
[
  {
    "name": "Data Science Certificate",
    "file": "certs/data-science.pdf"
  }
]
```

Steps:

1. Add certificate PDFs to the `certs/` folder.
2. Add or update entries in `certs.json`.
3. Keep paths relative, for example `certs/my-certificate.pdf`.

## Generic Template Version

If you want to reuse this layout for other people:

- Use `index-template.html` for placeholder-based content
- Use `certs-template.json` for certificate placeholders

This lets you duplicate the structure quickly and swap personal details.

## Deploy to GitHub Pages

1. Create a public GitHub repository.
2. Push this project to the `main` branch.
3. In GitHub: Settings > Pages.
4. Set Source to Deploy from a branch.
5. Choose `main` and `/ (root)`.
6. Save and wait 1 to 2 minutes.

Your site will be available at:

```text
https://your-username.github.io/repository-name/
```

If your repository is named `your-username.github.io`, the URL is:

```text
https://your-username.github.io/
```

## Update Workflow

After making changes:

```bash
git add .
git commit -m "Update portfolio content"
git push
```

GitHub Pages will redeploy automatically.
