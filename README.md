# Gopesh Pandey — Personal Portfolio

A blueprint-themed personal portfolio website built with **pure HTML & CSS** (no JavaScript).

## Live Preview

Open `index.html` directly in any browser — no build step required.

## Project Structure

```
wedev_project/
├── index.html   — full page structure and content
├── style.css    — all styling, theme, layout, animations
└── README.md    — this file
```

## Sections

| # | Section    | What it covers                                      |
|---|------------|-----------------------------------------------------|
| — | Navbar     | Sticky navigation with smooth scroll links          |
| — | Hero       | Animated blueprint grid background, intro text, CTAs|
| 01| About      | Bio, initials badge with pulsing ring               |
| 02| Skills     | Three cards — Languages, Tools, Learning            |
| 03| Projects   | Mall Billing System, Luhn Validator, Web Game       |
| 04| Education  | SST + BITS Pilani timeline                          |
| 05| Contact    | Email, GitHub, LinkedIn cards                       |
| — | Footer     | Roll number, build note                             |

## CSS Concepts Used (Syllabus Coverage)

| Syllabus Topic                        | Where it appears                                         |
|---------------------------------------|----------------------------------------------------------|
| HTML structure & semantic tags        | `<nav>`, `<section>`, `<article>`, `<footer>`            |
| CSS selectors & properties            | Throughout — colours, fonts, spacing                     |
| Box model (margin, border, padding)   | Every card, badge, button                                |
| Display & CSS units                   | `rem`, `vw`, `clamp()`, `%`, `px`                        |
| Flexbox                               | Navbar, hero CTA, skill lists, footer, timeline          |
| CSS Grid                              | About, skills, projects, contact sections                |
| Media queries & responsive design     | Tablet (≤900px) and phone (≤600px) breakpoints           |
| CSS positioning                       | `sticky` nav, `absolute` corners, `relative` sections    |
| Z-index & stacking                    | Hero grid overlay vs. content layer                      |
| Specificity & inheritance             | CSS custom properties (`--var`), cascade order           |
| Transitions & transforms              | Card hover lift (`translateY`), button colour swap       |
| Keyframe animations                   | `fadeUp`, `gridPan`, `pulse`                             |
| Pseudo-elements                       | `::before` / `::after` on cards, timeline, skill bullets |

## How to Answer TA Questions

**"Why did you choose this design?"**  
The blueprint drafting-table theme maps directly to the syllabus: the grid background demonstrates repeating gradients, every card visually expresses the box model, and the layout sections each target a specific CSS topic.

**"Explain the hero section layout."**  
The `.hero` uses `display: grid; place-items: center` to centre the content. The `.blueprint-grid` div sits behind it using `position: absolute; inset: 0`, and has a higher stacking order than the dark background but a lower `z-index` than `.hero-content`. The grid itself is two `repeating-linear-gradient` layers creating a graph-paper effect, animated with `@keyframes gridPan`.

**"How is the navbar sticky?"**  
`position: sticky; top: 0` keeps it in normal flow (unlike `fixed`) but pins it to the top once the user scrolls past it. `z-index: 100` ensures it sits above all section content.

**"How does the layout respond on mobile?"**  
Two `@media (max-width: ...)` blocks progressively simplify the layout: the two-column grids (about, contact) collapse to one column, button stacks vertically, and base spacing variables are overridden.

## Author

**Gopesh Pandey**  
Roll No. 26BCS10802  
Scaler School of Technology · CS & AI  
BITS Pilani · B.Sc. Honours  
[github.com/gopeshp588-commits](https://github.com/gopeshp588-commits) · [linkedin.com/in/gopesh-pandey-5b71b9434](https://www.linkedin.com/in/gopesh-pandey-5b71b9434/)
