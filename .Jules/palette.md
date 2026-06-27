# Palette's Journal - Critical UX Learnings

## 2025-05-15 - Improving Chat Bot Accessibility
**Learning:** Interactive elements implemented as `div` or `span` are invisible to screen readers and keyboard users unless explicitly given a role and tab index. Using semantic elements like `button` is always preferred. Focus management is crucial for modal-like experiences (like a chat window) to keep the user oriented.
**Action:** Always check if icon-only buttons have `aria-label` and if they are implemented using semantic `<button>` tags.
