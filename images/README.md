# Images Folder

This folder contains 9 delicious Indian/Asian cuisine images ready to use!

## 📸 Images Included

✅ **samosa.jpg** (22 KB) - Crispy golden samosas - Perfect for Starters  
✅ **paneer-tikka-masala.jpg** (106 KB) - Paneer in rich tomato gravy with naan  
✅ **butter-chicken.jpg** (39 KB) - Creamy butter chicken curry with rice  
✅ **paneer-curry.jpg** (27 KB) - Rich paneer curry - Main course  
✅ **chicken-tikka.jpg** (22 KB) - Grilled chicken tikka skewers  
✅ **gulab-jamun.jpg** (13 KB) - Traditional sweet gulab jamun dessert  
✅ **kulfi.jpg** (14 KB) - Creamy kulfi ice cream bars - Dessert  
✅ **lassi.jpg** (17 KB) - Refreshing traditional lassi drink  
✅ **mango-lassi.jpg** (15 KB) - Sweet mango lassi beverage  

**Total Size:** ~275 KB (highly optimized for fast loading!)

## 🎯 Perfect Match for Menu Items

These images align beautifully with Indian/Asian restaurant themes and can be easily mapped to your menu categories.

## 🎯 How to Use Images

### Option 1: Update Hero Background
In `css/style.css`, find the `.hero` section (around line 91) and replace the SVG background:

```css
.hero {
    background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)),
                url('../images/hero-bg.jpg');  /* Add your image here */
    background-size: cover;
    background-position: center;
}
```

### Option 2: Add Logo to Navbar
In all HTML files, update the navbar:

```html
<div class="nav-brand">
    <img src="images/logo.png" alt="Logo" style="height: 40px;">
    <h1>The Golden Spoon</h1>
</div>
```

### Option 3: Replace Menu Item Emojis with Photos
In `js/menu.js`, update the menu item display (around line 30):

```javascript
<div class="menu-item-image">
    <img src="images/food-photos/${item.image}" alt="${item.name}" 
         style="width: 100%; height: 100%; object-fit: cover;">
</div>
```

And add image filenames to menu items in `js/cart.js`:

```javascript
{
    id: 1,
    name: "Garlic Bread",
    image: "starters/garlic-bread.jpg",  // Add this line
    // ... rest of item
}
```

## 📐 Recommended Image Sizes

- **Logo**: 200x80px (PNG with transparency)
- **Hero Background**: 1920x1080px (JPG)
- **Menu Item Photos**: 600x600px (square, JPG)
- **About Section**: 1200x800px (JPG)

## 🎨 Image Tips

1. **Optimize images** before uploading (compress to reduce file size)
2. **Use JPG** for photos (smaller file size)
3. **Use PNG** for logos (supports transparency)
4. **Keep filenames lowercase** with hyphens (e.g., `garlic-bread.jpg`)
5. **Ensure images are high quality** but not too large (under 500KB each)

## 🔗 Free Stock Photo Resources

If you need placeholder images:
- **Unsplash** - unsplash.com (search "food")
- **Pexels** - pexels.com (search "restaurant")
- **Pixabay** - pixabay.com (search "cuisine")

---

**Note**: Currently the website uses emojis (🥖🍗🍰) as placeholders. You can keep them or replace with actual food photos by following the instructions above.
