# Marketing Consultancy Website

A single-page, vanilla HTML/CSS/JS marketing consultancy site: hero section, testimonials, and a Formspree-powered enquiry form.

![Preview of the site's hero section](assets/preview.png)

**Live site**: https://contentflowdigital321-cell.github.io/marketingagency/

## Structure
- `index.html` — everything: markup, CSS (in a `<style>` block), and JS (in a `<script>` block).
- `assets/preview.png` — screenshot of the hero section for this README.

## Spec checklist (verified)
- **Hero**: full-viewport height, gradient background, bold headline + subheadline, CTA button that smooth-scrolls to the enquiry form, sticky nav with Home/Testimonials/Contact anchors.
- **Testimonials**: "What Our Clients Say" section, 3-card responsive grid (stacks to 1 column on mobile), quote + name + company/role + avatar placeholder, hover lift effect.
- **Enquiry form**: Name / Email / Company (optional) / Message fields. Submits via `fetch()` as JSON to `https://formsubmit.co/ajax/contentflowdigital321@gmail.com` with `Accept: application/json`. Handles submit in JS: prevents default, shows a "Sending…" state, then a success message on 200 or an inline error on failure. Client-side validation for required fields + email format.
- **General**: mobile-first and responsive (breakpoints at 768px / 600px / 480px), smooth scrolling for anchor nav links, cohesive color palette via CSS custom properties, Poppins from Google Fonts as the only external dependency.

## Enquiry form delivery
The form posts to [FormSubmit](https://formsubmit.co) at line ~613 in `index.html`, targeting `contentflowdigital321@gmail.com` directly — no account or form ID needed. The **first** submission ever sent to a given address triggers a one-time confirmation email from FormSubmit that must be clicked to activate delivery; submissions before that point are accepted by the API but not forwarded.

## Verification notes
Reviewed line-by-line against the spec above and opened directly in a browser to confirm: sticky nav + anchor scrolling, hero CTA scroll-to-form, testimonial card hover/responsive stacking, and form validation/submit states (empty-field error, invalid-email error, "Sending…" state, success/error messaging). No discrepancies found — no code changes were required.
