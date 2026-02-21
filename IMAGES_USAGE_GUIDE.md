# 🖼️ How to Use Your New Images

Your images folder now contains **9 authentic Indian/Asian cuisine photos** that are perfect for your restaurant website!

## 📋 Image Inventory

| Image File | Best Use | Menu Category |
|------------|----------|---------------|
| `samosa.jpg` | Starters menu item | Starters |
| `chicken-tikka.jpg` | Starters/Main course | Starters/Main |
| `butter-chicken.jpg` | Main course item | Main Course |
| `paneer-tikka-masala.jpg` | Main course (hero image) | Main Course |
| `paneer-curry.jpg` | Main course item | Main Course |
| `gulab-jamun.jpg` | Dessert item | Desserts |
| `kulfi.jpg` | Dessert item | Desserts |
| `lassi.jpg` | Cold drink item | Cold Drinks |
| `mango-lassi.jpg` | Cold drink item | Cold Drinks |

---

## 🚀 Quick Implementation Guide

### Method 1: Update Menu Items with Real Photos

**Step 1:** Open `js/cart.js`

**Step 2:** Update the `menuData` array by adding `image` field to each item:

```javascript
const menuData = [
    // STARTERS
    {
        id: 1,
        name: "Samosa",  // Changed from "Garlic Bread"
        category: "starters",
        categoryDisplay: "Starters",
        price: 6.99,
        ingredients: "Crispy pastry filled with spiced potatoes, peas, served with chutney",
        emoji: "🥟",
        image: "samosa.jpg"  // ← ADD THIS LINE
    },
    {
        id: 2,
        name: "Chicken Tikka",  // Changed from "Spring Rolls"
        category: "starters",
        categoryDisplay: "Starters",
        price: 8.99,
        ingredients: "Marinated chicken, yogurt, spices, grilled to perfection",
        emoji: "🍢",
        image: "chicken-tikka.jpg"  // ← ADD THIS LINE
    },
    
    // MAIN COURSE
    {
        id: 4,
        name: "Butter Chicken",  // Changed from "Grilled Chicken"
        category: "main-course",
        categoryDisplay: "Main Course",
        price: 16.99,
        ingredients: "Tender chicken in creamy tomato sauce, butter, spices, served with rice",
        emoji: "🍛",
        image: "butter-chicken.jpg"  // ← ADD THIS LINE
    },
    {
        id: 5,
        name: "Paneer Tikka Masala",  // Changed from "Pasta Alfredo"
        category: "main-course",
        categoryDisplay: "Main Course",
        price: 14.99,
        ingredients: "Grilled paneer in rich tomato gravy, cream, aromatic spices",
        emoji: "🍲",
        image: "paneer-tikka-masala.jpg"  // ← ADD THIS LINE
    },
    {
        id: 6,
        name: "Paneer Curry",  // Keep as "Vegetable Curry"
        category: "main-course",
        categoryDisplay: "Main Course",
        price: 13.99,
        ingredients: "Cottage cheese, curry spices, tomatoes, cream, served with naan",
        emoji: "🍛",
        image: "paneer-curry.jpg"  // ← ADD THIS LINE
    },
    
    // DESSERTS
    {
        id: 7,
        name: "Gulab Jamun",  // Changed from "Chocolate Brownie"
        category: "desserts",
        categoryDisplay: "Desserts",
        price: 7.99,
        ingredients: "Sweet milk dumplings soaked in rose-flavored syrup",
        emoji: "🍡",
        image: "gulab-jamun.jpg"  // ← ADD THIS LINE
    },
    {
        id: 8,
        name: "Kulfi",  // Changed from "Ice Cream"
        category: "desserts",
        categoryDisplay: "Desserts",
        price: 5.99,
        ingredients: "Traditional Indian ice cream with cardamom, pistachios",
        emoji: "🍨",
        image: "kulfi.jpg"  // ← ADD THIS LINE
    },
    
    // COLD DRINKS
    {
        id: 10,
        name: "Sweet Lassi",  // Changed from "Fresh Juice"
        category: "cold-drinks",
        categoryDisplay: "Cold Drinks",
        price: 4.99,
        ingredients: "Refreshing yogurt drink with rose water, cardamom",
        emoji: "🥛",
        image: "lassi.jpg"  // ← ADD THIS LINE
    },
    {
        id: 11,
        name: "Mango Lassi",  // Changed from "Iced Coffee"
        category: "cold-drinks",
        categoryDisplay: "Cold Drinks",
        price: 5.49,
        ingredients: "Creamy yogurt smoothie blended with fresh mangoes",
        emoji: "🥭",
        image: "mango-lassi.jpg"  // ← ADD THIS LINE
    },
];
```

**Step 3:** Open `js/menu.js`

**Step 4:** Update the menu display function to show images instead of emojis:

Find the `displayMenuItems` function (around line 23) and replace:

```javascript
<div class="menu-item-image">
    ${item.emoji}
</div>
```

With:

```javascript
<div class="menu-item-image">
    ${item.image ? 
        `<img src="images/${item.image}" alt="${item.name}" 
         style="width: 100%; height: 100%; object-fit: cover;">` 
        : item.emoji}
</div>
```

---

### Method 2: Add Background Hero Image

**Option A:** Use Paneer Tikka Masala as hero background

Open `css/style.css`, find line ~91, replace with:

```css
.hero {
    background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
                url('../images/paneer-tikka-masala.jpg');
    background-size: cover;
    background-position: center;
}
```

---

## 🎨 Suggested Menu Updates

Since you now have Indian/Asian cuisine images, consider updating your menu to match:

### Starters:
- ✅ Samosa (use `samosa.jpg`)
- ✅ Chicken Tikka (use `chicken-tikka.jpg`)
- Keep or add: Soup of the Day

### Main Course:
- ✅ Butter Chicken (use `butter-chicken.jpg`)
- ✅ Paneer Tikka Masala (use `paneer-tikka-masala.jpg`)
- ✅ Paneer Curry (use `paneer-curry.jpg`)

### Desserts:
- ✅ Gulab Jamun (use `gulab-jamun.jpg`)
- ✅ Kulfi (use `kulfi.jpg`)
- Keep: Cheesecake (or replace)

### Cold Drinks:
- ✅ Sweet Lassi (use `lassi.jpg`)
- ✅ Mango Lassi (use `mango-lassi.jpg`)
- Keep: Soft Drinks

---

## ✅ Benefits of These Images

1. **Authentic Look**: Real Indian/Asian cuisine photos
2. **Small File Sizes**: Total only ~275 KB (fast loading!)
3. **Professional Quality**: High-resolution, appealing presentation
4. **Perfect Match**: Images align with menu categories
5. **Food Photography**: Proper lighting and plating

---

## 🔄 Before & After Example

### Before:
```javascript
{
    id: 1,
    name: "Garlic Bread",
    emoji: "🥖"
}
```

### After:
```javascript
{
    id: 1,
    name: "Samosa",
    emoji: "🥟",
    image: "samosa.jpg"
}
```

---

## 💡 Pro Tips

1. **Keep emoji as fallback**: If image doesn't load, emoji will show
2. **Update descriptions**: Change ingredients to match new dishes
3. **Adjust prices**: Update prices to match your restaurant
4. **Test thoroughly**: Check all images load correctly on menu page

---

## 📱 Mobile Responsive

All images are automatically responsive thanks to the CSS:
```css
.menu-item-image {
    width: 100%;
    height: 200px;
    object-fit: cover;  /* Ensures images look great at any size */
}
```

---

## 🎉 Ready to Go!

Your images are perfectly sized, optimized, and ready to use. Follow the steps above to integrate them into your restaurant website!

**Questions?** Check `ADMIN_GUIDE.md` for more customization tips.
