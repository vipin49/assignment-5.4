
## 1. Objective

The objective of this assignment is to create a small design system using CSS variables and reusable design tokens. CSS variables help maintain consistent colors, spacing, font sizes, and other design properties across a webpage.

## 2. Requirements

- Visual Studio Code
- HTML
- CSS
- Google Chrome
- Live Server extension (optional)

## 3. Project Folder Structure

Create a folder named `Assignment-5.4` with the following files:

```text
Assignment-5.4/
│
├── index.html
├── style.css
└── Assignment-5.4.md
```

## 4. HTML Code (index.html)

Create a file named `index.html` and paste the following complete code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>CSS Variables and Design Tokens</title>

    <!-- External CSS File -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header -->
    <header class="site-header">
        <div class="container">
            <h1>My Design System</h1>
            <p>
                A simple webpage built with reusable CSS variables
                and design tokens.
            </p>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="navigation">
        <div class="container nav-content">
            <a href="#home">Home</a>
            <a href="#colors">Colors</a>
            <a href="#spacing">Spacing</a>
            <a href="#components">Components</a>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="container">

        <!-- Introduction -->
        <section id="home" class="section">
            <h2>Welcome to My Design System</h2>

            <p>
                A design system is a collection of reusable design
                rules and components. CSS variables make it easier
                to update the appearance of a website from one place.
            </p>

            <button class="btn btn-primary">Primary Button</button>
            <button class="btn btn-secondary">Secondary Button</button>
        </section>

        <!-- Color Tokens -->
        <section id="colors" class="section">
            <h2>Color Tokens</h2>

            <p>
                These colors are defined as CSS variables and reused
                throughout the webpage.
            </p>

            <div class="color-grid">
                <div class="color-card">
                    <div class="color-preview primary-preview"></div>
                    <h3>Primary Color</h3>
                    <p>Used for buttons and important elements.</p>
                </div>

                <div class="color-card">
                    <div class="color-preview secondary-preview"></div>
                    <h3>Secondary Color</h3>
                    <p>Used for supporting buttons and accents.</p>
                </div>

                <div class="color-card">
                    <div class="color-preview background-preview"></div>
                    <h3>Background Color</h3>
                    <p>Used for the main page background.</p>
                </div>

                <div class="color-card">
                    <div class="color-preview text-preview"></div>
                    <h3>Text Color</h3>
                    <p>Used for readable body text.</p>
                </div>
            </div>
        </section>

        <!-- Spacing Tokens -->
        <section id="spacing" class="section">
            <h2>Spacing Tokens</h2>

            <p>
                Small, medium, and large spacing variables help keep
                margins and padding consistent.
            </p>

            <div class="spacing-example">
                <div class="spacing-box spacing-small">
                    Small Spacing
                </div>

                <div class="spacing-box spacing-medium">
                    Medium Spacing
                </div>

                <div class="spacing-box spacing-large">
                    Large Spacing
                </div>
            </div>
        </section>

        <!-- Font Size Tokens -->
        <section class="section">
            <h2>Typography Tokens</h2>

            <p class="text-small">
                Small Text — This uses the small font-size variable.
            </p>

            <p class="text-medium">
                Medium Text — This uses the medium font-size variable.
            </p>

            <p class="text-large">
                Large Text — This uses the large font-size variable.
            </p>
        </section>

        <!-- Reusable Components -->
        <section id="components" class="section">
            <h2>Reusable Cards and Buttons</h2>

            <div class="card-grid">
                <article class="card">
                    <h3>Design Consistency</h3>
                    <p>
                        Reusable variables help maintain the same colors,
                        spacing, and typography throughout a website.
                    </p>
                    <button class="btn btn-primary">Learn More</button>
                </article>

                <article class="card">
                    <h3>Easy Maintenance</h3>
                    <p>
                        Changing a single CSS variable can update
                        multiple elements at the same time.
                    </p>
                    <button class="btn btn-secondary">Explore</button>
                </article>

                <article class="card">
                    <h3>Reusable Styles</h3>
                    <p>
                        Design tokens reduce repeated values and make
                        CSS easier to maintain.
                    </p>
                    <button class="btn btn-primary">Get Started</button>
                </article>
            </div>
        </section>

        <!-- Variable Testing -->
        <section class="section">
            <h2>Variable Testing</h2>

            <p>
                Change the primary color variable in the CSS file.
                The primary buttons, header, and other related elements
                will update automatically.
            </p>

            <p class="note">
                Testing example: Change --color-primary from #2563eb
                to #7c3aed and reload the webpage.
            </p>
        </section>

    </main>

    <!-- Footer -->
    <footer class="site-footer">
        <div class="container">
            <p>&copy; 2026 My Design System. Created using HTML and CSS.</p>
        </div>
    </footer>

</body>
</html>
```

## 5. CSS Code (style.css)

Create a file named `style.css` in the same folder and paste the following complete code:

```css
/* =========================================
   1. DESIGN TOKENS: CSS VARIABLES
   ========================================= */

:root {
    /* Color Variables */
    --color-primary: #2563eb;
    --color-secondary: #0f766e;
    --color-background: #f1f5f9;
    --color-text: #1e293b;
    --color-white: #ffffff;
    --color-border: #cbd5e1;
    --color-muted: #64748b;
    --color-surface: #eaf1ff;

    /* Spacing Variables */
    --space-small: 8px;
    --space-medium: 16px;
    --space-large: 32px;

    /* Font Size Variables */
    --font-size-small: 14px;
    --font-size-medium: 16px;
    --font-size-large: 24px;

    /* Additional Design Tokens */
    --font-family-base: Arial, Helvetica, sans-serif;
    --border-radius: 10px;
    --border-radius-small: 6px;
    --shadow-card: 0 4px 12px rgba(15, 23, 42, 0.08);
    --container-width: 1100px;
}

/* =========================================
   2. GENERAL STYLING
   ========================================= */

* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    margin: 0;
    padding: 0;
    font-family: var(--font-family-base);
    font-size: var(--font-size-medium);
    background-color: var(--color-background);
    color: var(--color-text);
    line-height: 1.7;
}

.container {
    width: 90%;
    max-width: var(--container-width);
    margin: 0 auto;
}

h1,
h2,
h3 {
    line-height: 1.3;
}

h2 {
    font-size: var(--font-size-large);
    color: var(--color-primary);
    margin-top: 0;
    margin-bottom: var(--space-medium);
}

h3 {
    font-size: 19px;
    margin-top: 0;
    margin-bottom: var(--space-small);
}

p {
    margin-top: 0;
    margin-bottom: var(--space-medium);
}

/* =========================================
   3. HEADER
   ========================================= */

.site-header {
    background-color: var(--color-primary);
    color: var(--color-white);
    padding: var(--space-large) 0;
    text-align: center;
}

.site-header h1 {
    font-size: 36px;
    margin-top: 0;
    margin-bottom: var(--space-small);
}

.site-header p {
    margin-bottom: 0;
}

/* =========================================
   4. NAVIGATION
   ========================================= */

.navigation {
    background-color: var(--color-white);
    border-bottom: 1px solid var(--color-border);
}

.nav-content {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: var(--space-medium);
    flex-wrap: wrap;
    padding: var(--space-medium) 0;
}

.navigation a {
    color: var(--color-primary);
    text-decoration: none;
    font-weight: bold;
    padding: var(--space-small);
    border-radius: var(--border-radius-small);
}

.navigation a:hover {
    background-color: var(--color-surface);
}

/* =========================================
   5. MAIN SECTIONS
   ========================================= */

main {
    padding-top: var(--space-large);
    padding-bottom: var(--space-large);
}

.section {
    background-color: var(--color-white);
    padding: var(--space-large);
    margin-bottom: var(--space-large);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-card);
}

/* =========================================
   6. BUTTONS
   ========================================= */

.btn {
    display: inline-block;
    border: none;
    border-radius: var(--border-radius-small);
    padding: var(--space-small) var(--space-medium);
    margin: var(--space-small) var(--space-small) 0 0;
    font-family: var(--font-family-base);
    font-size: var(--font-size-medium);
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.btn-primary {
    background-color: var(--color-primary);
    color: var(--color-white);
}

.btn-primary:hover {
    background-color: var(--color-secondary);
}

.btn-secondary {
    background-color: var(--color-secondary);
    color: var(--color-white);
}

.btn-secondary:hover {
    background-color: var(--color-primary);
}

/* =========================================
   7. COLOR TOKEN CARDS
   ========================================= */

.color-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: var(--space-medium);
    margin-top: var(--space-large);
}

.color-card {
    overflow: hidden;
    border: 1px solid var(--color-border);
    border-radius: var(--border-radius);
    background-color: var(--color-white);
    padding-bottom: var(--space-medium);
}

.color-card h3,
.color-card p {
    margin-left: var(--space-medium);
    margin-right: var(--space-medium);
}

.color-card h3 {
    margin-top: var(--space-medium);
}

.color-card p {
    font-size: var(--font-size-small);
    color: var(--color-muted);
    margin-bottom: 0;
}

.color-preview {
    height: 85px;
}

.primary-preview {
    background-color: var(--color-primary);
}

.secondary-preview {
    background-color: var(--color-secondary);
}

.background-preview {
    background-color: var(--color-background);
    border-bottom: 1px solid var(--color-border);
}

.text-preview {
    background-color: var(--color-text);
}

/* =========================================
   8. SPACING TOKEN EXAMPLES
   ========================================= */

.spacing-example {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: var(--space-medium);
}

.spacing-box {
    background-color: var(--color-surface);
    color: var(--color-primary);
    border-left: 4px solid var(--color-primary);
    border-radius: var(--border-radius-small);
    font-weight: bold;
}

.spacing-small {
    padding: var(--space-small);
}

.spacing-medium {
    padding: var(--space-medium);
}

.spacing-large {
    padding: var(--space-large);
}

/* =========================================
   9. TYPOGRAPHY TOKENS
   ========================================= */

.text-small {
    font-size: var(--font-size-small);
}

.text-medium {
    font-size: var(--font-size-medium);
}

.text-large {
    font-size: var(--font-size-large);
    color: var(--color-secondary);
    font-weight: bold;
}

/* =========================================
   10. REUSABLE CARDS
   ========================================= */

.card-grid {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: var(--space-medium);
    margin-top: var(--space-large);
}

.card {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    background-color: var(--color-white);
    border: 1px solid var(--color-border);
    border-top: 4px solid var(--color-primary);
    border-radius: var(--border-radius);
    padding: var(--space-medium);
    box-shadow: var(--shadow-card);
}

.card h3 {
    color: var(--color-primary);
}

.card p {
    font-size: var(--font-size-small);
    color: var(--color-muted);
}

.card .btn {
    margin-top: auto;
}

/* =========================================
   11. TESTING NOTE
   ========================================= */

.note {
    background-color: var(--color-surface);
    color: var(--color-text);
    border-left: 4px solid var(--color-primary);
    padding: var(--space-medium);
    border-radius: var(--border-radius-small);
    font-size: var(--font-size-small);
}

/* =========================================
   12. FOOTER
   ========================================= */

.site-footer {
    background-color: var(--color-text);
    color: var(--color-white);
    text-align: center;
    padding: var(--space-large) 0;
}

.site-footer p {
    margin-bottom: 0;
    font-size: var(--font-size-small);
}

/* =========================================
   13. RESPONSIVE DESIGN
   ========================================= */

@media (max-width: 800px) {
    .color-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .card-grid {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 500px) {
    .container {
        width: 92%;
    }

    .site-header h1 {
        font-size: 28px;
    }

    .section {
        padding: var(--space-medium);
    }

    h2 {
        font-size: 21px;
    }

    .color-grid {
        grid-template-columns: 1fr;
    }

    .nav-content {
        gap: var(--space-small);
    }
}
```

## 6. Explanation of CSS Variables

CSS variables are reusable values defined with names beginning with `--`. They can be used elsewhere through the `var()` function.

Example:

```css
:root {
    --color-primary: #2563eb;
    --space-medium: 16px;
    --font-size-large: 24px;
}

h2 {
    color: var(--color-primary);
    font-size: var(--font-size-large);
    margin-bottom: var(--space-medium);
}
```

### Design tokens used in this assignment

| Variable | Value | Purpose |
|---|---|---|
| `--color-primary` | `#2563eb` | Main brand color |
| `--color-secondary` | `#0f766e` | Supporting color |
| `--color-background` | `#f1f5f9` | Page background |
| `--color-text` | `#1e293b` | Main text color |
| `--space-small` | `8px` | Small spacing |
| `--space-medium` | `16px` | Medium spacing |
| `--space-large` | `32px` | Large spacing |
| `--font-size-small` | `14px` | Small text |
| `--font-size-medium` | `16px` | Normal body text |
| `--font-size-large` | `24px` | Section headings |

## 7. How to Change a Variable and Test It

Follow these steps to verify that the design tokens work correctly.

1. Open `style.css` in Visual Studio Code.
2. Find the `:root` block at the top of the file.
3. Locate this variable:

```css
--color-primary: #2563eb;
```

4. Change it to:

```css
--color-primary: #7c3aed;
```

5. Save the file using `Ctrl + S`.
6. Refresh the webpage in Google Chrome.

### Expected result

The header, primary buttons, section headings, card accents, and other elements using `--color-primary` will change to the new purple color.

Similarly, change:

```css
--space-medium: 16px;
```

to:

```css
--space-medium: 24px;
```

After saving and refreshing, elements using `var(--space-medium)` will have increased spacing.

**Important:** Only elements that reference the changed variable will update. Elements with independently defined values will remain unchanged.

## 8. Steps to Run the Website

1. Open Visual Studio Code.
2. Create the `Assignment-5.4` folder.
3. Create `index.html` and paste the HTML code.
4. Create `style.css` and paste the CSS code.
5. Save both files.
6. Ensure both files are in the same folder.
7. Open `index.html` with Live Server or directly in Google Chrome.
8. Verify the colors, spacing, typography, buttons, and cards.
9. Change a variable in `:root` and observe the result.

## 9. Expected Output

The webpage should display:

- A colored header and navigation bar.
- Four color-token cards.
- Small, medium, and large spacing examples.
- Three different font sizes.
- Reusable primary and secondary buttons.
- Three cards using consistent design tokens.
- A responsive layout for mobile and desktop screens.
- Consistent styling controlled through CSS variables.

## 10. Result

The design-token stylesheet and sample webpage were successfully created using HTML and CSS. Reusable CSS variables were defined in `:root` for primary, secondary, background, and text colors; spacing; and font sizes. These variables were applied to headings, buttons, and cards. Changing a variable demonstrated how multiple elements can update consistently.

## 11. Submission

Submit the following files:

1. `index.html` — Sample webpage using the design tokens.
2. `style.css` — Stylesheet containing reusable CSS variables.
3. `Assignment-5.4.md` — Assignment documentation.

