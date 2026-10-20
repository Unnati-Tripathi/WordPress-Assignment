# ClearPath — Gutenberg Page Building Guide

Step-by-step instructions for building each ClearPath page in WordPress using the Gutenberg block editor and Kadence Blocks.

---

## Before You Start

Make sure you've completed the WordPress Setup Guide:
- ✅ Kadence theme is active
- ✅ Kadence Blocks plugin is active
- ✅ Colors and typography are configured in the Customizer
- ✅ Default content is deleted
- ✅ Permalinks set to "Post name"

---

## Creating Pages

### Step 1: Create All 5 Pages First

Go to **Pages → Add New Page** and create these pages (just the titles for now):

1. **Home**
2. **About**
3. **Services**
4. **Career Resources** (this will become the Posts listing page)
5. **Contact**

For the "Career Resources" page, just create it with the title only — don't add content. This page will automatically display your blog posts.

### Step 2: Set the Homepage and Posts Page

1. Go to **Settings → Reading**
2. Select **"A static page"**
3. **Homepage:** Select "Home"
4. **Posts page:** Select "Career Resources"
5. Click **Save Changes**

### Step 3: Create the Navigation Menu

1. Go to **Appearance → Menus** (or Appearance → Customize → Menus)
2. Click **"Create a new menu"**
3. Name it **"Primary Navigation"**
4. Add all 5 pages in this order: Home, About, Services, Career Resources, Contact
5. Check **"Primary"** under Menu Locations
6. Click **Save Menu**

---

## Building Each Page

Open each page by going to **Pages → All Pages → click the page title → Edit**.

### Building the Home Page

Reference: `content/pages/home.md` for all copy.

#### Hero Section

1. Click **"+"** to add a block → search **"Row Layout"** (Kadence)
2. Choose a **1-column layout**
3. In Row Layout settings (right panel):
   - Background Color: `#1B2A4A` (navy)
   - Padding: 80px top, 80px bottom (desktop); 48px on mobile
   - Max Width: Full Width
   - Inner Max Width: 1200px
   - Content Alignment: Center
4. Inside the row, add:
   - **Heading block (H1):** "Navigate Your Career with Confidence"
     - Color: `#F5F5F0` (off-white)
     - Alignment: Center
   - **Paragraph block:** Add the hero description text
     - Color: `#F5F5F0`
     - Alignment: Center
     - Max width: 700px (use the block width settings)
   - **Advanced Button block (Kadence):**
     - Text: "Explore Our Services"
     - Link: `/services`
     - Background: `#2A9D8F` (teal)
     - Text color: `#FFFFFF`
     - Border radius: 4px
     - Alignment: Center

#### Services Overview Section

1. Add another **Row Layout** block below the hero
2. Choose a **3-column layout** (equal widths)
3. Row settings:
   - Background: `#FAF7F2` (cream) or `#F0EDE8` (light gray)
   - Padding: 60px top/bottom
4. Before the columns, add:
   - **Heading (H2):** "What We Offer" — centered
   - **Paragraph:** Brief intro — centered
5. In **each column**, add:
   - **Heading (H3):** Service name (e.g., "Resume Review")
   - **Paragraph:** 2-sentence description
   - **Button:** "Learn More →" linking to `/services`
6. Style each column as a card:
   - Background: White (`#FFFFFF`)
   - Padding: 32px
   - Border radius: 8px
   - Border top: use a Separator block or Kadence's border settings with `#2A9D8F` (teal)

#### Resource Library Preview Section

1. Add another **Row Layout** block
2. Choose **3-column layout**
3. Add heading: "From Our Resource Library"
4. Add intro paragraph
5. Option A: Use a **Latest Posts** block (WordPress core) — set to show 3 posts, display excerpt
6. Option B: Manually create 3 cards linking to your resource posts
7. Style with consistent card appearance

#### Call to Action Section

1. Add a **Row Layout** block
2. Set to **1-column, full width**
3. Background: `#1B2A4A` (navy)
4. Padding: 60px top/bottom
5. Add centered **Heading (H2):** "Ready to Take the Next Step?"
6. Add centered **Paragraph** with supporting text
7. Add **Advanced Button:** "Get in Touch" → link to `/contact`
   - Background: `#2A9D8F` (teal), text: white

---

### Building the About Page

Reference: `content/pages/about.md`

1. **Heading (H1):** "About ClearPath"
2. **Paragraph:** Intro text
3. **Heading (H2):** "Our Mission" + paragraphs
4. **Heading (H2):** "Who We Help" + paragraph + List block
5. **Row Layout (3-column)** for "Our Approach":
   - Background: `#F0EDE8`
   - 3 columns: "Practical First" / "Accessible to Everyone" / "Honest and Realistic"
   - Each with H3 + paragraph
6. **Paragraph (italic):** Portfolio project disclaimer

---

### Building the Services Page

Reference: `content/pages/services.md`

1. **Heading (H1):** "Our Services" + intro paragraph
2. For each service, use a **Row Layout (1 or 2 column)**:
   - White background with teal top border
   - **Heading (H2):** Service name with emoji
   - **Paragraph:** Description
   - **List block:** "What's Included" items
   - **Advanced Button:** "Contact Us" → `/contact`
3. **Navy CTA section** at the bottom (same pattern as Home)
4. **Italic disclaimer** paragraph

---

### Building the Contact Page

Reference: `content/pages/contact.md`

1. **Heading (H1):** "Get in Touch" + intro paragraph
2. **WPForms block:**
   - First, create the form in WPForms → Add New (see contact.md for field details)
   - Then add a WPForms block on the page and select your form
3. **Row Layout** with light gray background:
   - **Heading (H3):** "Other Ways to Reach Us"
   - **Paragraph:** Sample email address + email delivery note
4. **Italic paragraph:** Technical note about form delivery

---

## Creating Resource Posts (Career Resource Library)

### Step 1: Create Categories

1. Go to **Posts → Categories**
2. Create two categories:

| Name | Slug | Description |
|------|------|-------------|
| Guides & Templates | `guides-templates` | Checklists, templates, and how-to articles for job seekers |
| Interview & Job Search | `interview-job-search` | Interview prep, networking advice, and job search strategies |

### Step 2: Create Each Post

For each resource article, go to **Posts → Add New Post**:

1. **Set the title** (from the content file)
2. **Paste the content** from the corresponding markdown file in `content/posts/`
3. **Set the Category** (right panel → Categories)
4. **Add Tags** (right panel → Tags — type each tag and press Enter)
5. **Write the Excerpt** (right panel → Excerpt — copy from the content file)
6. **Set a Featured Image** (optional — you can upload a simple image or skip for now)
7. Click **Publish**

### Post List:

| # | Title | Category | Tags |
|---|-------|----------|------|
| 1 | Resume Checklist: 10 Things to Verify Before Submitting | Guides & Templates | resume, checklist, entry-level |
| 2 | 15 Common Interview Questions and How to Approach Them | Interview & Job Search | interview, preparation, tips |
| 3 | Job Application Tracking Guide | Guides & Templates | job-search, organization, tracking |
| 4 | How to Write a Cover Letter That Gets Read | Guides & Templates | cover-letter, writing, entry-level |
| 5 | Networking for Introverts: A Practical Guide | Interview & Job Search | networking, career, tips |

### Step 3: Configure Blog Layout

1. Go to **Appearance → Customize → Posts / Blog → Blog Layout**
2. Set the archive/blog layout:
   - Layout: Grid (2 or 3 columns)
   - Show: Title, Excerpt, Categories, Date
   - Post content: Excerpt
3. Click **Publish**

---

## Setting Up the Footer Content

1. Go to **Appearance → Widgets** or **Appearance → Customize → Footer**
2. Kadence footer has widget areas. Add content to the 3 columns:

**Column 1:**
- Add a **Paragraph** widget: "ClearPath — Career guidance for students and fresh graduates. Practical resources and personalized support to help you take confident first steps."

**Column 2:**
- Add a **Navigation Menu** widget
- Title: "Quick Links"
- Select the Primary Navigation menu

**Column 3:**
- Add a **Paragraph** widget
- Title: "Get in Touch"
- Content: "contact@clearpath-careers.com (sample — not monitored)"

---

## Final Verification

After building all pages, check:

- [ ] Home page loads as the front page (not the blog listing)
- [ ] Career Resources page shows your 5 posts
- [ ] All navigation links work
- [ ] All buttons link to correct pages
- [ ] Footer displays correctly with 3 columns
- [ ] Mobile view: hamburger menu works, cards stack to 1 column
- [ ] Contact form displays and can be submitted (check confirmation message)
- [ ] Categories and tags display on posts
- [ ] No placeholder or "Lorem ipsum" text remains
