# MY_PORTFOLIO
# Harsh Rai - Data Analyst Portfolio

A modern, responsive single-page portfolio website designed for an entry-level Data Analyst / MIS Executive. This project showcases skills, projects, and certifications using a clean, glassmorphism-inspired UI.

## 🚀 Features

*   **Responsive Design**: Fully responsive layout using Tailwind CSS, optimized for mobile and desktop.
*   **Single File Architecture**: Most logic and styling are contained within `index.html` for simplicity.
*   **Dynamic Content**: Content sections (Skills, Projects, Certifications) are rendered via JavaScript, making updates easy without digging through HTML structure.
*   **Performance**: Optimized CSS and minimal JavaScript usage (using `requestAnimationFrame` for scroll spying).
*   **Glassmorphism UI**: Modern visual aesthetic with translucent cards and subtle gradients.

## 🛠️ Tech Stack

*   **HTML5**: Semantic markup.
*   **CSS3**: Tailwind CSS (via CDN) + Custom CSS variables for theming.
*   **JavaScript**: Vanilla JS for DOM manipulation and data rendering.

## 📂 Project Structure

```text
portfolio 2.0/
├── index.html          # Main entry point containing structure, styles, and logic
├── assets/
│   └── resume.pdf      # (Optional) Place your resume file here
└── README.md           # Project documentation
```

## ⚙️ How to Use

1.  **Download**: Clone or download this repository.
2.  **Run**: Simply open `index.html` in any modern web browser. No build step or server is required.

## 📝 Customization

The content is separated from the HTML structure to make editing easier. Scroll down to the `<script>` tag at the bottom of `index.html` to update your information.

### Updating Data
Look for the following variables in the JavaScript section at the bottom of the file:

*   **Navigation**: Update the array `['Home','About',...]` to change menu links.
*   **Profile Snapshot**: Edit the array passed to `$('snapshotList').innerHTML`.
*   **Keywords**: Edit the array passed to `$('keywords').innerHTML`.
*   **Skills**: Modify the `skillsGrid` array structure (Category -> List of skills).
*   **Projects**: Update the objects inside `$('projectsGrid').innerHTML`.
*   **Certifications**: Update the objects inside `$('certsGrid').innerHTML`.

### Updating Resume
Ensure you have a file named `resume.pdf` inside an `assets` folder, or update the `href` in the HTML:
```html
<!-- Line ~68 -->
<a href="assets/resume.pdf" download ...>
```

## 🎨 Styling

Styling is primarily handled by **Tailwind CSS**. Custom overrides and theme variables (colors like `--accent`, `--bg`, `--card`) are defined in the `<style>` block in the `<head>`.

To change the color scheme, simply modify the `:root` variables:
```css
:root {
    --accent: #006b6a; /* Change this to your preferred primary color */
}
```
