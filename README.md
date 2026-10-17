# c243490-JS.portfolio
The original version of my Jarin Sabah's portfolio code: Personal portfolio website of c-243490, Jarin Sabah, a CSE student at IIUC, built with HTML, CSS and JavaScript. Showcases projects, services and skills in a clean, responsive layout.
# Sabah — Personal Portfolio

A responsive personal portfolio website for **Sabah**, a Computer Science & Engineering student at the International Islamic University Chittagong (IIUC), aspiring software developer and UI/UX designer.

Built with plain **HTML, CSS and JavaScript** — no build step, no framework.

> Always learning. Always creating. Always growing.

---

## Sections

| Section | What it shows |
|---|---|
| **Home** | Intro, portrait, typing animation, rotating text ring, social links |
| **About** | Short bio, education, key numbers, interests |
| **Works** | Swipeable slider of 5 featured projects |
| **My Services** | Accordion with 4 services |
| **Skills** | Frontend, Backend and Design icons |
| **My Approach** | Personal philosophy |
| **Contact** | Message form |
| **Footer** | Logo, tagline, social links |

---

## Folder structure

```
sabah-portfolio/
├── index.html            # Page content (all sections)
├── README.md             # This file
└── assets/
    ├── css/
    │   └── styles.css    # All styling + responsive breakpoints
    ├── js/
    │   └── main.js       # Menu, typing text, slider, accordion, form, animations
    └── img/
        ├── logo.png          # "j." monogram (nav + footer)
        ├── favicon.png       # Browser tab icon
        ├── home-img.png      # Portrait on the home section
        └── work-img-1..5.png # Project preview images
```

---

## How to run

1. Unzip the project.
2. Double-click `index.html` to open it in your browser.

That's it. An internet connection is needed because fonts, icons and the helper libraries load from a CDN.

For live reload while editing, use the **Live Server** extension in VS Code (right-click `index.html` → *Open with Live Server*).

---

## Libraries used (loaded from CDN)

- [Remix Icon](https://remixicon.com/) — UI icons
- [Devicon](https://devicon.dev/) — technology icons in Skills
- [Swiper](https://swiperjs.com/) — project slider
- [Typed.js](https://github.com/mattboldt/typed.js) — typing text on Home
- [ScrollReveal](https://scrollrevealjs.org/) — scroll animations
- [EmailJS](https://www.emailjs.com/) — sending the contact form
- Google Fonts — Poppins and Syne

---

## Customise it

### Change the colours
Open `assets/css/styles.css` and edit the variables at the top (`:root`). The palette comes from the logo: charcoal `#2a2a2a` and warm off-white `#e6e5e1`.

### Change the text
Everything you read on the page lives in `index.html`. Search for the text you want to change and edit it.

- **Typing roles:** `strings` list in `main.js`, under *HOME TYPED JS*
- **Projects:** each project is one block inside the `work__swiper` section
- **Skills:** each skill is one `skills__item` — change the icon class and the name

### Replace project images
Swap `assets/img/work-img-1.png` … `work-img-5.png` with real screenshots, keeping the same file names. Use about a 3:2 shape (for example 1200 × 800 px).

### Update social links
In `index.html`, replace the `https://github.com/`, LinkedIn, Behance and Instagram links with your own profile URLs. They appear twice: in the Home section and in the footer.

### Add testimonials later
The testimonials section is left out until there is genuine feedback to show. When you have some, add a new section between *Approach* and *Contact*, plus its styles.

---

## Set up the contact form

The form works in two ways:

- **Before setup:** it opens the visitor's email app with the message filled in.
- **After setup:** it sends the message straight to your inbox using EmailJS.

To turn on EmailJS:

1. Create a free account at [emailjs.com](https://www.emailjs.com/).
2. Add an email service and a template. Use these template variables: `user_name`, `user_email`, `message`.
3. Open `assets/js/main.js`, find *CONTACT EMAIL JS*, and fill in:

```js
const EMAILJS_PUBLIC_KEY  = 'YOUR_PUBLIC_KEY',
      EMAILJS_SERVICE_ID  = 'YOUR_SERVICE_ID',
      EMAILJS_TEMPLATE_ID = 'YOUR_TEMPLATE_ID',
      FALLBACK_EMAIL      = 'your-email@example.com'
```

---

## Responsive design

The layout adapts to these screen sizes:

| Breakpoint | Layout |
|---|---|
| Under 540px | Phones — single column, slide-in menu |
| 540px and up | Large phones — wider menu, 2-column skills |
| 768px and up | Tablets — 2-column About and Contact, 2 projects per row |
| 1150px and up | Desktop — full top menu, 3 projects per row, custom cursor |
| 2048px and up | Large screens — slightly scaled up |

---

## Publish it for free

Any static host works. Two easy options:

- **GitHub Pages** — push the folder to a repository, then *Settings → Pages → Deploy from branch*.
- **Netlify** — drag and drop the project folder onto [app.netlify.com/drop](https://app.netlify.com/drop).

---

## Credits

- Design and content: Sabah
- Starter structure follows the Bedimcode responsive portfolio tutorial

&copy; 2026 Sabah. All rights reserved.
