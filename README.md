# Jellyfin ElegantFin Add-ons

⚠️ **Important notice / Credits:**  
This project is fully based on the awesome [ElegantFin Theme](https://github.com/lscambo13/ElegantFin) by **[@lscambo13](https://github.com/lscambo13)**.  
All credits and the work goes to him. this is **not a standalone theme**, but only **add-ons / overrides** you can apply _on top_ of ElegantFin.  
The **original theme is not modified**, it stays untouched.

---

## ✨ Changes in this repo

- **Favorite heart**: when marked as favorite, the heart is now **fully filled red** instead of only showing a red outline.
- **Square posters & cards** (instead of rounded corners in the original).
- Show the header **home** button again.
- Hide the **Forgot password** button.
- Everything is delivered as **separate overrides** → just import or copy them.

---

## 📦 Modules

### ❤️ Favorite Heart Override

<details>
  <summary>🔗 Import from repo</summary>

```css
@import url("https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/heart.css");
```

</details>

<details>
  <summary>📋 Copy & Paste CSS</summary>

```css
/* Favorite Heart filled red */
.material-icons.detailButton-icon.favorite.ratingbutton-icon-withrating {
  color: red !important;
  font-variation-settings: "FILL" 1, "wght" 400, "GRAD" 0, "opsz" 48;
}
.material-icons.detailButton-icon.favorite.ratingbutton-icon-withrating::before {
  content: "favorite";
  color: red !important;
}
```

</details>

<details>
    <summary>🖼️ Image of a filled red heart </summary>

![Filled Red Heart](https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/images/heart-filled.png)

![Not Filled Red Heart](https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/images/heart-outline.png)

</details>

---

### ⬛ Square Poster Override

<details>
  <summary>🔗 Import from repo</summary>

```css
@import url("https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/square.css");
```

</details>

<details>
  <summary>📋 Copy & Paste CSS</summary>

```css
/* Posters and images with square corners */
.cardScalable,
.visualCardBox,
.listItemImage,
.listItemImageButton,
.coveredImage,
.cardImageContainer,
.cardImage,
.itemImage,
.primaryImageWrapper img {
  border-radius: 0 !important;
}

/* Cast/Person cards square instead of round */
@supports (aspect-ratio: 1 / 1) {
  #castCollapsible .cardScalable,
  #guestCastContent .cardScalable {
    border-radius: 0 !important;
  }
}
```

</details>

<details>
    <summary>🖼️ round vs Square Poster </summary>

![Round Corners](https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/images/round-corners.png)

![Square Corners](https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/images/square-corners.png)

</details>

---

### 🏠 Show Home Button at the top

<details>
  <summary>🔗 Import from repo</summary>

```css
@import url("https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/show-homebutton.css");
```

</details>
<details>
  <summary>📋 Copy & Paste CSS</summary>

```css
/* Show the header home button again */
.skinHeader-withBackground:not(.semiTransparent) .headerHomeButton {
  display: initial !important;
}
```

</details>

---

### ❌ Hide "Forgot Password" Button on Login Screen

<details>
    <summary>🔗 Import from repo</summary>

```css
@import url("https://raw.githubusercontent.com/Panda260/ElegantFin-addones/main/hide-forgotpassword.css");
```

</details>

<details>
    <summary>📋 Copy & Paste CSS</summary>

```css
/* Hide the "Forgot Password" button */
.skinHeader-withBackground:not(.semiTransparent) .headerForgotPasswordButton {
  display: none !important;
}
```

</details>

<br>

---

## 🚀 Usage

1. First, make sure you import the **[original ElegantFin theme](https://github.com/lscambo13/ElegantFin?tab=readme-ov-file#-how-to-installsetup-this-theme)** in Jellyfin:
   ```css
   @import url("https://cdn.jsdelivr.net/gh/lscambo13/ElegantFin@main/Theme/ElegantFin-jellyfin-theme-build-latest-minified.css");
   ```
2. Import one or more of these snippets from the add-ons section below the main elegantfin import.
3. Done 🎉 only the necessary parts are overridden.

---

## ℹ️ Note

These add-ons are **compatible with ElegantFin**, but may need adjustments with future updates of the main theme.  
If you like ElegantFin, please ⭐️ the [original repo](https://github.com/lscambo13/ElegantFin) by [@lscambo13](https://github.com/lscambo13).
