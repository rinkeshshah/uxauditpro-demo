# Larkfield Coffee Roasters: a deliberately flawed demo

**Demo site with deliberate UX issues, used to test UXAuditPro. Not a real business.**

A fictional one-page site with known UX defects, used to test UXAuditPro's
`/uxaudit` skill end to end: audit, propose fixes, apply them after approval,
re-audit, compare. Nothing on the page is random or time-dependent, so two
audits of an unchanged page see exactly the same elements.

The broken state is tagged `broken`. To reset after a test run:
`git checkout broken -- . && git commit -am "Reset to broken" && git push`.

| # | Defect | Where |
|---|---|---|
| D1 | Text fails WCAG AA contrast: stat labels `#a3a3a3` on white (2.52:1) | `styles.css` `.stat-label` |
| D2 | Images with no `alt` attribute: logo and hero | `index.html` |
| D3 | Tap targets under 44x44px on mobile: logo, nav links, bean links, footer icons | `styles.css` |
| D4 | Nav links 0px apart on mobile | `styles.css` `.nav a` |
| D5 | Skip link stays 1x1px and is never revealed on focus | `styles.css` `.skip` |
| D6 | Hero has no call to action | `index.html` `.hero` |
