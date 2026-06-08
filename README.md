# Inclusive Design: Accessibility-First Dublin Travel Documentation

A front-end web application built during a 3-week intensive study abroad program in Dublin, Ireland. The project serves a dual purpose: it acts as a professional, Irish-themed travel documentation platform while functioning as a rigorous exercise in programmatic accessibility. The interface is engineered to remain completely usable under severe assistive technology and user preference constraints, including total blindness, screen reader dependency, motor impairments, and motion sensitivity.

## Core Objective

The central challenge of this project was balancing a vibrant, culturally rich design with strict compliance to Web Content Accessibility Guidelines (WCAG) 2.1 AA and AAA standards. Rather than treating accessibility as an afterthought, the application was built from the ground up to ensure that visual styling, high-contrast Irish color palettes, and interactive media never compromised structure, keyboard navigation, or screen reader compatibility.

## Tech Stack and Testing Tools

* **Languages:** HTML5, CSS3, Vanilla JavaScript
* **Audit Tools:** WAVE (Web Accessibility Evaluation Tool), Deque aXe, Lighthouse
* **Assistive Tech Testing:** NVDA (NonVisual Desktop Access), VoiceOver, Manual Keyboard/Switch Sequential Mapping

## Accessibility Architecture and Implementation Features

### 1. Visual Accommodations and Theme Control

* **High-Contrast Irish Aesthetic:** Developed a professional, emerald-and-gold visual theme that meets or exceeds WCAG contrast minimums (4.5:1 for body text, 3:1 for large components), ensuring text remains completely legible against background elements.
* **Native Dark Mode Toggle:** Implemented a system-preferred and manual dark mode theme switch using CSS custom properties, providing a low-fatigue viewing experience for users with light sensitivity.
* **Reduced Motion Architecture:** Integrated a `prefers-reduced-motion` media query pipeline that automatically disables or minimizes CSS transitions and animations across the travel logs for users with vestibular or motion disorders.

### 2. Non-Visual Navigation and Media Integrity

* **Contextual Alt Text:** Authored descriptive, non-redundant alternative text for all imagery capturing Dublin's landmarks, ensuring blind and low-vision users receive equivalent contextual information.
* **Semantic Landmark Anchoring:** Structured the travel platform using explicit HTML5 elements (`<main>`, `<nav>`, `<header>`, `<article>`) to allow screen readers to jump fluidly across journal entries without getting lost in generic containers.
* **ARIA Live Regions:** Configured `aria-live="polite"` regions on dynamic components, ensuring that state changes (such as switching between dark/light modes or filtering entries) are announced audibly without disrupting user focus.

### 3. Keyboard Operability and Motor Controls

* **Keyboard-Only Traversal:** Assured 100% functionality of the application without a mouse. All interactive components, links, and forms are fully focusable via sequential `Tab` key navigation.
* **Visible Focus Management:** Designed custom, high-visibility focus indicators that distinctly outline active components, replacing default browser focus rings with high-contrast borders optimized for low-vision and keyboard-only users.
* **Skip-to-Content Routing:** Programmed an accessible bypass mechanism at the top of the DOM structure, letting alternative-input users skip the global header navigation to read the primary travel logs instantly.

## Audit and Validation Performance

To validate the codebase against automated and manual benchmarks, the application underwent iterative testing pipelines:

| Metric / Audit | Baseline (Day 3) | Shipped Target |
| :--- | :--- | :--- |
| **Lighthouse Accessibility Score** | 74 / 100 | **100 / 100** |
| **aXe Automated Violations** | 14 Alerts | **0 Violations** |
| **WAVE Contrast Errors** | 8 Failures | **0 Failures** |
| **Keyboard Operability** | Focus traps present | **Full sequential coverage** |

## Key Takeaways from Dublin

Developing this software in an intensive, international ecosystem highlighted that professional visual design and deep accessibility are not mutually exclusive. By leveraging semantic markup, flexible layouts, and modern CSS media features, it is entirely possible to capture a specific regional theme while honoring the diverse needs of all web users.

---

### How to Run the App Locally

Use this link: 
