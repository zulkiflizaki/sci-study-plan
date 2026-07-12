# School of Computing and Informatics Study Plan

# Academic Study Plan & Curriculum Tracker

An interactive, front-end dashboard designed to map out academic course pathways, monitor credit hour distributions, and visualize graduation scenarios. Built entirely with semantic HTML, CSS utility classes, and vanilla JavaScript.

Link to Repository: [https://github.com/zulkiflizaki/sci-study-plan](https://github.com/zulkiflizaki/sci-study-plan)

---

## 🚀 Features

* **Visual Curriculum Mapping:** Organized matrix layout displaying course codes, names, prerequisites, and semester-by-semester timelines.
* **Dynamic Scenario Tracking:** Built-in classes to toggle between different credit scenarios and elective combinations.
* **Zero Dependencies:** Pure vanilla HTML5 and CSS3. Lightweight, fast, and loads instantly without heavy frameworks.
* **Live Update Metadata:** Integrates directly with the GitHub REST API to fetch and display the exact date of your last repository push automatically.

---

## 🛠️ Tech Stack

* **Structure:** HTML5
* **Styling:** CSS3 (Custom grid/table layout with strict color-coded utility classes)
* **Dynamic Elements:** JavaScript (ES6+ Fetch API)

---

## 📦 Getting Started

### Prerequisites
To run this project locally, all you need is a modern web browser. 

### Installation
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/zulkiflizaki/sci-study-plan.git
   ```
2. Navigate into the project directory:
   ```bash
   cd sci-study-plan
   ```
3. Open `index.html` directly in any browser:
   ```bash
   # On macOS
   open index.html
   
   # On Linux
   xdg-open index.html
   
   # Or simply double-click the file in your file explorer
   ```

---

## ⚙️ Customization Guide

### 1. Connecting Your GitHub Repository
To ensure the **"Last Updated"** element correctly displays your own repository's push history, update the variables inside the `<script>` tag at the bottom of `index.html`:

```javascript
// Replace these with your details
const owner = "zulkiflizaki"; 
const repo = "sci-study-plan";   
```

### 2. Updating Course Data
Courses are arranged inside structured `<table>` rows. To add or modify a subject, locate the target semester block and update the table data cell (`<td>`):

```html
<tr>
  <td class="cell-code">SECJ1013</td>
  <td class="cell-black-normal">Programming Technique I</td>
  <td class="cell-credit">3</td>
</tr>
```

### 3. Styling Theme Classes
The visual hierarchy relies on explicit theme classes defined in the `<style>` block. You can change the dashboard flavor by modifying the core utility rules:
* `.cell-october-main` — Used for core engineering/science subjects.
* `.cell-credit-black` — Used for credit hour callouts.
* `.scenario-1` — Used for alternative elective configurations.

> ⚠️ **Note:** Ensure your color choices maintain proper accessibility contrast. If setting a background to dark or black (`#000000`), always pair it with `color: #ffffff !important;` to keep the text visible.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE). Feel free to fork it, modify it, and adapt it to your own university curriculum structure!
