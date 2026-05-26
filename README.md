# 💍 Yuan & Ismery — Wedding Website

A beautiful, single-file wedding website for **September 11, 2025**.

## 📁 File Structure

```
Wedding/
├── index.html        ← The entire website (open this in any browser)
├── README.md         ← This file
└── photos/
    ├── 1.jpg         ← Hero background photo (full-screen)
    ├── 2.jpg         ← "Our Story" section photo
    ├── 3.jpg         ← Gallery photo 1
    ├── 4.jpg         ← Gallery photo 2
    ├── 5.jpg         ← Gallery photo 3
    ├── 6.jpg         ← Gallery photo 4
    ├── 7.jpg         ← Gallery photo 5
    ├── 8.jpg         ← Gallery photo 6
    ├── 9.jpg         ← Gallery photo 7
    └── 10.jpg        ← Gallery photo 8
```

---

## 🖼️ How to Replace Photos

1. Create a folder named `photos` in the same directory as `index.html` (if it doesn't exist).
2. Add your photos using the **exact filenames** listed above (e.g., `1.jpg`, `2.jpg`, etc.).
3. Photos can be `.jpg`, `.jpeg`, `.png`, or `.webp` — just rename them to match the expected filename and extension used in the HTML.
4. Reload `index.html` in your browser — photos will appear automatically.

> **Tip:** Each `<img>` tag in the HTML contains a comment like `<!-- Replace photos/3.jpg with your gallery photo #1 -->` to help you identify which file maps to which slot.

---

## 👥 How to Add Guests to the Seat Finder

Open `index.html` in any text editor (Notepad, VS Code, etc.) and find this section near the bottom inside the `<script>` tag:

```javascript
const guestList = [
  { name: "Juan Pérez",    seats: 2, table: "Table 1" },
  { name: "María García",  seats: 1, table: "Table 3" },
  // ADD MORE GUESTS HERE
];
```

Add a new line for each guest following the same format:

```javascript
{ name: "Guest Full Name", seats: 2, table: "Table 4" },
```

- **`name`** — The exact name guests will type when searching (search is case-insensitive).
- **`seats`** — Number of seats reserved for this guest.
- **`table`** — The table label displayed in the result (e.g., `"Table 5"`).

Save the file and the seat finder will use the updated list immediately.

---

## 🌐 How to Deploy to GitHub Pages (3 steps)

### Step 1 — Push your files to GitHub

Create a new public repository on [github.com](https://github.com) and upload:
- `index.html`
- `README.md`
- The entire `photos/` folder

You can drag & drop the files directly on the GitHub website, or use the command line:

```bash
git init
git add .
git commit -m "Wedding website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### Step 2 — Enable GitHub Pages

1. Go to your repository on GitHub.
2. Click **Settings** → **Pages** (in the left sidebar).
3. Under **Source**, select **Deploy from a branch**.
4. Choose **`main`** branch and **`/ (root)`** folder.
5. Click **Save**.

### Step 3 — Visit your live site

After 1–2 minutes, your site will be live at:

```
https://YOUR_USERNAME.github.io/YOUR_REPO/
```

GitHub will show the URL in the **Pages** settings after deployment.

---

## ✏️ Other Customizations

| What to change | Where to find it in `index.html` |
|---|---|
| Contact email | Search for `yuan.ismery@example.com` — replace both occurrences |
| WhatsApp number | Search for `wa.me/15551234567` — replace the number (no `+` sign) |
| Ceremony venue & time | Inside `<!-- CEREMONY CARD -->` in the Details section |
| Reception venue & time | Inside `<!-- RECEPTION CARD -->` in the Details section |
| Love story text | Three `<p>` tags inside `#story .story-text` |
| Wedding date | The JS countdown target: `new Date('2025-09-11T16:00:00')` |

---

Made with ❤️ — Yuan & Ismery, September 11, 2025
