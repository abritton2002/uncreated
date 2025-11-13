# Uncreated Minimal Drop Site

A stark, spiritual minimalism theme for product drops — inspired by YEEZY Supply and DONDA aesthetics.

## What Was Built

### New Sections
1. **`sections/uncreated-hero-minimal.liquid`**
   - Fullscreen hero with large typography
   - Brand name + slogan
   - Smooth scroll CTA button
   - Customizable in theme editor

2. **`sections/uncreated-product-minimal.liquid`**
   - Single product display
   - Size selector with minimal pill buttons
   - Add to cart functionality
   - Product description
   - Choose product in theme settings

3. **`sections/uncreated-footer-minimal.liquid`**
   - Social media links
   - Copyright
   - Tagline
   - Centered minimal layout

### Styling
- **`assets/uncreated-minimal.css`** - All custom CSS for the drop aesthetic
  - EB Garamond display font
  - Inter body font
  - Off-white (#f5f5f0) background
  - Near-black (#0a0a0a) text
  - Smooth animations
  - Fully responsive

### Modified Files
- **`templates/index.json`** - Homepage now uses minimal sections
  - Old sections preserved with `_ARCHIVED_` prefix
  - Can be re-enabled anytime

## How to Use

### Setup in Shopify Theme Editor

1. **Go to Shopify Admin → Online Store → Themes**
2. **Click "Customize" on your theme**
3. **On the Homepage:**
   - You'll see 3 sections: Hero, Product, Footer
   - Configure each section in the left sidebar

### Configure Product Section

1. Click on **"Uncreated Product (Minimal)"** section
2. **Select a product** from the dropdown
3. Customize:
   - Button text (default: "ADD TO BAG")
   - Limited edition badge
   - Product description visibility
   - Colors and padding

### Customize Hero

1. Click on **"Uncreated Hero (Minimal)"** section
2. Edit:
   - Brand name (default: "UNCREATED")
   - Title size (60-200px)
   - Subtitle text
   - CTA button text
   - Background color
   - Optional background image

### Customize Footer

1. Click on **"Uncreated Footer (Minimal)"** section
2. Add/edit social links:
   - Click "Add block" → "Social Link"
   - Set label (e.g., "@uncreated")
   - Set URL (e.g., your Instagram)
3. Edit copyright text and tagline

## Header Behavior

On the homepage, the header automatically becomes minimal:
- ✅ Logo centered
- ✅ Cart icon visible
- ❌ Navigation menu hidden
- ❌ Search hidden
- ❌ Announcement bar hidden

On other pages (product, collection, cart), the header remains normal with full navigation.

## Deployment to GitHub + Shopify

### Initial Setup

1. **Initialize Git repo** (if not already):
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Uncreated minimal drop theme"
   ```

2. **Create GitHub repo**:
   - Go to GitHub.com
   - Create new repository named "uncreated"
   - Don't initialize with README (you already have code)

3. **Push to GitHub**:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/uncreated.git
   git branch -M main
   git push -u origin main
   ```

### Connect GitHub to Shopify

1. **In Shopify Admin**:
   - Go to **Online Store → Themes**
   - Click **Add theme → Connect from GitHub**

2. **Select Repository**:
   - Choose your organization/account
   - Select the "uncreated" repository
   - Select the branch (usually `main`)

3. **Theme will appear** in your theme library connected to GitHub

### Auto-Sync Workflow

Once connected:
- ✅ **GitHub → Shopify**: Every push syncs automatically
- ✅ **Shopify → GitHub**: Edits in theme editor commit to GitHub
- ✅ **Two-way sync**: Always in sync

### Making Changes

**Option A: Edit in Shopify Theme Editor**
1. Customize → Make changes
2. Save
3. Changes automatically commit to GitHub

**Option B: Edit Code Locally**
1. Make changes to files locally
2. Commit and push:
   ```bash
   git add .
   git commit -m "Update product section styling"
   git push
   ```
3. Shopify theme updates automatically

## Restore Old Homepage

If you want to go back to the original store homepage:

1. **In Shopify Theme Editor**
2. **On Homepage template**
3. **Click "Add section"** at the bottom
4. **Scroll down** to find archived sections (they're still there, just hidden)
5. **Rearrange sections** to bring back old layout
6. **Remove minimal sections** if desired

All original sections are preserved in `templates/index.json` with the `_ARCHIVED_` prefix.

## Customization Tips

### Change Color Scheme to Dark Mode

In each section settings:
- Background Color: `#0a0a0a` (dark)
- Text Color: `#f5f5f0` (light)

### Add Product Images

1. In Shopify Admin → Products
2. Upload high-quality images to your product
3. The minimal product section automatically displays the featured image

### Typography Adjustments

Edit `assets/uncreated-minimal.css`:
- Line 13-14: Change font families
- Search for `font-size` to adjust sizes globally

### Animation Speed

Edit `assets/uncreated-minimal.css`:
- Line 17: `--transition-smooth` controls hover transitions
- Lines 395-424: Animation keyframes and durations

## File Structure

```
uncreated/
├── sections/
│   ├── uncreated-hero-minimal.liquid      [New - Hero section]
│   ├── uncreated-product-minimal.liquid   [New - Product section]
│   ├── uncreated-footer-minimal.liquid    [New - Footer section]
│   └── [all original Dawn sections...]
│
├── assets/
│   ├── uncreated-minimal.css              [New - All custom styles]
│   └── [all original Dawn assets...]
│
├── templates/
│   ├── index.json                         [Modified - Uses minimal sections]
│   └── [all other templates unchanged...]
│
└── [all other Dawn files unchanged...]
```

## Support

### Common Issues

**Problem**: Product section shows "Please select a product"
- **Solution**: Go to theme editor → Product section → Select a product

**Problem**: Header still shows menu
- **Solution**: Clear browser cache, `uncreated-minimal.css` might not be loaded

**Problem**: Colors don't match
- **Solution**: Check section settings for background/text colors

**Problem**: Theme not syncing from GitHub
- **Solution**: Check Shopify theme card for sync errors, click "View logs"

### Testing Before Publishing

1. Connected theme appears as **unpublished** in theme library
2. Click **Preview** to test without affecting live site
3. When ready, click **Publish** to make it live

## Brand Assets

- Logo: `BlackNoBack.png`
- Favicon: `Uncreated_Curve_Logo_Black_2.png`
- Instagram: @uncreated.shop
- TikTok: @uncreated.shop

---

**Built with:** Shopify Dawn + Custom Minimal Sections
**Aesthetic:** Stark spiritual minimalism
**Slogan:** "Created by the Uncreated One"
