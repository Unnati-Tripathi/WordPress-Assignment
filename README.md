# ClearPath — Career Resource & Consulting Website

A professional WordPress website for **ClearPath**, a fictional career consulting service for students and fresh graduates. Built to demonstrate practical CMS skills, responsive design, content management, and deployment — suitable for a fresher-level technical interview.

## 🎯 Project Purpose

This is a **portfolio project** demonstrating real WordPress skills:
- Page and post creation using the Gutenberg block editor
- Content organization with categories and tags
- Media management and responsive design
- Theme customization without custom code
- Full site deployment to a live hosting environment

## 🏗️ Tech Stack

| Component | Choice |
|-----------|--------|
| CMS | WordPress (latest stable) |
| Theme | Kadence (Free) |
| Block Editor | Gutenberg (native) + Kadence Blocks |
| Contact Form | WPForms Lite |
| Migration | All-in-One WP Migration |
| Local Dev | LocalWP |
| Hosting | InfinityFree (free tier) |
| SSL | Let's Encrypt (via InfinityFree) |

## 📄 Website Pages

1. **Home** — Landing page with hero, services overview, featured resources, and CTA
2. **About** — Company mission, audience, and approach
3. **Services** — Resume Review, Interview Preparation, Career Planning
4. **Career Resources** — Library of articles and guides (WordPress Posts)
5. **Contact** — Contact form with alternative contact information

## 🎨 Design

- **Colors:** Navy blue (`#1B2A4A`), warm cream (`#FAF7F2`), teal accent (`#2A9D8F`)
- **Typography:** Inter (headings + body), Merriweather (accent quotes)
- **Style:** Clean, modern editorial — looks like a genuine small consultancy

## 📁 Repository Structure

```
WordPress-Assignment/
├── README.md                          ← You are here
├── .gitignore
├── docs/
│   ├── design-system.md               ← Colors, fonts, component specs
│   ├── deployment-guide.md            ← Full deployment walkthrough
│   ├── wordpress-setup-guide.md       ← LocalWP + theme + plugin setup
│   ├── gutenberg-building-guide.md    ← Step-by-step page building
│   ├── cms-demonstration-guide.md     ← How to demonstrate CMS skills
│   └── interview-prep.md             ← Interview Q&A and project intro
├── content/
│   ├── pages/
│   │   ├── home.md                    ← Home page content
│   │   ├── about.md                   ← About page content
│   │   ├── services.md                ← Services page content
│   │   └── contact.md                 ← Contact page content
│   └── posts/
│       ├── resume-checklist.md
│       ├── common-interview-questions.md
│       ├── job-application-tracking.md
│       ├── cover-letter-guide.md
│       └── networking-for-introverts.md
└── assets/
    └── images/                        ← Optimized images (added later)
```

## 🚀 Quick Start

### 1. Install LocalWP (Linux)

```bash
# Download the .deb package from https://localwp.com/
# Then install:
sudo dpkg -i local-*-linux.deb
sudo apt-get install -f   # Fix any dependency issues
```

### 2. Create the Site

1. Open LocalWP → Click **"Create a new site"**
2. Name: **ClearPath**
3. Environment: **Preferred** (uses latest PHP + MySQL)
4. Admin username: `admin` / Password: (choose a strong one)
5. Click **Add Site** → site available at `clearpath.local`

### 3. Install Theme & Plugins

1. Log into `clearpath.local/wp-admin`
2. **Theme:** Appearance → Themes → Add New → Search "Kadence" → Install & Activate
3. **Plugins:** Plugins → Add New → Install & Activate:
   - Kadence Blocks
   - WPForms Lite
   - All-in-One WP Migration

### 4. Build the Site

Follow the guides in `docs/` to configure the theme, build pages, and add content.

### 5. Deploy

Follow `docs/deployment-guide.md` for step-by-step InfinityFree deployment.

## ⚠️ Important Notes

- This is a **fictional company** — all services and content are samples for demonstration
- **No real client data**, testimonials, or fabricated statistics are used
- WordPress core files and `wp-config.php` are **never committed** to this repository
- Email delivery on free hosting is unreliable — this is documented honestly

## 📝 License

This project is created for educational and portfolio purposes.
