# ClearPath — WordPress Setup Guide (Linux)

This guide walks you through setting up the ClearPath WordPress site on your local Linux machine using **LocalWP**, installing the **Kadence** theme, and configuring the 3 required plugins.

---

## Part 1: Install LocalWP on Linux

### Step 1: Download LocalWP

1. Open your browser and go to **[localwp.com](https://localwp.com/)**
2. Click **"Download for Free"**
3. Fill in the form (name and email — you can use any email)
4. Select **Linux** as your platform
5. Download the `.deb` file

### Step 2: Install LocalWP

Open a terminal and run:

```bash
# Navigate to your Downloads folder
cd ~/Downloads

# Install the .deb package
sudo dpkg -i local-*-linux.deb

# If there are dependency errors, fix them with:
sudo apt-get install -f
```

### Step 3: Launch LocalWP

- Find **Local** in your application menu, or run `local` from the terminal
- On first launch, it may ask you to agree to terms and set up
- Click through the setup — no special configuration needed

> **Troubleshooting:** If LocalWP doesn't start, ensure you have these dependencies:
> ```bash
> sudo apt-get install libnss3 libatk1.0-0 libatk-bridge2.0-0 libcups2 libxcomposite1 libxrandr2 libgbm1 libpango-1.0-0 libcairo2
> ```

---

## Part 2: Create the ClearPath Site

### Step 1: Create a New Site

1. Open LocalWP
2. Click the green **"+ Create a new site"** button
3. Select **"Create a new site"** (not from Blueprint)
4. Click **Continue**

### Step 2: Name Your Site

- **Site name:** `ClearPath`
- LocalWP will automatically set the domain to `clearpath.local`
- Click **Continue**

### Step 3: Choose Environment

- Select **"Preferred"** (this uses the latest stable PHP and MySQL)
- The "Custom" option is not needed for this project
- Click **Continue**

### Step 4: Set Admin Credentials

| Field | Value |
|-------|-------|
| WordPress Username | `admin` |
| WordPress Password | Choose a strong password you'll remember |
| WordPress Email | `admin@clearpath.local` (or any email) |

- Click **"Add Site"**
- Wait for LocalWP to set up WordPress (takes 1–2 minutes)

### Step 5: Access Your Site

Once setup is complete, you'll see the ClearPath site in LocalWP. Two important buttons:

- **"Open Site"** — Opens the frontend: `http://clearpath.local`
- **"Admin"** — Opens the WordPress dashboard: `http://clearpath.local/wp-admin`

> **Note:** You may need to click **"Trust"** to set up the local SSL certificate. This is optional for local development.

---

## Part 3: Install the Kadence Theme

### Step 1: Access the Theme Installer

1. Click **"Admin"** in LocalWP to open the WordPress dashboard
2. Log in with your admin credentials
3. Go to **Appearance → Themes**
4. Click **"Add New Theme"** (button at the top)

### Step 2: Install Kadence

1. In the search box, type **"Kadence"**
2. Find the theme by **Starter Templates** (formerly Kadence WP)
3. Click **"Install"**
4. After installation, click **"Activate"**

### Step 3: Skip the Setup Wizard (for now)

Kadence may show a setup wizard. You can **skip it** — we'll configure everything manually to understand each setting.

---

## Part 4: Install the 3 Plugins

### Navigate to Plugins

1. In the WordPress dashboard, go to **Plugins → Add New Plugin**

### Install Each Plugin

For each plugin below, search by name, click **"Install Now"**, then click **"Activate"**:

| # | Plugin Name | Search Term | Author |
|---|-------------|-------------|--------|
| 1 | **Kadence Blocks** | Kadence Blocks | Starter Templates | 
| 2 | **WPForms Lite** | WPForms | WPForms |
| 3 | **All-in-One WP Migration** | All-in-One WP Migration | ServMask |

After installing all three, go to **Plugins → Installed Plugins** to verify all 3 are active.

---

## Part 5: Configure Basic WordPress Settings

### 5.1 General Settings

Go to **Settings → General**:

| Setting | Value |
|---------|-------|
| Site Title | `ClearPath` |
| Tagline | `Career Guidance for Students and Fresh Graduates` |
| Timezone | Select your timezone (e.g., `Asia/Kolkata` for IST) |

Click **"Save Changes"**.

### 5.2 Permalink Settings

Go to **Settings → Permalinks**:

1. Select **"Post name"** (this creates clean URLs like `/about`, `/services`)
2. Click **"Save Changes"**

This is critical — it ensures your URLs are readable and SEO-friendly.

### 5.3 Reading Settings (do this after creating pages)

We'll come back to this after creating the Home page and Resources page. The settings will be:

| Setting | Value |
|---------|-------|
| Your homepage displays | **A static page** |
| Homepage | Home (after creating it) |
| Posts page | Career Resources (after creating it) |

### 5.4 Discussion Settings

Go to **Settings → Discussion**:

- Uncheck **"Allow people to submit comments on new posts"** (we don't need blog comments for this project)
- Click **"Save Changes"**

### 5.5 Delete Default Content

WordPress creates sample content on install. Delete it:

1. **Pages → All Pages:** Delete "Sample Page" and "Privacy Policy" (you can recreate Privacy Policy later if needed)
2. **Posts → All Posts:** Delete "Hello world!" post
3. Empty the **Trash** for both Pages and Posts

---

## Part 6: Configure the Kadence Theme

### 6.1 Set the Color Palette

1. Go to **Appearance → Customize**
2. Click **Colors & Fonts → Colors**
3. You'll see 9 color circles. Click each one and enter these hex values:

| Slot | Hex Code | Role |
|------|----------|------|
| Accent 1 | `#1B2A4A` | Navy (primary) |
| Accent 2 | `#2A9D8F` | Teal (accent) |
| Contrast 1 | `#2C2C2C` | Charcoal (body text) |
| Contrast 2 | `#5A6270` | Slate (subtitles) |
| Contrast 3 | `#D1CEC9` | Light gray (borders) |
| Base 1 | `#FAF7F2` | Warm cream (background) |
| Base 2 | `#FFFFFF` | White (cards) |
| Base 3 | `#F0EDE8` | Light warm gray (alt sections) |

4. Click **Publish** (top of the Customizer)

### 6.2 Set Typography

1. Still in the Customizer, go to **Colors & Fonts → Typography**
2. **Base Font (Body):**
   - Family: **Inter** (search in the Google Fonts dropdown)
   - Size: 16px (or 1rem)
   - Weight: Regular (400)
   - Line Height: 1.7
3. **Heading Font:**
   - Family: **Inter**
   - H1: Size 40px, Weight 700, Line Height 1.2
   - H2: Size 32px, Weight 700, Line Height 1.3
   - H3: Size 24px, Weight 600, Line Height 1.4
4. Click **Publish**

### 6.3 Configure the Header

1. In the Customizer, go to **Header**
2. Kadence shows a visual header builder at the bottom of the screen
3. **Top Row:** Leave empty or remove
4. **Main Row:**
   - **Left side:** Drag the **"Logo"** element here
   - **Right side:** Drag the **"Primary Navigation"** element here
5. Click on the **Logo** element:
   - Choose **"Site Title"** (not image logo)
   - The site title "ClearPath" will display using your theme fonts
6. Click on **Main Row settings** (the row itself):
   - Background: White (`#FFFFFF`)
   - Height: 80px
7. Click **Publish**

> **Note:** We'll set up the navigation menu after creating the pages.

### 6.4 Configure the Footer

1. In the Customizer, go to **Footer**
2. **Top Row (Widget Area):**
   - Set to 3 columns
   - Background: `#1B2A4A` (navy)
   - We'll add content to footer widgets after creating pages
3. **Bottom Row:**
   - Add a **"Copyright"** element
   - Edit the copyright text to: `© {year} ClearPath. This is a sample portfolio project.`
   - Background: `#1B2A4A` (navy)
   - Text color: `#F5F5F0` (off-white)
4. Click **Publish**

### 6.5 Set Layout Defaults

1. In the Customizer, go to **General → Layout**
2. Set **Content Max Width:** 1200px
3. Go to **General → Buttons**
4. Set button border radius: 4px
5. Set button colors:
   - Background: `#1B2A4A` (navy)
   - Text: `#FFFFFF` (white)
   - Hover Background: `#2D4A7A` (lighter navy)
   - Hover Text: `#FFFFFF`
6. Click **Publish**

---

## ✅ Phase 2 Checklist

After completing this guide, verify:

- [ ] LocalWP is installed and running on your Linux machine
- [ ] ClearPath site is created and accessible at `clearpath.local`
- [ ] You can log into the WordPress admin at `clearpath.local/wp-admin`
- [ ] Kadence theme is installed and activated
- [ ] Kadence Blocks plugin is installed and activated
- [ ] WPForms Lite plugin is installed and activated
- [ ] All-in-One WP Migration plugin is installed and activated
- [ ] Colors are set: navy, teal, cream palette in the Customizer
- [ ] Fonts are set: Inter for body and headings
- [ ] Permalinks are set to "Post name"
- [ ] Default sample content (Hello World post, Sample Page) is deleted
- [ ] Header shows "ClearPath" text logo with navigation area
- [ ] Footer has navy background with copyright text

Once all items are checked, proceed to **Phase 3: Website Content Creation** using the `gutenberg-building-guide.md`.
