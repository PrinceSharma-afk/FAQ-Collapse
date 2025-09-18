# ❓ FAQ Collapse

A fun FAQ Accordion project from **50 Projects in 50 Days**.  
Click on a question to reveal the answer. The toggle button changes from `+` to `−` when expanded.

---

## 🚀 Live Demo

👉 [Click here to try it out](https://PrinceSharma-afk.github.io/faq-collapse/)

---

## 📸 Preview

**Example FAQ:**

**Q:** Why did the math book look sad?  
**A:** Because it had too many problems.

**Q:** Why don't programmers like nature?  
**A:** It has too many bugs.

---

## 🛠️ Built With

- **HTML5** – structure  
- **CSS3** – styling & animations  
- **JavaScript (ES6)** – DOM manipulation for toggling

---

## 📂 Project Structure

```
faq-collapse/
│
├── index.html          # Main HTML file
├── style.css           # Styling
├── script.js           # Toggle logic
└── README.md           # Documentation
```

---

## ⚙️ How It Works

1. Each FAQ is wrapped in a `.faq` container.  
2. The answer text `.faq-text` is hidden by default using CSS (`display: none`).  
3. Clicking the `.faq-toggle` button toggles the `.active` class on the parent `.faq`.  
4. When `.active` is present:
   - The answer text becomes visible (`display: block`).  
   - The button icon switches from `+` to `−`.

**JS snippet:**

```js
const btns = document.querySelectorAll('.faq-toggle');

btns.forEach((btn) => {
  btn.addEventListener('click', () => {
    btn.parentNode.classList.toggle('active');
    btn.textContent = btn.parentNode.classList.contains('active') ? '−' : '+';
  });
});
```

---

## 💡 Usage

1. **Clone the repo:**
   ```bash
   git clone https://github.com/PrinceSharma-afk/faq-collapse.git
   ```

2. **Navigate to the folder:**
   ```bash
   cd faq-collapse
   ```

3. **Open `index.html` in your browser** and click the questions to see answers.

---

## ✨ Features

- **Smooth Animations** – CSS transitions for opening/closing
- **Responsive Design** – Works on all screen sizes
- **Interactive Toggle** – Visual feedback with `+`/`−` icons
- **Clean UI** – Modern accordion design
- **Accessibility** – Keyboard navigation support

---

## 🎨 Customization

### Adding New FAQs

Add a new FAQ block in your HTML:

```html
<div class="faq">
  <div class="faq-question">
    <h3>Your question here?</h3>
    <button class="faq-toggle">+</button>
  </div>
  <div class="faq-text">
    <p>Your answer here.</p>
  </div>
</div>
```

### Styling Options

Modify `style.css` to change:
- Colors (`--primary-color`, `--secondary-color`)
- Animation duration (`transition: all 0.3s ease`)
- Font sizes and spacing
