## 2026-06-28 - [XSS Protection in InnerHTML Templates]
**Vulnerability:** Several templates were injecting user-controlled or database-sourced data (like `item.status`, `user.name`, and `con.name`) into `innerHTML` without sanitization, leading to potential Cross-Site Scripting (XSS) risks.
**Learning:** In a single-page application (SPA) using plain JavaScript and template literals to update the DOM via `innerHTML`, it's easy to overlook sanitization for variables that seem "safe" but could be manipulated in the database or during the user session.
**Prevention:** Always use a sanitization function (like the existing `esc()`) when injecting any dynamic data into `innerHTML`. Alternatively, use `textContent` for simple text updates to avoid HTML parsing altogether.
