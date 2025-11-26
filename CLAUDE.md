# The King's Treasure - Web Edition

**Inherits from**: Main vault CLAUDE.md
**Scope**: This directory and subdirectories only

## Image Workflow

When creating or updating game sprites:

### 1. Create/Save Original PNG
- Save the original high-resolution PNG to `../sprites_backup_png/[category]/`
- Categories: `enemies`, `items`, `locations`, `shields`, `weapons`
- Keep originals at full resolution for future use

### 2. Create Optimized WebP Version
Run these commands from the `web-edition` directory:

```bash
# Resize to 512x512 max dimension
sips -Z 512 "../sprites_backup_png/[category]/[filename].png" --out "/tmp/resized.png"

# Convert to WebP with quality 80
cwebp -q 80 "/tmp/resized.png" -o "assets/sprites/[category]/[filename].webp"

# Clean up
rm /tmp/resized.png
```

### 3. Update Preloader (if new file)
Add the new sprite path to `js/preloader.js` in the appropriate section.

### Example: Adding a New Enemy
```bash
# 1. Save original to backup
cp ~/Downloads/new_enemy.png ../sprites_backup_png/enemies/

# 2. Create optimized version
sips -Z 512 "../sprites_backup_png/enemies/new_enemy.png" --out "/tmp/resized.png"
cwebp -q 80 "/tmp/resized.png" -o "assets/sprites/enemies/new_enemy.webp"

# 3. Don't forget the defeated version too!
sips -Z 512 "../sprites_backup_png/enemies/new_enemy_defeated.png" --out "/tmp/resized.png"
cwebp -q 80 "/tmp/resized.png" -o "assets/sprites/enemies/new_enemy_defeated.webp"
```

### Image Specifications
- **Format**: WebP (for web deployment)
- **Max Dimension**: 512x512 pixels
- **Quality**: 80 (good balance of quality/size)
- **Naming**: lowercase, underscores for spaces (e.g., `shark_tooth_amulet.webp`)

### Backup Location
Original PNGs are stored at: `kings-treasure/sprites_backup_png/`

## Deployment

### GitHub Pages
- Repository: https://github.com/dperalta716/kings-treasure-online
- Live URL: https://dperalta716.github.io/kings-treasure-online/

### To Deploy Changes
```bash
git add -A
git commit -m "Description of changes"
git push
```
Changes go live in ~1 minute after push.
