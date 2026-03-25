# Lab 11 — Accessible Custom Components (Accordion)

##  Objectives

- Identify missing accessibility requirements in a custom UI component  
- Apply the WAI‑ARIA Accordion Pattern  
- Add the required ARIA attributes to the HTML  
- Ensure the accordion is fully operable with keyboard and screen readers  
- Publish the accessible version on GitHub Pages  

---

##  What Was Updated

The JavaScript was already corrected in the updated repo, so no additional JS changes were required.

The following **ARIA attributes** were added to the HTML:

### On each accordion button:
- `aria-expanded`
- `aria-controls`

### On each accordion panel:
- `role="region"`
- `aria-labelledby`

These attributes ensure that assistive technologies correctly announce:

- Whether a section is expanded or collapsed  
- Which button controls which panel  
- Which heading labels each region  

---

##  Keyboard Accessibility

The accordion now supports the required keyboard interactions:

- **Tab / Tab+Shift** — Move focus between accordion headers  
- **Enter / Space** — Toggle the selected accordion section  
- **Arrow Up / Arrow Down** (Optional) — Move between accordion headers  
- **Home / End** (Optional) — Jump to the first or last header  

---

##  Testing

### Keyboard Testing
- Navigate using **Tab**, **Shift+Tab** ,**Enter**, and **Space**
- Confirm that focus order is logical and predictable  

### Screen Reader Testing
- Confirm that each header is announced as a button  
- Confirm that expanded/collapsed states are announced  
- Confirm that each panel is labeled correctly  

---

##  Published GitHub Pages Link

**Live Demo:**  
*([Fixed html](https://saramir26.github.io/CST8914-lab11-VB/))*  


---

##  Lab Questions

### **1. What keyboard function can you improve to increase usability?**

To improve usability, enable Arrow Up, Arrow Down, Home, and End to move focus between accordion headers. These interactions allow keyboard‑only users to navigate and operate the accordion efficiently.

### **2. What ARIA attributes were missing?**

The original accordion was missing several required ARIA attributes:

- `aria-expanded` on each header button  
- `aria-controls` to associate each button with its panel  
- `aria-labelledby` on each panel  
- Proper updates to ARIA states when panels open or close  

These attributes ensure screen readers correctly announce the accordion structure and state changes.

