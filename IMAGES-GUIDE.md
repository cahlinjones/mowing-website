# Image & Video Guide for My Robot Mowers Website

## How to Add Your Images and Videos

### 1. Hero Background Image

**Location:** Homepage hero section
**File:** `index.html` and `css/style.css`

**Steps:**
1. Add your hero background image to the `images/` folder (e.g., `hero-bg.jpg`)
2. Open `css/style.css`
3. Find the `.hero-background` section (around line 580)
4. Change this line:
   ```css
   background-image: none;
   ```
   To:
   ```css
   background-image: url('images/hero-bg.jpg');
   ```

**Recommended specs:**
- Size: 1920x1080px or larger
- Format: JPG (for photos)
- File size: Under 500KB (optimize for web)
- Subject: Lawn or yard with good lighting

---

### 2. Product Images & YouTube Videos

**Location:** Homepage product section
**Files to edit:** `index.html`

#### Snow Blower (Featured Product)

**Search for:** `<!-- REPLACE WITH YOUR SNOW BLOWER IMAGE -->`

**Steps:**
1. Add your product image to `images/` folder:
   - Image: `yarbo-snow-blower.jpg`

2. Find a Yarbo snow blower video on YouTube:
   - Go to YouTube and find the video
   - Copy the video ID from the URL
   - Example: `youtube.com/watch?v=dQw4w9WgXcQ` → ID is `dQw4w9WgXcQ`

3. Replace `YOUR_SNOW_BLOWER_VIDEO_ID` in **TWO places** in the iframe src:
   ```html
   src="https://www.youtube.com/embed/VIDEO_ID?autoplay=1&mute=1&loop=1&playlist=VIDEO_ID&controls=0"
   ```

**Image specs:**
- Size: 1600x900px (16:9 ratio)
- Format: JPG
- File size: Under 200KB

#### Lawn Mower

**Search for:** `<!-- REPLACE WITH YOUR LAWN MOWER IMAGE -->`

**Steps:**
1. Add your product image: `yarbo-lawn-mower.jpg`
2. Get YouTube video ID from Yarbo's channel
3. Replace `YOUR_LAWN_MOWER_VIDEO_ID` in **TWO places**

---

### 3. How the YouTube Video Hover Works

When you add both an image and YouTube video ID:
- **Default state:** Shows the image
- **On hover:** Image fades out, YouTube video fades in and starts playing automatically
- **Video settings:** Muted, looped, no controls, autoplays on hover

**Important Notes:**
- You must replace the video ID in **2 places** in each iframe (for looping to work)
- Videos are embedded from YouTube, so no copyright issues!
- Videos will autoplay muted when someone hovers over the product

---

### 4. Removing Placeholders

Once you've added your real images:

**Search for:** `<div class="placeholder-image`

**Delete** these entire div blocks (they're just the SVG placeholders)

Example - DELETE THIS:
```html
<!-- Placeholder (remove when you add real images) -->
<div class="placeholder-image snow-blower">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
        <!-- ... SVG code ... -->
    </svg>
</div>
```

---

## Quick Search Commands

To find where to add images, search your HTML files for:

- `<img` - Finds all image tags
- `<video` - Finds all video tags
- `REPLACE WITH YOUR` - Finds all placeholder comments
- `placeholder-image` - Finds all placeholder divs to delete

---

## Image Optimization Tips

1. **Compress images** before uploading:
   - Use TinyPNG.com or Squoosh.app
   - Aim for under 200KB per product image

2. **Optimize videos:**
   - Use HandBrake or FFmpeg
   - H.264 codec, MP4 format
   - Lower bitrate for web (2-3 Mbps is plenty)

3. **Test file sizes:**
   - Run: `ls -lh images/` to see file sizes
   - Keep total page weight under 3MB

---

## File Structure

```
terrain-trace-website/
├── images/
│   ├── hero-bg.jpg              ← Add your hero image
│   ├── yarbo-snow-blower.jpg    ← Add your product image
│   └── yarbo-lawn-mower.jpg     ← Add your product image
```

**Note:** Videos come from YouTube embeds, so no video files needed!

---

Need help? All the image/video locations are clearly marked with HTML comments!
