# ArtCellarHouston-ReBrand

# Actionable Plan for Re-Theming artcellarhouston.com for Accessibility

This plan will guide you through the first 20 steps to make **artcellarhouston.com** a leader in accessibility among its competitors. Each step is practical, specific, and supported by resources to help you execute it effectively.

---

## Step 1: Choose an Accessible Shopify Theme
- **Action:** Select the **Dawn theme** as the foundation for your re-theming process.
- **Why:** Dawn is a free Shopify theme designed with structured content sequencing, making it easier for screen readers to navigate.
- **Resource:** [Dawn Theme on Shopify](https://themes.shopify.com/themes/dawn/styles/default)

---

## Step 2: Implement Proper Heading Structure
- **Action:** Use a single `<h1>` tag for the main page title and sequential `<h2>`, `<h3>`, etc., for subsections.
- **Why:** A logical heading hierarchy helps screen reader users understand the page structure.
- **Resource:** [Shopify: Accessibility for Themes](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility)

---

## Step 3: Add Alt Text to All Images
- **Action:** Add descriptive alt text to every image (e.g., "abstract painting of a sunset").
- **Why:** Alt text enables visually impaired users to understand image content via screen readers.
- **Resource:**  
  - [Add Alt Text to Product Images](https://help.shopify.com/en/manual/products/product-media/add-alt-text)  
  - [Add Alt Text to Other Images](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility/adding-alt-text)

---

## Step 4: Ensure Color Contrast Meets Standards
- **Action:** Adjust colors to achieve a contrast ratio of at least 4.5:1 for body text and 3:1 for headings.
- **Why:** Sufficient contrast improves readability for users with low vision.
- **Resource:** [Contrast Ratio Checker](https://contrast-ratio.com)

---

## Step 5: Add a Skip-to-Content Link
- **Action:** Include a "skip to content" link at the top of each page, targeting the main content area (e.g., `#main`).
- **Why:** This allows keyboard users to bypass repetitive navigation links.
- **Resource:** [WCAG: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html)

---

## Step 6: Label All Form Fields
- **Action:** Ensure every form input (e.g., contact or checkout fields) has a visible, associated label.
- **Why:** Labels help screen readers identify the purpose of each field.
- **Resource:** [Shopify: Form Accessibility](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility)

---

## Step 7: Ensure Keyboard Navigation Support
- **Action:** Add visible focus indicators (e.g., outlines or highlights) to all interactive elements like buttons and links.
- **Why:** Focus indicators assist users who rely on keyboards instead of a mouse.
- **Resource:** [WCAG: Focus Visible](https://www.w3.org/WAI/WCAG21/Understanding/focus-visible.html)

---

## Step 8: Make Slideshows and Videos Accessible
- **Action:** Disable auto-play for slideshows and videos, and add controls to pause or stop them.
- **Why:** Auto-playing content can disorient users with cognitive or vestibular disorders.
- **Resource:** [W3C: Understanding Vestibular Disorders](https://a11yproject.com/posts/understanding-vestibular-disorders)

---

## Step 9: Provide Captions and Transcripts for Media
- **Action:** Add closed captions to videos and transcripts to audio content.
- **Why:** Captions and transcripts make multimedia accessible to deaf or hard-of-hearing users.
- **Resource:** [W3C: Captions and Transcripts](https://www.w3.org/WAI/media/av/captions/)

---

## Step 10: Use ARIA Landmarks for Navigation
- **Action:** Apply ARIA landmarks (e.g., `role="navigation"`, `role="main"`) to define key page regions.
- **Why:** ARIA landmarks improve screen reader navigation by identifying content areas.
- **Resource:** [W3C: ARIA Landmarks](https://www.w3.org/WAI/ARIA/apg/patterns/landmarks/)

---

## Step 11: Install an Accessibility App
- **Action:** Integrate an accessibility tool like **accessiBe** or **UserWay** into your Shopify store.
- **Why:** These apps automate fixes for common issues and help maintain compliance.
- **Resource:**  
  - [accessiBe for Shopify](https://accessibe.com/integrations/shopify)  
  - [UserWay for Shopify](https://userway.org/shopify)

---

## Step 12: Test with WAVE Accessibility Tool
- **Action:** Run an accessibility audit using the WAVE tool to identify errors and areas for improvement.
- **Why:** WAVE provides a detailed report to guide your accessibility enhancements.
- **Resource:** [WAVE Web Accessibility Evaluation Tool](https://wave.webaim.org)

---

## Step 13: Conduct Keyboard Navigation Testing
- **Action:** Test the entire website using only a keyboard to ensure all features are accessible.
- **Why:** This ensures usability for individuals with motor impairments.
- **Resource:** [Shopify: Accessibility Testing](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility)

---

## Step 14: Ensure Text Resizing and Readability
- **Action:** Set body text to at least 16px and avoid justified text alignment.
- **Why:** Larger, left-aligned text improves readability for users with visual impairments.
- **Resource:** [WCAG: Text Resizing](https://www.w3.org/WAI/WCAG21/Understanding/resize-text.html)

---

## Step 15: Make Links Visually Distinct
- **Action:** Style text links (e.g., underline or bold) to differentiate them from surrounding text.
- **Why:** Clear link styling helps users with cognitive impairments identify clickable elements.
- **Resource:** [WCAG: Link Purpose](https://www.w3.org/WAI/WCAG21/Understanding/link-purpose-in-context.html)

---

## Step 16: Avoid Opening Links in New Tabs
- **Action:** Configure links to open in the same tab unless linking to external sites (and warn users if so).
- **Why:** Keeping navigation predictable enhances user control and orientation.
- **Resource:** [Shopify: Accessibility Best Practices](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility)

---

## Step 17: Use Lighthouse for Continuous Testing
- **Action:** Integrate Lighthouse CI into your development workflow for automated accessibility checks.
- **Why:** Continuous testing prevents new accessibility issues during updates.
- **Resource:** [Lighthouse CI GitHub Action](https://github.com/GoogleChrome/lighthouse-ci)

---

## Step 18: Create an Accessibility Statement
- **Action:** Publish a page detailing your commitment to accessibility and how users can provide feedback.
- **Why:** This builds trust and meets transparency expectations.
- **Resource:** [Shopify Accessibility Statement](https://www.shopify.com/accessibility)

---

## Step 19: Train Staff on Accessibility
- **Action:** Provide training for your team on accessibility best practices and tools.
- **Why:** An informed team ensures accessibility remains a priority in all updates.
- **Resource:** [W3C: Web Accessibility Training](https://www.w3.org/WAI/training/)

---

## Step 20: Schedule Regular Accessibility Audits
- **Action:** Conduct quarterly accessibility audits using WAVE or similar tools.
- **Why:** Regular checks maintain compliance and address new issues promptly.
- **Resource:** [WAVE Web Accessibility Evaluation Tool](https://wave.webaim.org)

---

## Summary
By following these **20 steps**, you can re-theme **artcellarhouston.com** on Shopify to be a highly accessible website, offering an inclusive experience for all users. Starting with the Dawn theme, addressing critical accessibility elements like headings, alt text, and keyboard navigation, and leveraging tools like accessiBe and WAVE, you’ll ensure compliance with WCAG standards. Ongoing testing and staff training will keep the site accessible long-term.

For additional support, consult Shopify’s [Accessibility for Themes](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility) and the [WCAG Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/). Let’s make **artcellarhouston.com** a standout example of accessibility in the art and events space!
