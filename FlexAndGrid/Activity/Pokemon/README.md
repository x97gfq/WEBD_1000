# Responsive Pokémon Cards

This project demonstrates a simple, responsive HTML5 layout using **CSS Grid** and **Flexbox** to display six Pokémon cards. Each card includes an image and a name, styled with minimal CSS for clarity and educational purposes.

## 📁 Files

### `index.html`

This file contains the structure of the webpage. It includes:

- A `<div class="container">` that wraps all the Pokémon cards.
- Each card is a `<div class="card">` containing:
  - An `<img>` element for the Pokémon sprite.
  - An `<h3>` element for the Pokémon's name.

### `style.css`

This file contains the styling rules for the layout and cards. It uses:

- **CSS Grid** for the overall layout of the cards.
- **Flexbox** inside each card to align content vertically.
- Minimal styling for readability and responsiveness.

---

## 🧱 Layout Techniques

### CSS Grid: `.container`

```css
.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 20px;
}
```

#### 🔍 Explanation:

- `display: grid;` enables grid layout on the container.
- `grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));` is the key to responsive behavior:
  - `repeat(...)` tells the browser to repeat the column definition.
  - `auto-fit` automatically calculates how many columns can fit in the container based on available space.
  - `minmax(150px, 1fr)` ensures each column is **at least 150px wide**, but can grow to fill available space.
  - `1fr` means each column takes up **one fraction** of the remaining space, evenly distributed.

This setup allows the grid to adapt to different screen sizes:
- On large screens, more columns fit side by side.
- On smaller screens, fewer columns appear, and they stack vertically if needed.

### Flexbox: `.card`

```css
.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}
```

#### 🔍 Explanation:

- `display: flex;` enables Flexbox layout inside each card.
- `flex-direction: column;` stacks the image and text vertically.
- `align-items: center;` centers the content horizontally.
- `text-align: center;` ensures the text is centered within the card.

This makes each card's content neatly aligned and visually balanced.

---

## 📱 Responsive Design

The combination of Grid and Flexbox ensures that the layout works well across devices:

- **Desktop**: Cards are arranged in multiple columns.
- **Tablet**: Fewer columns, but still side-by-side.
- **Mobile**: Cards stack vertically for readability.

No media queries are needed thanks to the flexibility of `auto-fit` and `minmax()` in Grid.

---

## 🧪 How to Use

1. Download or clone the repository.
2. Open `index.html` in a browser.
3. Resize the browser window to see the responsive behavior in action.

---

## 🧠 Learning Objectives

- Understand how to use **CSS Grid** for responsive layouts.
- Learn how **Flexbox** helps align content within components.
- Explore the power of `grid-template-columns` with `auto-fit` and `minmax()`.

---

## 🔗 Resources

- [CSS Grid Layout Guide (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)
- [A Complete Guide to Flexbox (CSS-Tricks)](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [PokeAPI Sprites](https://github.com/PokeAPI/sprites)

---

Happy coding! 🎉
