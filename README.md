# BLACCTOGRAPHY — Website

> "Your OC Photography Man" · Mobile Phone Photography · DMV Area

---

## 🚀 How to Deploy to GitHub Pages

### Step 1 — Create a GitHub Repo
1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **"New repository"**
3. Name it exactly: `blacctography` (or your GitHub username repo for a root URL)
4. Set it to **Public**
5. Click **"Create repository"**

### Step 2 — Upload the Files
1. On your new repo page, click **"uploading an existing file"**
2. Drag and drop **all files and folders** from this zip:
   - `index.html`
   - `portfolio.html`
   - `about.html`
   - `contact.html`
   - `css/style.css`
   - `js/main.js`
   - `images/` folder (add your photos here — see below)
3. Click **"Commit changes"**

### Step 3 — Enable GitHub Pages
1. Go to your repo **Settings** tab
2. Scroll to **Pages** in the left sidebar
3. Under **Source**, select `main` branch and `/ (root)` folder
4. Click **Save**
5. Your site will be live at: `https://yourusername.github.io/blacctography/`

---

## 📸 Adding Your Real Photos

The portfolio page uses placeholder emoji blocks. To add your actual photos:

1. Put your photo files in the `/images/` folder
2. Open `portfolio.html` and find each `.port-item` block
3. Replace the `.port-ph` div with an `<img>` tag:

```html
<!-- BEFORE (placeholder) -->
<div class="port-ph fc1" style="--ar:1" data-caption="Events · DC">🎉</div>

<!-- AFTER (real photo) -->
<img src="images/your-photo.jpg" alt="Event coverage DC 2025" class="port-item-img" style="--ar:1"/>
```

**Recommended image specs:**
- Format: JPG or WebP
- Width: 1200px max (keeps load times fast)
- Quality: 80% compression
- Name files clearly: `event-dc-march-2025.jpg`

---

## 📁 File Structure

```
blacctography/
├── index.html          → Homepage (hero, pricing, booking form, testimonials)
├── portfolio.html      → Portfolio grid with category filter + lightbox
├── about.html          → About / story / philosophy page
├── contact.html        → Contact form + FAQ
├── css/
│   └── style.css       → All shared styles (tokens, nav, footer, animations)
├── js/
│   └── main.js         → Shared JavaScript (flash effect, scroll reveal, forms)
├── images/             → Add your photos here
│   └── .gitkeep
└── README.md           → This file
```

---

## ✏️ Customization Notes

- **Colors**: Edit the CSS variables at the top of `css/style.css` under `:root {}`
- **Pricing**: Update prices in `index.html` (search for `$150`, `$250`, `$500`)
- **Email**: Replace `connectwithblaccmatter@gmail.com` throughout all files
- **Instagram**: Replace `@blacctography` / `instagram.com/blacctography` throughout
- **Pixieset**: Replace `blacctographyinc.pixieset.com` throughout

---

## 🔗 External Links (pre-configured)
- Instagram: https://instagram.com/blacctography
- Print Shop: https://blacctographyinc.pixieset.com
- Email: connectwithblaccmatter@gmail.com

---

© 2025 Blacctography · DMV Mobile Photography
