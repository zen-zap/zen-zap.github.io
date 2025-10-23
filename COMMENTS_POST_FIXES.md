# Comments & Post Visibility Fixes

## Issues Identified & Fixed

### 1. ✅ Comments Not Showing on Blog Posts
**Problem:** The Chirpy theme uses `script_includes` instead of directly including the comment partial in the post layout.

**Solution:** Created a custom `_layouts/post.html` that explicitly includes comments via `tail_includes`:
```yaml
tail_includes:
  - related-posts
  - post-nav
  - comment
```

This overrides the theme's default post layout and ensures comments are loaded properly.

### 2. ✅ Pokemon Post Not Showing
**Problem:** Your post file was named `2025-11-10-pokemon.md` with a November date, but today is October 23, 2025. Jekyll doesn't show future-dated posts by default.

**Solution:** The file has been corrected to `2025-10-23-pokemon.md` with matching date in front matter.

## How Comments Work Now

### For Blog Posts (layout: post)
- Uses custom `_layouts/post.html` (overrides theme)
- Includes `comment.html` via `tail_includes`
- Uses **default Giscus styling** (no custom CSS)
- Responsive and fits within content area perfectly

### For Project Pages (layout: project)
- Uses custom `_layouts/project.html`
- Includes `comment.html` directly
- Loads `giscus-custom.css` with theme-matching colors
- Custom minimal styling

## Testing Checklist

1. **Blog Posts:**
   - Visit http://localhost:4000/2025/10/23/pokemon/
   - Visit http://localhost:4000/2025/10/07/quic/
   - Comments should appear at bottom (default Giscus theme)
   - Should be responsive and not stretch

2. **Project Pages:**
   - Visit your project pages
   - Comments should have custom turquoise styling
   - Should integrate seamlessly

3. **Home Page:**
   - Visit http://localhost:4000/
   - Should see all 3 posts listed:
     - Hey There! (July 13)
     - QUIC (Oct 7)
     - Hey pokemon! (Oct 23)

## Files Modified

1. **`_layouts/post.html`** (NEW)
   - Custom post layout with comment support
   - Overrides theme's default

2. **`_includes/comment.html`**
   - Conditional CSS loading (only for projects)

3. **`assets/css/giscus-custom.css`**
   - Simplified (only for projects)
   - Removed all problematic layout rules

## Important Notes

- **Don't use future dates** in post filenames or front matter
- The filename date should match the `date:` in front matter
- Comments on posts use Giscus default theme (reliable, responsive)
- Comments on projects use custom theme (turquoise colors)

## If Comments Still Don't Work

1. Clear Jekyll cache: `bundle exec jekyll clean`
2. Restart server: `Ctrl+C` then `bundle exec jekyll serve`
3. Hard refresh browser: `Ctrl+Shift+R` or `Cmd+Shift+R`
4. Check browser console for errors
5. Ensure GitHub Discussions is enabled on your repo
6. Ensure Giscus app is installed on your repo

---

**Status:** Both issues should now be resolved! 🎉
