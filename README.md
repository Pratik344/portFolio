# Pratik Raval — Portfolio Website

A clean, responsive personal portfolio website built with pure HTML5, CSS3, and vanilla JavaScript.
No build tools, no dependencies — just open `index.html` in a browser.

---

## 🗂️ Project Structure

```
portfolio/
├── index.html          # Main HTML (all sections)
├── style.css           # All styles + dark/light theme
├── script.js           # Theme toggle, scroll reveal, nav behaviour
├── assets/
│   └── favicon.svg     # SVG favicon (PR initials)
└── README.md           # This file
```

---

## ✏️ How to Edit Content

| What to change | Where |
|---|---|
| Name, title, summary | `index.html` → `#home` and `#about` sections |
| Skills | `index.html` → `#skills` section |
| Work experience | `index.html` → `#experience` section |
| Projects | `index.html` → `#projects` section |
| Education | `index.html` → `#education` section |
| Contact info | `index.html` → `#contact` section |
| Colors / fonts | `style.css` → `:root` and `[data-theme="light"]` blocks |
| Animations timing | `style.css` → `.reveal`, `.delay-*` classes |
| Nav / scroll behaviour | `script.js` |

### Changing the Accent Color
Open `style.css` and update these two variables inside `:root`:
```css
--c-accent:  #4f8ef7;   /* main blue */
--c-accent-2: #38d9c0;  /* teal highlight */
```

### Adding a Real Profile Photo
Replace the initials avatar in `index.html`:
```html
<!-- Find this block and replace the .avatar-initials div -->
<div class="avatar-ring">
  <img src="assets/photo.jpg" alt="Pratik Raval"
       style="width:100%;height:100%;border-radius:50%;object-fit:cover;" />
</div>
```
Then put your photo at `assets/photo.jpg`.

### Adding a New Project Card
Copy one of the `.project-card` blocks inside `#projects` and update the content.

### Adding a GitHub Link
In a project card, add inside `.project-links`:
```html
<a href="https://github.com/your-username/repo" target="_blank" rel="noopener" class="project-link">
  <svg viewBox="0 0 24 24" fill="currentColor">
    <path d="M12 0C5.37 0 0 5.37 0 12c0 5.3 3.44 9.8 8.2 11.4.6.1.82-.26.82-.57v-2c-3.34.72-4.04-1.6-4.04-1.6-.54-1.38-1.33-1.74-1.33-1.74-1.09-.74.08-.73.08-.73 1.2.09 1.84 1.24 1.84 1.24 1.07 1.83 2.8 1.3 3.49 1 .1-.78.42-1.31.76-1.61-2.67-.3-5.47-1.33-5.47-5.93 0-1.31.47-2.38 1.24-3.22-.12-.3-.54-1.52.12-3.18 0 0 1-.32 3.3 1.23a11.5 11.5 0 016 0c2.28-1.55 3.29-1.23 3.29-1.23.66 1.66.24 2.88.12 3.18.77.84 1.23 1.91 1.23 3.22 0 4.61-2.8 5.63-5.48 5.92.43.37.81 1.1.81 2.22v3.29c0 .32.22.69.83.57C20.57 21.8 24 17.3 24 12c0-6.63-5.37-12-12-12z"/>
  </svg>
  GitHub
</a>
```

---

## 🚀 Deploying to GitHub Pages

### Step 1 — Create a GitHub Repository
1. Go to [github.com](https://github.com) and click **New repository**
2. Name it `portfolio` (or `<your-username>.github.io` for a root domain)
3. Set it to **Public**
4. Do **not** initialise with a README (you already have one)

### Step 2 — Push Your Files
Open a terminal in the `portfolio/` folder:

```bash
git init
git add .
git commit -m "Initial portfolio commit"
git branch -M main
git remote add origin https://github.com/<your-username>/portfolio.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Choose **main** branch and **/ (root)** folder
5. Click **Save**

Your site will be live at:
```
https://<your-username>.github.io/portfolio/
```
(It can take 1–3 minutes to go live.)

### Step 4 — Update After Changes
```bash
git add .
git commit -m "Update portfolio content"
git push
```
GitHub Pages will automatically rebuild and redeploy.

### Optional — Custom Domain
1. In **Settings → Pages**, enter your domain under **Custom domain**
2. Add a `CNAME` file to the repo root containing your domain:
   ```
   www.yourdomain.com
   ```
3. Configure your DNS registrar to point to GitHub's servers.

---

## 🌗 Dark / Light Mode
The site defaults to dark mode. The user's preference is saved in `localStorage`
under the key `pr-theme`. The toggle button in the top-right nav switches modes.

---

## 📱 Browser Support
Works in all modern browsers: Chrome, Firefox, Safari, Edge.
No polyfills needed for the features used.

---

## 📄 License
Feel free to use and adapt this portfolio for your own use.
