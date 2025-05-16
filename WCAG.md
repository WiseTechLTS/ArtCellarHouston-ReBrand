# WCAG 2.1 Level AA Compliance for artcellarhouston.com Redesign

This guide provides Shopify developers with detailed **WCAG 2.1 Level AA compliance requirements** for the rebranding and redesign of **artcellarhouston.com** using the **Studio theme**. It outlines the Web Content Accessibility Guidelines (WCAG) principles, specific success criteria, and actionable steps to ensure the site is accessible to users with visual, auditory, motor, and cognitive disabilities. The focus is on integrating accessibility with SEO and addressing Studio theme-specific issues.

---

## Objectives
- **Achieve WCAG 2.1 Level AA Compliance:** Meet legal and ethical accessibility standards.
- **Enhance User Experience (UX):** Ensure inclusivity for all users, boosting SEO via reduced bounce rates.
- **Address Studio Theme Issues:** Fix known accessibility gaps (e.g., improper HTML tags, low contrast).
- **Support Houston Audience:** Ensure accessibility for local users, aligning with SEO goals.

---

## Key Considerations
WCAG 2.1 Level AA is the widely accepted standard for web accessibility, required by laws like the ADA and Section 508. The Studio theme has strengths (e.g., keyboard navigation, responsive design) but issues like improper HTML tags, low contrast, and non-hidden offscreen products require targeted fixes. Shopify’s tools and apps (e.g., accessiBe) can streamline compliance.

---

## WCAG 2.1 Overview
WCAG 2.1 is built on four principles (POUR):
1. **Perceivable:** Content must be presentable to users in ways they can perceive (e.g., text alternatives, captions).
2. **Operable:** Interface components must be operable (e.g., keyboard navigation, no time limits).
3. **Understandable:** Content must be understandable (e.g., clear language, predictable navigation).
4. **Robust:** Content must be compatible with assistive technologies (e.g., screen readers).

Level AA includes all Level A and AA success criteria, balancing feasibility and inclusivity. Below are key requirements and implementation steps for **artcellarhouston.com**, mapped to the 10 developer steps previously outlined.

---

## WCAG Compliance Details and Implementation

### 1. Perceivable Requirements
WCAG ensures users can perceive content regardless of sensory abilities.

#### Success Criteria
- **1.1.1 Non-text Content (Level A):** Provide text alternatives for non-text content (e.g., images).
- **1.4.1 Use of Color (Level A):** Don’t rely on color alone to convey information.
- **1.4.3 Contrast Minimum (Level AA):** Text contrast ratio of 4.5:1 (body) and 3:1 (large text/headings).
- **1.4.4 Resize Text (Level AA):** Text must resize up to 200% without loss of content or functionality.
- **1.4.5 Images of Text (Level AA):** Avoid images of text unless essential.

#### Implementation (Tied to Developer Steps)
- **Step 3: Add Image Alt Text**
  - **Action:** Add descriptive alt text to all images (e.g., `alt="Houston art workshop painting session"`) in Liquid templates (`sections/image-banner.liquid`) and Shopify Admin (**Products > Media**).
  - **Studio Issue:** Studio’s alt text is often repetitive or missing. Ensure unique, context-specific alt text.
  - **Tool:** [Shopify: Add Alt Text](https://help.shopify.com/en/manual/products/product-media/add-alt-text)
- **Step 8: Address Accessibility Issues**
  - **Action:** Fix Studio’s low contrast by updating `assets/base.css` (e.g., `color: #000; background: #fff;` for 4.5:1 ratio). Use **Contrast Ratio Checker** to verify.
  - **Action:** Ensure color isn’t the only indicator (e.g., underline links, not just color them).
  - **Tool:** [Contrast Ratio Checker](https://contrast-ratio.com)
- **Step 6: Ensure Mobile Responsiveness**
  - **Action:** Support text resizing by using relative units (e.g., `rem`, `vw`) in `base.css`. Test at 200% zoom.
  - **Studio Issue:** Studio’s input fields may not scale well. Adjust `font-size` and `padding`.
  - **Tool:** [BrowserStack](https://www.browserstack.com)

---

### 2. Operable Requirements
WCAG ensures users can interact with the site regardless of physical abilities.

#### Success Criteria
- **2.1.1 Keyboard (Level A):** All functionality must be accessible via keyboard.
- **2.4.1 Bypass Blocks (Level A):** Provide a skip-to-content link to bypass repetitive content.
- **2.4.4 Link Purpose (Level A):** Ensure link purpose is clear from context or text.
- **2.4.7 Focus Visible (Level AA):** Keyboard focus indicators must be visible.
- **2.5.3 Label in Name (Level AA):** Accessible names of controls match visible labels.

#### Implementation (Tied to Developer Steps)
- **Step 8: Address Accessibility Issues**
  - **Action:** Add a skip-to-content link in `header.liquid` (e.g., `<a href="#main" class="skip-link">Skip to content</a>`).
  - **Action:** Ensure all interactive elements (e.g., buttons, forms) have visible focus styles in `base.css` (e.g., `outline: 2px solid blue;`).
  - **Studio Issue:** Studio’s filter controls are non-compliant. Add `aria-label` to clarify purpose
