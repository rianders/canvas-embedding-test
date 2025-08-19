# Embedding Interactive HTML Content in Canvas using GitHub Pages

## 📚 Overview

Canvas blocks JavaScript execution in uploaded HTML files for security reasons. This guide shows you how to host your interactive content on GitHub Pages (free) and embed it in Canvas, allowing full JavaScript functionality for applications like:
- Interactive simulations
- Pose detection apps
- Data visualizations
- Games and animations
- Any HTML/CSS/JavaScript project

## 🚀 Quick Start Guide

### Prerequisites
- A GitHub account (free at [github.com](https://github.com))
- Your HTML file(s) ready to deploy
- Access to create/edit Canvas Pages in your course

### Step 1: Create a GitHub Repository

1. **Sign in to GitHub** and click the **"+"** button in the top right
2. Select **"New repository"**
3. Configure your repository:
   - **Repository name:** Choose something descriptive (e.g., `physics-simulations`, `pose-detection-app`)
   - **Description:** Optional but helpful
   - **Public/Private:** Must be **Public** for free GitHub Pages hosting
   - **Initialize with README:** Optional (you can add this file later)
4. Click **"Create repository"**

### Step 2: Upload Your HTML File

1. In your new repository, click **"uploading an existing file"** or **"Add file" → "Upload files"**
2. Upload your HTML file(s):
   - **IMPORTANT:** Name your main file `index.html` (this will be your homepage)
   - You can also upload CSS, JavaScript, images, and other assets
3. Add a commit message (e.g., "Add interactive content")
4. Click **"Commit changes"**

### Step 3: Enable GitHub Pages

1. In your repository, click **"Settings"** (top menu bar)
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Source"**, select:
   - **Source:** Deploy from a branch
   - **Branch:** main (or master)
   - **Folder:** / (root)
4. Click **"Save"**
5. GitHub will display your site URL at the top of the Pages settings:
   ```
   Your site is live at https://[your-username].github.io/[repository-name]/
   ```

### Step 4: Wait for Deployment

1. Click the **"Actions"** tab in your repository
2. You'll see a workflow running (orange circle)
3. Wait for it to complete (green checkmark) - usually 1-2 minutes
4. Test your site by visiting the URL directly

### Step 5: Create the Embed Code

Once your site is live, create an iframe embed code:

```html
<iframe src="https://[your-username].github.io/[repository-name]/" 
        width="100%" 
        height="600"
        frameborder="0">
</iframe>
```

**For apps needing camera/microphone access:**
```html
<iframe src="https://[your-username].github.io/[repository-name]/" 
        width="100%" 
        height="800"
        frameborder="0"
        allow="camera; microphone"
        allowfullscreen>
</iframe>
```

### Step 6: Add to Canvas

1. Navigate to your Canvas course
2. Create a new **Page** (or edit an existing one)
3. In the Rich Content Editor, click the **HTML Editor** button (`</>`)
4. Paste your iframe code
5. Click **"Save"** or **"Update"**
6. Switch back to the Rich Content Editor to preview
7. Save the Canvas Page

## 📁 File Structure Examples

### Single File Project
```
repository/
└── index.html (contains all HTML, CSS, and JavaScript)
```

### Multi-File Project
```
repository/
├── index.html
├── style.css
├── script.js
├── images/
│   └── logo.png
└── data/
    └── dataset.json
```

## 🔧 Troubleshooting

### Content Not Showing in Canvas
- Verify the GitHub Pages site works by visiting it directly
- Check that you're using the HTML editor in Canvas, not the visual editor
- Ensure your repository is public
- Wait 2-5 minutes after enabling GitHub Pages

### JavaScript Not Working
- This shouldn't happen with GitHub Pages hosting
- Check browser console for errors (F12 → Console)
- Ensure all file paths are relative, not absolute

### Camera/Microphone Not Working
- Add `allow="camera; microphone"` to your iframe
- Note: HTTPS is required (GitHub Pages provides this)

### Height/Width Issues
- Adjust the `height` attribute (try 600, 800, or "100vh")
- Use `width="100%"` for responsive design
- Consider adding `style="min-height: 600px"` for better mobile display

## 💡 Best Practices

1. **Test Locally First:** Open your HTML file directly in a browser before uploading
2. **Use Relative Paths:** Reference assets with relative paths (`./images/logo.png`)
3. **Mobile Responsive:** Test on different screen sizes
4. **Clear Instructions:** Add usage instructions within your app for students
5. **Accessibility:** Include alt text, proper contrast, and keyboard navigation

## 🔄 Updating Your Content

1. Edit files directly on GitHub or upload new versions
2. Commit your changes
3. GitHub Pages automatically redeploys (1-2 minutes)
4. Canvas iframe will show updated content (may need to refresh)

## 🎯 Examples of Interactive Content

Perfect for embedding:
- **STEM:** Physics simulations, graphing calculators, molecular viewers
- **Computer Science:** Code editors, algorithm visualizers, debugging tools
- **Health/Kinesiology:** Pose detection, anatomy models, exercise trackers
- **Data Science:** Interactive charts, data explorers, statistical tools
- **Arts:** Drawing tools, music synthesizers, animation creators

## 🚫 Canvas File Upload Limitations

Why direct Canvas uploads don't work:
- Canvas sandboxes HTML files with `sandbox` attribute without `allow-scripts`
- Security headers prevent JavaScript execution
- This is intentional for security (prevents XSS attacks)
- No workaround exists within Canvas's file system

## 📚 Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Canvas Instructor Guide](https://community.canvaslms.com/t5/Instructor-Guide/tkb-p/Instructor)
- [MDN iframe Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

## 🤝 Support

For GitHub issues:
- Check [GitHub Status](https://www.githubstatus.com/)
- Visit [GitHub Support](https://support.github.com/)

For Canvas issues:
- Contact your institution's IT support
- Check Canvas Community forums

## 📝 License

This guide is provided as-is for educational purposes. Feel free to share and adapt for your institution's needs.

---

*Created for faculty who need to embed interactive JavaScript content in Canvas LMS*
