# 📚 BCSBooks

A simple, responsive static website where B.Sc. Computer Science (BCS) students can browse subjects semester by semester and open PDF study material for each subject.

Built with plain **HTML, CSS and JavaScript**. No frameworks, no build step, no backend.

---

## ✨ Features

- **Landing page** with Home, About, Stream (semester selection) and Contact sections
- **Six semester pages** (F.Y, S.Y and T.Y BCS, Sem I to VI), each listing its subjects as cards
- **PDF links** for subjects (Google Drive), currently available for Semester V and VI
- **Responsive navbar** with a hamburger menu for mobile screens
- **Dark mode toggle** (on the Semester I page)
- **Scroll-reveal animations** on the home page (ScrollReveal)
- **Login / Register page** with an animated toggle between the two forms (UI only)
- **About page** describing the purpose of the site

---

## 🗂️ Project Structure

```
book/
├── index.html      # Home page (hero, about, semester cards, contact, footer)
├── about.html      # About Us page
├── login.html      # Login / Register UI (not linked from the navbar yet)
├── sem1.html       # Semester I subjects
├── sem2.html       # Semester II subjects
├── sem3.html       # Semester III subjects
├── sem4.html       # Semester IV subjects
├── sem5.html       # Semester V subjects (with PDF links)
├── sem6.html       # Semester VI subjects (with PDF links)
├── style.css       # Main styles (index and about pages)
├── about.css       # About page styles
├── login.css       # Login / Register styles
├── sem1.css        # Styles shared by all semester pages
├── script.js       # Navbar toggle, dark mode, ScrollReveal
└── *.jpg           # Images (image.jpg, img.jpg, img.jp.jpg, immg.jpg)
```

---

## 🎓 Semester and Subject Overview

| Semester | Class | Subjects |
|----------|-------|----------|
| I | F.Y BCS | C Programming, DBMS, Matrix Algebra, Descriptive Mathematics, Semiconductor Devices, Principles of Digital Electronics, Descriptive Statistics, Mathematical Statistics |
| II | F.Y BCS | Advanced C Programming, Relational Database, Linear Algebra, Graph Theory, Instrumentation System, Basics of Computer Organisation, Methods of Applied Statistics, Continuous Probability |
| III | S.Y BCS | Data Structures & Algorithms I, Software Engineering, Groups and Coding Theory, Numerical Techniques, Microcontroller Architecture, Digital Communication, English |
| IV | S.Y BCS | Data Structures & Algorithms II, Computer Networks, Computational Geometry, Operations Research, Embedded System Design, Wireless Communication, English |
| V | T.Y BCS | Operating System I, Computer Networks II, Data Science, Blockchain, Web Technology, Java I, Theoretical Computer Science, Python |
| VI | T.Y BCS | Operating System II, Software Testing, Web Technologies II, Data Analytics, Java II, Compiler Construction, Software Testing Tools |

---

## 🛠️ Tech Stack

| Purpose | Technology |
|---------|------------|
| Structure | HTML5 |
| Styling | CSS3 (CSS variables, Flexbox/Grid, Poppins font via Google Fonts) |
| Interactivity | Vanilla JavaScript |
| Icons | [Boxicons](https://boxicons.com/) (CDN) |
| Animations | [ScrollReveal](https://scrollrevealjs.org/) (CDN) |
| Extras | jQuery and Bootstrap 3 JS (CDN, loaded on About and Login pages) |

> An internet connection is needed for fonts, icons and animations, since they load from CDNs.

---

## 🚀 Getting Started

1. **Download or clone** the project folder.
2. **Open `index.html`** in any modern browser (double-click it), or serve it locally:

   ```bash
   # Python
   cd book
   python -m http.server 8000
   # then visit http://localhost:8000
   ```

   Or use the **Live Server** extension in VS Code.

No installation or build step is required.

---

## ➕ Adding or Updating Study Material

1. Upload the PDF to Google Drive and set sharing to **Anyone with the link**.
2. Open the matching semester file (for example `sem1.html`).
3. Find the subject card and set the link:

   ```html
   <a href="YOUR_GOOGLE_DRIVE_LINK"><h2>Subject Name</h2></a>
   ```

4. Save and refresh the page.

---

## ⚠️ Known Issues and Future Improvements

- **PDF links missing** for Semesters I to IV, and some in III and VI (`href=""` or `#`).
- **`script.js` error on the home page:** it looks for a dark mode button (`#darkmode`) that only exists in `sem1.html`, so on `index.html` the script stops with an error and scroll animations may not run. Fix by wrapping the dark mode code in a null check.
- **Scripts not loaded on semester pages:** `sem1.html` to `sem6.html` do not include `script.js`, so the hamburger menu and dark mode toggle do not work there.
- **Navbar links on inner pages** all point to `index.html` instead of the specific sections (`index.html#about`, and so on).
- **Login page is UI only:** there is no backend or validation, the password field uses `type="text"` (should be `type="password"`), and the page is not linked from the main navigation.
- **Typos in subject names** (for example "Reletional", "Instrumation", "Therotical", "Embeded") should be corrected.
- **Duplicate image files:** `img.jpg` and `img.jp.jpg` are identical.
- **Footer links** (Privacy Policy, Disclaimer, Terms of Use) are placeholders.
- Consider adding a **search bar** for subjects and a **real authentication system** in future.

---

