\# Accessibility \& Architecture Audit Report

\*\*Target Website:\*\* MyGov India (https://www.mygov.in/cookie-settings)  

\*\*Lighthouse Score:\*\* 89 / 100  

\*\*Audit Date:\*\* 2026-11-02



\---



\## Documented Accessibility Issues



\### Issue 1: Select elements do not have associated text labels

\- \*\*Component:\*\* Cookie Category Dropdown / Search Filter Selects (`All Categories`)

\- \*\*WCAG Criterion:\*\* WCAG 1.3.1 Info and Relationships (Level A) \& WCAG 4.1.2 Name, Role, Value

\- \*\*Evidence:\*\* Lighthouse audit flagged form `<select>` elements without explicit `<label>` tags or `aria-label` attributes.

\- \*\*Impact:\*\* Screen readers cannot announce the purpose of the selector to visually impaired users.

\- \*\*Remediation Priority:\*\* P0 (Critical)

\- \*\*Suggested Fix:\*\*

&#x20; ```html

&#x20; <label for="category-select" class="sr-only">Filter by Category</label>

&#x20; <select id="category-select" name="category">

&#x20;   <option value="all">All Categories</option>

&#x20; </select>

