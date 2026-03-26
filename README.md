# CoreSense General Meeting – Madrid, URJC Aranjuez

**Website:** https://coresenseeu.github.io/Coresense-Madrid-General-Meeting/

This repository contains the static website for the **CoreSense Horizon Europe project General Meeting**, hosted at Universidad Rey Juan Carlos (URJC), Campus de Aranjuez, on **27–28 May 2026**.

The site has three pages:

| File | Description |
|---|---|
| `index.html` | Home page – overview, dates, location, consortium |
| `organization.html` | Attendees list, 2-day agenda, and meals/dietary table |
| `venue.html` | Campus map, travel directions, hotels, and social activity sign-up |

---

## Requirements

- Git
- Python 3 (to preview the site locally)

---

## Clone the repository

1. On GitHub, open the repository and copy the URL from the **Code** button.
2. Clone it on your machine:

```bash
git clone <REPOSITORY_URL>
cd Coresense-Madrid-General-Meeting
```

---

## Preview locally

Since this is a static website, serve it with Python's built-in web server from the project root:

```bash
python3 -m http.server 8000
```

Then open your browser at:

- http://localhost:8000/index.html

Press `Ctrl+C` to stop the server.

---

## Contributing via Pull Request

All updates (attendees, agenda, dietary preferences, social activity sign-up) are made by editing the HTML files and opening a Pull Request. If you are not familiar with GitHub, follow the steps below.

### 1) Fork the repository

Go to the repository on GitHub and click **Fork** (top-right corner). This creates your own copy under your account.

### 2) Clone your fork

```bash
git clone <YOUR_FORK_URL>
cd Coresense-Madrid-General-Meeting
```

### 3) Create a branch for your changes

Never work directly on `main`. Create a descriptive branch:

```bash
git checkout -b add-yourname-attendee
```

### 4) Edit the relevant file and test locally

See the sections below for exactly which file and which table to edit.  
Once edited, preview the result in your browser:

```bash
python3 -m http.server 8000
```

### 5) Commit and push

```bash
git status
git add -A
git commit -m "Add <Your Name> to attendees / meals / social activity"
git push -u origin add-yourname-attendee
```

### 6) Open the Pull Request

- Go to your fork on GitHub.
- GitHub usually shows a prompt to open a Pull Request from the new branch.
- If not, go to the **Pull requests** tab → **New pull request**.
- Ensure the **base repository** is the original and your branch is selected.
- Add a short description and submit.

The organisers will review and merge it.

---

## How to add yourself to the tables

### Attendees table (`organization.html`)

Find the following comment inside `<tbody>` of the attendees table:

```html
<!-- ADD NEW ATTENDEE – copy the <tr> block below and fill in -->
```

Copy the template `<tr>` block immediately below it and fill in your data:

```html
<tr>
  <td>Your Full Name</td>
  <td>Your Institution</td>
  <td>Your Country</td>
  <td><a href="mailto:you@example.com">you@example.com</a></td>
  <td>✓</td>  <!-- Day 1: ✓ or — -->
  <td>✓</td>  <!-- Day 2: ✓ or — -->
  <td></td>   <!-- Notes (optional) -->
</tr>
```

Column reference:

| Column | Description |
|---|---|
| Name | Your full name |
| Institution | Consortium partner (UPM, URJC, TU Delft, Fraunhofer IPA, PAL Robotics, IMR, CTU Prague) |
| Country | Country of your institution |
| E-mail | Contact e-mail (wrapped in `<a href="mailto:…">`) |
| Day 1 | Attending 27 May? Use `✓` or `—` |
| Day 2 | Attending 28 May? Use `✓` or `—` |
| Notes | Any relevant remark (optional) |

---

### Meals / dietary table (`organization.html`)

Find the comment:

```html
<!-- ADD NEW ENTRY – copy the <tr> block below and fill in -->
```

inside the meals table `<tbody>` and copy the template:

```html
<tr>
  <td>Your Full Name</td>
  <td>Your Institution</td>
  <td>Omnivore / Vegetarian / Vegan / Other</td>
  <td>Allergies or intolerances (or "None")</td>
  <td>✓</td>  <!-- Day 1 Lunch -->
  <td>✓</td>  <!-- Day 1 Dinner -->
  <td>✓</td>  <!-- Day 2 Lunch -->
  <td></td>   <!-- Notes (optional) -->
</tr>
```

Column reference:

| Column | Description |
|---|---|
| Name | Your full name |
| Institution | Your consortium partner |
| Dietary type | Omnivore / Vegetarian / Vegan / Other |
| Allergies / intolerances | List any, or write "None" |
| Day 1 Lunch | Use `✓` or `—` |
| Day 1 Dinner | Use `✓` or `—` |
| Day 2 Lunch | Use `✓` or `—` |
| Notes | Optional notes |

---

### Social activity sign-up (`venue.html`)

The social activity is a guided visit to the **Palacio Real de Aranjuez** on the afternoon of Day 2 (28 May, ~14:30 departure).

Find the comment inside the social-activity table `<tbody>`:

```html
<!-- ADD NEW ENTRY – copy the <tr> block below and fill in -->
```

and copy the template:

```html
<tr>
  <td>Your Full Name</td>
  <td>Your Institution</td>
  <td>Yes / No</td>  <!-- Attending the visit -->
  <td></td>          <!-- Special needs or notes (optional) -->
</tr>
```

Column reference:

| Column | Description |
|---|---|
| Name | Your full name |
| Institution | Your consortium partner |
| Attending visit | `Yes` or `No` |
| Special needs / notes | Mobility requirements or other needs (optional) |

---

## Repository structure

```
Coresense-Madrid-General-Meeting/
├── index.html          # Home page
├── organization.html   # Attendees, agenda, meals
├── venue.html          # Campus, travel, hotels, social activity
├── styles.css          # Shared stylesheet
└── img/
    ├── CoreSense-Logo.png
    └── Logo-URJC.svg
```
