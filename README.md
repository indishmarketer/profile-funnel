# Shubho Dey – Systems & Growth (One-Page Profile)

A fast, modern, single-page personal profile built with **HTML + Tailwind CSS + Vanilla JavaScript**.  
This page is designed to act as a **link-in-bio / personal landing page** with newsletter signup, courses, socials, projects, testimonials, and contact form — all powered by a single static file.

---

## ✨ Features

- 🚀 **Single-file static site** (no build step required)
- 🎨 **Tailwind CSS (CDN)** for styling
- ⚡ **FOUC-free loading** (no ugly flash on load)
- 🖼️ Hero image preloaded for faster first paint
- 📨 Newsletter + Contact form (via Webhook)
- 🎥 Video modal support (YouTube embeds)
- 🧱 Skeleton loaders for better UX
- 📱 Fully responsive (mobile-first)
- 🔒 No backend required

---

## 🛠️ Tech Stack

- **HTML5**
- **Tailwind CSS (via CDN)**
- **Vanilla JavaScript**
- **Lucide Icons**
- **Webhook (Pabbly / Zapier / Make)**

---

## 📁 Project Structure

This project uses **ONE FILE ONLY**:

```

/
├── index.html
└── README.md

````

There is:
- ❌ No Node.js
- ❌ No React
- ❌ No build tools
- ❌ No server

---

## 🚀 How to Run Locally

### Option 1: Open directly
Just double-click `index.html` and open it in your browser.

### Option 2: Simple local server (recommended)
```bash
# Python
python -m http.server
````

Then open:

```
http://localhost:8000
```

---

## 🌐 Deployment Options

This is a **static site**, so choose **Static / No Build**.

### Cloudflare Pages

* Connect GitHub repo
* Framework preset: **None**
* Build command: ❌ (leave empty)
* Output directory: `/`

### Coolify

* Build Pack: **Static**
* Port: ❌ not required
* Start command: ❌ not required

### GitHub Pages

* Enable Pages
* Source: `main` branch
* Folder: `/root`

---

## 🔗 Webhook Configuration

This page sends data to **one webhook URL** for both forms.

### Edit this line in `<script>`:

```js
const WEBHOOK_URL = "https://your-webhook-url-here";
```

### Payload Types Sent

#### Newsletter form

```json
{
  "type": "newsletter",
  "name": "User Name",
  "email": "user@email.com",
  "page": "current URL"
}
```

#### Contact form

```json
{
  "type": "contact",
  "name": "User Name",
  "email": "user@email.com",
  "message": "User message",
  "page": "current URL"
}
```

You can route both in your automation tool based on `type`.

---

## 🎥 Video Modal (YouTube)

Social cards and testimonials support video playback using:

```js
videoEmbed: "https://www.youtube.com/embed/VIDEO_ID"
```

Videos open inside a modal (no redirect).

---

## ✏️ Customization Guide

### Change Name

```html
<h2>Shubho Dey</h2>
```

### Change Mission Statement

```html
<h1>My mission is to help businesses...</h1>
```

### Update Social Links

Edit the `SOCIALS` array in JavaScript.

### Update Courses / Projects / Testimonials

Edit:

* `COURSES`
* `PROJECTS`
* `TESTIMONIALS`

All sections auto-render from data.

---

## 🧩 Icons Used

Powered by **Lucide Icons**.

Common icons:

* `youtube`
* `instagram`
* `linkedin`
* `book-open` (Medium)
* `file-text` (Blog)
* `image` (Pinterest)

---

## 🛡️ Security Notes

* No API keys exposed
* Webhook URL is public (expected for static sites)
* Add validation inside your automation tool if needed

---

## 📜 License

This project is **free for personal use**.

If you reuse or adapt it:

* Give credit 🙏
* Don’t resell as a template without modification

---

## 👋 Author

**Shubho Dey**
Solo Builder — Systems & Growth

* 🌐 [https://www.indishmarketer.com](https://www.indishmarketer.com)
* 🧠 Newsletter: Weekly (Sundays, 10 AM)

---

## ✅ Final Notes

This project is intentionally:

* Simple
* Fast
* Beginner-friendly
* Production-ready

If you ever want to:

* Split CSS / JS
* Convert to React / Next.js
* Add analytics
* Improve Lighthouse score

You can do that later — this foundation is solid.

---

Happy building 🚀


