# ClearPath — Deployment Guide (InfinityFree + Linux)

Step-by-step guide to deploy ClearPath from LocalWP to InfinityFree free hosting with a free subdomain and HTTPS.

---

## Part 1: Sign Up for InfinityFree

1. Go to **[infinityfree.com](https://www.infinityfree.com/)**
2. Click **"Sign Up"** and create a free account
3. Verify your email address

## Part 2: Create a Hosting Account

1. After logging in, click **"Create Account"** on the dashboard
2. **Choose a subdomain:**
   - Select the free subdomain option
   - Type your desired name, e.g., `clearpath`
   - Choose from available domains (e.g., `.infinityfree.com`, `.rf.gd`, `.epizy.com`)
   - Your site URL will be something like: `clearpath.rf.gd`
3. Set your account password (this is for the hosting control panel, not WordPress)
4. Click **"Create"**
5. Wait for the account to be activated (usually instant, sometimes up to 24 hours)

## Part 3: Install WordPress on InfinityFree

### Option A: Softaculous (Recommended)

1. In your InfinityFree account, click **"Control Panel"**
2. Find and click **"Softaculous Apps Installer"**
3. Find **WordPress** in the list and click **"Install"**
4. Configure the installation:

| Setting | Value |
|---------|-------|
| Choose Protocol | `https://` |
| Choose Domain | Your subdomain (e.g., `clearpath.rf.gd`) |
| In Directory | Leave **empty** (installs at root) |
| Site Name | ClearPath |
| Site Description | Career Guidance for Students and Fresh Graduates |
| Admin Username | `admin` (or choose your own) |
| Admin Password | A **strong** password (different from your hosting password) |
| Admin Email | Your real email |
| Language | English |

5. Click **"Install"**
6. Once complete, note down:
   - Site URL: `https://clearpath.rf.gd`
   - Admin URL: `https://clearpath.rf.gd/wp-admin`
   - Admin credentials

### Option B: Manual Installation

If Softaculous is unavailable:

1. **Create a database:** In the control panel, go to MySQL Databases → Create Database. Note the database name, username, and password.
2. **Download WordPress:** Go to [wordpress.org/download](https://wordpress.org/download/) and download the latest ZIP.
3. **Upload files:** Use the control panel's File Manager or an FTP client (like FileZilla) to upload and extract WordPress files to the `htdocs/` directory.
4. **Run the installer:** Visit your subdomain URL in a browser and follow the WordPress setup wizard. Enter your database credentials when prompted.

## Part 4: Prepare the Local Site for Migration

On your **LocalWP** site:

### Step 1: Clean Up

1. Log into `clearpath.local/wp-admin`
2. Delete any draft/test content you don't want migrated
3. Go to **Settings → Reading** → Uncheck "Discourage search engines from indexing this site" (if checked)

### Step 2: Export with All-in-One WP Migration

1. Go to **All-in-One WP Migration → Export**
2. Click **"Export To" → File**
3. Wait for the export to complete
4. Click **"Download"** to save the `.wpress` file to your computer
5. Note the file size — InfinityFree's free import limit should handle files under ~200MB

## Part 5: Import to InfinityFree

### Step 1: Install the Migration Plugin on the Live Site

1. Log into your InfinityFree WordPress admin: `https://clearpath.rf.gd/wp-admin`
2. Go to **Plugins → Add New Plugin**
3. Search for **"All-in-One WP Migration"**
4. Click **Install Now → Activate**

### Step 2: Import Your Site

1. Go to **All-in-One WP Migration → Import**
2. Click **"Import From" → File**
3. Select the `.wpress` file you downloaded earlier
4. Wait for the upload and import to complete
5. When prompted, click **"Proceed"** to confirm the import
6. The plugin will replace all content, themes, plugins, and update all URLs automatically

### Step 3: Re-Save Permalinks

This is **critical** — skip it and your pages will show 404 errors:

1. Go to **Settings → Permalinks**
2. Make sure **"Post name"** is selected
3. Click **"Save Changes"** (even if nothing visibly changed)

### Step 4: Log In Again

After import, your login credentials will be the ones from your **local site** (not the ones you set on InfinityFree). Log in with the LocalWP admin username and password.

## Part 6: Configure Production Settings

### 6.1 Verify Site URLs

1. Go to **Settings → General**
2. Verify both URLs use `https://`:
   - WordPress Address (URL): `https://clearpath.rf.gd`
   - Site Address (URL): `https://clearpath.rf.gd`
3. Click **Save Changes**

### 6.2 Enable HTTPS / SSL

1. In the InfinityFree control panel, find **"Free SSL Certificates"** or **"SSL/TLS"**
2. Click to activate Let's Encrypt SSL for your subdomain
3. Wait for the certificate to be issued (can take a few hours)
4. Once active, verify your site loads with `https://` and shows a padlock icon

### 6.3 Force HTTPS (if needed)

If your site still loads on `http://`, add this to your `.htaccess` file (via File Manager in the control panel):

```apache
# Force HTTPS
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

### 6.4 Update WordPress Admin Password

1. Go to **Users → Your Profile**
2. Scroll to **"Set New Password"**
3. Generate or enter a strong password
4. Click **"Update Profile"**

## Part 7: Post-Deployment Verification Checklist

Test everything on the live site:

### Pages & Content
- [ ] Home page loads correctly with hero, services, resources, and CTA sections
- [ ] About page displays all sections
- [ ] Services page shows all 3 service cards
- [ ] Career Resources page lists all 5 posts
- [ ] Contact page shows the form
- [ ] Each resource post opens and displays correctly
- [ ] No "Lorem ipsum" or placeholder text

### Navigation & Links
- [ ] Header navigation works on all pages
- [ ] All buttons link to correct pages
- [ ] Footer links work
- [ ] No links point to `clearpath.local` or `localhost`

### Images & Media
- [ ] All images load (no broken image icons)
- [ ] Images are not oversized (check page load time)

### Forms
- [ ] Contact form displays correctly
- [ ] Form can be submitted (fills out and shows confirmation)
- [ ] Note: Email delivery may not work — this is expected on free hosting

### Mobile & Responsive
- [ ] Site looks correct on mobile (use browser DevTools → Toggle Device Toolbar, or test on a phone)
- [ ] Hamburger menu works on mobile
- [ ] Cards stack to single column on small screens
- [ ] Text is readable without horizontal scrolling

### Security & Technical
- [ ] Site loads with `https://` (padlock icon in browser)
- [ ] No mixed-content warnings in browser console (F12 → Console)
- [ ] Permalinks work (pages don't show 404 errors)

## Part 8: Troubleshooting Common Issues

### "404 Not Found" on pages
**Fix:** Go to Settings → Permalinks → click Save Changes. This regenerates the `.htaccess` file.

### Images not loading
**Fix:** Check if image URLs still reference `clearpath.local`. The migration plugin should handle this, but if not:
1. Install the **Better Search Replace** plugin
2. Search for `clearpath.local` → Replace with `clearpath.rf.gd`
3. Run on all tables

### Mixed content warnings
**Fix:** Some resources load via `http://` instead of `https://`. Use Better Search Replace:
- Search: `http://clearpath.rf.gd`
- Replace: `https://clearpath.rf.gd`

### Import fails (file too large)
**Fix:** InfinityFree may restrict upload sizes. Try:
1. In the control panel, check the PHP upload limit (increase if possible)
2. Use the All-in-One WP Migration extension for larger files
3. Or use File Manager to upload the `.wpress` file to `wp-content/ai1wm-backups/` and import from there

### Contact form emails not arriving
**Expected behavior on free hosting.** Document this honestly. In a real deployment, add WP Mail SMTP plugin with Gmail or SendGrid.

## Part 9: Backups

### Creating a Backup
1. Log into your live WordPress admin
2. Go to **All-in-One WP Migration → Export → File**
3. Download the `.wpress` file
4. Store it safely (Google Drive, local backup folder)

### When to Back Up
- **Before** updating WordPress core, theme, or plugins
- **Before** making major content changes
- **Weekly** if you're actively updating the site
- **Before** deployment or migration

### Updating WordPress Safely
1. Back up first (export `.wpress` file)
2. Update **plugins** first (one at a time, test after each)
3. Update the **theme** next (test after)
4. Update **WordPress core** last (test after)
5. If anything breaks, restore from your backup using All-in-One WP Migration → Import

---

## Quick Reference

| What | Where |
|------|-------|
| Live site | `https://clearpath.rf.gd` (your actual subdomain) |
| Admin panel | `https://clearpath.rf.gd/wp-admin` |
| Hosting control panel | InfinityFree dashboard |
| Backups | All-in-One WP Migration → Export |
| SSL certificate | InfinityFree control panel → SSL |
