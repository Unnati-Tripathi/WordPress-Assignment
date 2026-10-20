# ClearPath — CMS Demonstration Guide

This guide explains how to demonstrate real WordPress CMS skills using the ClearPath website. Each section maps to a skill you should be able to show and explain in an interview.

---

## 1. Creating and Publishing Content

### Create a New Page

1. Go to **Pages → Add New Page**
2. Enter a title
3. Add content using Gutenberg blocks (paragraphs, headings, images, buttons)
4. Click **"Preview"** (top right) to see how it looks before publishing
5. Click **"Publish"** when ready
6. Click **"View Page"** to see the live version

**Interview talking point:** "WordPress uses a block-based editor called Gutenberg. Each piece of content — a paragraph, heading, image, or button — is a separate block that I can add, move, and configure independently."

### Create a New Post

1. Go to **Posts → Add New Post**
2. Enter a title
3. Add content
4. In the right panel, set the **Category** and **Tags**
5. Write an **Excerpt** (short summary shown on listing pages)
6. Click **Publish**

**Key difference to explain:** "Pages are for static content like the About page. Posts are for dynamic content like articles — they have dates, categories, and tags, and they appear in reverse chronological order on the blog/resources page."

### Edit Existing Content

1. Go to **Pages → All Pages** (or **Posts → All Posts**)
2. Hover over the item → click **"Edit"**
3. Make changes in the block editor
4. Click **"Preview"** to check → **"Update"** to save

### Update a Service Description (Without Code)

This demonstrates content management:

1. Go to **Pages → All Pages → Services → Edit**
2. Find the service card you want to update
3. Click on the text block and make changes
4. Click **Update**

**Interview talking point:** "The client can update service descriptions, pricing, and details directly through the WordPress dashboard without needing a developer. That's the power of a CMS."

---

## 2. Organizing Content with Categories and Tags

### View Categories

1. Go to **Posts → Categories**
2. You'll see: "Guides & Templates" and "Interview & Job Search"

### Add a New Category

1. Enter the category name (e.g., "Career News")
2. Add a slug (e.g., `career-news`)
3. Optionally add a description
4. Click **"Add New Category"**

### Add Tags to a Post

1. Edit any post
2. In the right panel, find **Tags**
3. Type a tag name and press **Enter**
4. Tags are created on the fly — no need to pre-define them

**Interview talking point:** "Categories are broad groupings — like folders. Tags are specific cross-cutting topics — like labels. A resume checklist post is in the 'Guides & Templates' category but tagged with 'resume', 'checklist', and 'entry-level'. This makes content easier to organize and find."

---

## 3. Media Management

### Upload an Image

1. Go to **Media → Add New Media File**
2. Drag and drop an image, or click **"Select Files"**
3. After upload, click the image to edit metadata:
   - **Title:** Descriptive name
   - **Alt Text:** Description for accessibility (important for screen readers and SEO)
   - **Caption:** Optional visible caption

### Add an Image to a Page

1. Edit any page in Gutenberg
2. Click **"+"** → search **"Image"**
3. Upload or select from the Media Library
4. Set alt text and alignment

### Replace an Image

1. Edit the page containing the image
2. Click on the image block
3. Click **"Replace"** in the block toolbar
4. Upload a new image or select from the Media Library

**Interview talking point:** "WordPress has a built-in Media Library for managing all uploaded files. I always add descriptive alt text to images for accessibility and SEO — screen readers use alt text to describe images to visually impaired users."

---

## 4. Navigation Menu Management

### Edit the Menu

1. Go to **Appearance → Menus**
2. Select "Primary Navigation"
3. To **add a page:** Check the page in the left panel → click "Add to Menu"
4. To **reorder:** Drag menu items up or down
5. To **remove:** Expand the item → click "Remove"
6. Click **"Save Menu"**

### Create a Sub-Menu

1. Drag a menu item slightly **to the right** (indented under another item)
2. It becomes a dropdown sub-item
3. Save the menu

**Interview talking point:** "Navigation menus in WordPress are managed through the admin dashboard. I can add, remove, and reorder menu items without touching any code. Kadence theme also provides a visual header builder for more control."

---

## 5. Homepage and Blog Page Configuration

### Change What the Homepage Displays

1. Go to **Settings → Reading**
2. **"Your homepage displays"** — choose between:
   - **Your latest posts:** The homepage shows blog posts (default WordPress behavior)
   - **A static page:** The homepage shows a specific page (what we're using)
3. When "A static page" is selected:
   - **Homepage:** The page to show as the front page
   - **Posts page:** The page where blog posts are listed

**Interview talking point:** "By default, WordPress shows blog posts on the homepage. For a business website, I configured it to use a static page as the homepage and set a separate page for the career resources blog. This is a standard WordPress setting under Settings → Reading."

---

## 6. Managing the Contact Form

### View Form Settings

1. Go to **WPForms → All Forms**
2. Click on **"ClearPath Contact Form"**
3. Review the fields, notifications, and confirmation settings

### Edit Form Fields

1. In the form editor, click any field to edit its label, placeholder, or validation
2. Drag fields to reorder
3. Click **Save**

### Test the Form

1. Visit the Contact page on the frontend
2. Fill out all fields
3. Click Submit
4. Verify the confirmation message appears

**Interview talking point:** "I used WPForms Lite for the contact form because it's beginner-friendly and doesn't require code. I configured the form fields, set up a confirmation message, and tested the submission process. On free hosting, email delivery is unreliable, so in production I'd add an SMTP plugin to ensure messages reach the inbox."

---

## 7. Preview Before Publishing

### Preview a Draft

1. Edit any page or post
2. Make changes
3. Click **"Preview"** → choose Desktop, Tablet, or Mobile preview
4. The preview opens in a new tab — it's not visible to the public
5. If satisfied, click **"Update"** (or "Publish" for new content)

### Schedule a Post

1. Edit a post
2. In the right panel, click the **"Publish"** date
3. Set a future date and time
4. Click **"Schedule"** instead of "Publish"
5. The post will go live automatically at the scheduled time

**Interview talking point:** "WordPress lets me preview content changes before they go live, and schedule posts for future publication. This is important for content management — you can review everything before your audience sees it."

---

## Demonstration Checklist

Use this checklist to practice demonstrating CMS skills:

- [ ] Create a new draft post with a title, body, category, tags, and excerpt
- [ ] Preview the draft on desktop and mobile
- [ ] Publish the post and verify it appears on the Career Resources page
- [ ] Edit an existing service description on the Services page
- [ ] Upload an image to the Media Library with proper alt text
- [ ] Add the image to a page
- [ ] Replace an image on a page
- [ ] Add a new item to the navigation menu
- [ ] Reorder navigation menu items
- [ ] Change the homepage setting from static to latest posts (then change it back)
- [ ] Submit the contact form and verify the confirmation message
- [ ] View WPForms settings and explain the notification setup
- [ ] Add a new category and assign a post to it
- [ ] Add tags to an existing post
