# 10 Steps for Shopify Developers to Rebrand artcellarhouston.com with Studio Theme

This guide provides Shopify developers with **10 actionable steps** to rebrand **artcellarhouston.com** on Shopify using the **Studio theme**. The steps focus on maintaining SEO rankings, optimizing for Houston-based art searches, and ensuring accessibility compliance with WCAG 2.1 Level AA. Each step includes technical details, Shopify-specific tools, and resources, tailored to the Studio theme’s characteristics.

---

## Objectives
- **Preserve SEO Equity:** Maintain rankings, organic traffic, and backlink value.
- **Enhance Accessibility:** Ensure compliance with WCAG for users with disabilities.
- **Optimize Local SEO:** Boost visibility for Houston-specific searches.
- **Deliver a Fast, Mobile-Friendly Site:** Align with Google’s Core Web Vitals and mobile-first indexing.

---

## Key Considerations
The Studio theme offers keyboard navigation compatibility and responsive design but has accessibility issues, such as improper HTML tags, low contrast, and non-hidden offscreen products. Developers must address these while leveraging Shopify’s tools (e.g., URL Redirects, Metafields) and apps (e.g., accessiBe) to streamline the rebrand.

---

## 10 Steps for Shopify Developers

### 1. Set Up Studio Theme in a Staging Environment
- **Action:** Install the Studio theme and create a staging environment for development.
- **Details:**
  - Download Studio from the Shopify Theme Store and apply it to a duplicated store or staging URL.
  - Use Shopify’s **preview mode** or a password-protected environment to test changes.
  - Initialize version control (e.g., Git) for theme files (`theme.liquid`, `sections/`, `assets/`).
- **Why:** Staging ensures no live site disruptions; Studio’s responsive design supports SEO and UX.
- **Tools/Resources:**  
  - [Shopify Theme Store: Studio](https://themes.shopify.com/themes/studio/styles/default)  
  - [Shopify: Preview Themes](https://help.shopify.com/en/manual/online-store/themes/preview)  
- **Timeline:** Days 1-2

---

### 2. Correct Studio’s Heading Structure
- **Action:** Implement one `<h1>` per page and sequential `<h2>`, `<h3>` tags, fixing Studio’s improper HTML tags.
- **Details:**
  - Edit Liquid templates (e.g., `main-page.liquid`, `product.liquid`) to ensure a single `<h1>` for the main title (e.g., “Art Cellar Houston - Art Workshops”).
  - Replace misused tags (e.g., `<div>` for headings) with proper `<h2>`, `<h3>` for sections like “Upcoming Events” or “Art Kits.”
  - Test with a screen reader (e.g., NVDA) to verify logical navigation.
- **Why:** Proper headings enhance SEO crawlability and accessibility for screen readers.
- **Tools/Resources:**  
  - [Shopify: Liquid Templates](https://shopify.dev/docs/themes/liquid)  
  - [WCAG: Headings](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html)  
- **Timeline:** Days 3-4

---

### 3. Add Alt Text to Images
- **Action:** Implement descriptive alt text for all images, addressing Studio’s alt text issues.
- **Details:**
  - Update image tags in Liquid files (e.g., `{% render 'image' %}`) with `alt` attributes (e.g., `alt="Houston art class painting session"`).
  - For product images, add alt text via Shopify Admin (**Products > Media**).
  - For theme images (e.g., banners), edit `sections/image-banner.liquid` to include dynamic alt text.
- **Why:** Alt text improves image SEO and ensures accessibility for visually impaired users.
- **Tools/Resources:**  
  - [Shopify: Add Alt Text](https://help.shopify.com/en/manual/products/product-media/add-alt-text)  
  - [Shopify: Theme Image Handling](https://shopify.dev/docs/themes/sections)  
- **Timeline:** Days 5-6

---

### 4. Configure 301 Redirects for URL Changes
- **Action:** Set up 301 redirects for all changed URLs to preserve SEO equity.
- **Details:**
  - Use a redirect spreadsheet from the SEO audit to map old URLs (e.g., `/painting-kits`) to new ones (e.g., `/art-kits`).
  - Implement redirects in Shopify Admin (**Online Store > Navigation > URL Redirects**).
  - Test redirects with **Redirect Checker** to confirm no 404 errors occur.
- **Why:** 301 redirects transfer link equity and prevent ranking losses.
- **Tools/Resources:**  
  - [Shopify: URL onRedirects](https://help.shopify.com/en/manual/online-store/menus-and-links/url-redirects)  
  - [Redirect Checker](https://www.redirect-checker.org)  
- **Timeline:** Days 7-8

---

### 5. Optimize Meta Tags and Structured Data
- **Action:** Add SEO-friendly meta tags and schema markup for pages and events.
- **Details:**
  - Edit `theme.liquid` to include dynamic meta titles and descriptions with Houston keywords (e.g., `<title>Houston Art Classes | Art Cellar Houston</title>`).
  - Use Shopify’s **Metafields** to manage custom meta data for products and pages.
  - Add `LocalBusiness` and `Event` schema in JSON-LD format to `head` via `snippets/schema.liquid`.
- **Why:** Optimized meta tags and schema boost click-through rates and rich snippets.
- **Tools/Resources:**  
  - [Shopify: Metafields](https://help.shopify.com/en/manual/custom-data/metafields)  
  - [Schema Markup Generator](https://technicalseo.com/tools/schema-markup-generator)  
- **Timeline:** Days 9-10

---

### 6. Ensure Mobile Responsiveness
- **Action:** Customize Studio for mobile-first design and test across devices.
- **Details:**
  - Adjust CSS in `assets/base.css` for fluid layouts (e.g., `max-width: 100%` for images).
  - Fix Studio’s filter control issues by ensuring mobile-friendly inputs (e.g., `input[type="checkbox"]` with clear labels).
  - Test with Shopify’s **Device Preview** or **BrowserStack** on multiple devices.
- **Why:** Mobile-first indexing is critical for SEO; Studio’s responsive design needs fine-tuning.
- **Tools/Resources:**  
  - [Shopify: Theme Customization](https://shopify.dev/docs/themes/customization)  
  - [BrowserStack](https://www.browserstack.com)  
- **Timeline:** Days 11-12

---

### 7. Enhance Page Speed
- **Action:** Optimize code and assets for fast loading times.
- **Details:**
  - Minify CSS/JavaScript in `assets/` using Shopify’s minification or **PageSpeed Optimizer**.
  - Convert images to WebP and add `loading="lazy"` to `img` tags for lazy loading.
  - Test with **Google PageSpeed Insights**, aiming for a score >80.
- **Why:** Page speed is a ranking factor and improves user retention.
- **Tools/Resources:**  
  - [PageSpeed Optimizer](https://apps.shopify.com/page-speed-optimizer)  
  - [Google PageSpeed Insights](https://pagespeed.web.dev)  
- **Timeline:** Days 13-14

---

### 8. Address Studio’s Accessibility Issues
- **Action:** Implement accessibility features, fixing Studio’s specific issues.
- **Details:**
  - Add a skip-to-content link in `header.liquid` (e.g., `<a href="#main" class="skip-link">Skip to content</a>`).
  - Include ARIA landmarks in `theme.liquid` (e.g., `<nav role="navigation">`, `<main role="main">`).
  - Fix low contrast in `base.css` (e.g., `color: #000; background: #fff;` for 4.5:1 ratio) and hide offscreen products from assistive tech (e.g., `aria-hidden="true"`).
- **Why:** Accessibility enhances SEO via better UX and ensures WCAG compliance.
- **Tools/Resources:**  
  - [Shopify: Accessibility](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility)  
  - [WCAG: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html)  
- **Timeline:** Days 15-16

---

### 9. Integrate an Accessibility App
- **Action:** Install and configure **accessiBe** to automate accessibility fixes.
- **Details:**
  - Add accessiBe via Shopify App Store, embedding its script in `theme.liquid` (`<head>`).
  - Configure settings to address Studio’s issues (e.g., alt text, contrast, keyboard navigation).
  - Test with **WAVE** to verify fixes and identify manual adjustments.
- **Why:** Automates compliance, reducing development time for accessibility.
- **Tools/Resources:**  
  - [accessiBe Shopify](https://accessibe.com/integrations/shopify)  
  - [WAVE](https://wave.webaim.org)  
- **Timeline:** Day 17

---

### 10. Test and Deploy
- **Action:** Conduct comprehensive testing and deploy the redesigned site.
- **Details:**
  - Test SEO with **Google Search Console** (crawl errors, sitemap submission).
  - Test accessibility with **WAVE** and keyboard navigation (Tab key).
  - Verify redirects, meta tags, and schema using **Redirect Checker** and **Rich Results Test**.
  - Deploy via Shopify Admin and monitor with **Google Analytics**.
- **Why:** Ensures a smooth launch with no SEO or accessibility issues.
- **Tools/Resources:**  
  - [Google Search Console](https://search.google.com/search-console)  
  - [Google Rich Results Test](https://search.google.com/test/rich-results)  
  - [Google Analytics](https://analytics.google.com)  
- **Timeline:** Days 18-20

---

## Timeline Overview
- **Days 1-2:** Set up Studio theme and staging.
- **Days 3-6:** Fix headings and add alt text.
- **Days 7-10:** Configure redirects, meta tags, and schema.
- **Days 11-14:** Ensure mobile responsiveness and page speed.
- **Days 15-17:** Address accessibility and install app.
- **Days 18-20:** Test and deploy.

---

## Summary
These **10 steps** guide Shopify developers to rebrand **artcellarhouston.com** using the Studio theme, ensuring SEO preservation, Houston-specific optimization, and WCAG compliance. By addressing Studio’s accessibility issues (e.g., HTML tags, contrast), leveraging Shopify tools, and using apps like accessiBe, developers can deliver a fast, inclusive, and search-friendly site. Post-launch monitoring with Google Analytics and Search Console ensures ongoing success.

For further guidance, consult:
- [Shopify Developer Docs](https://shopify.dev/docs)
- [Shopify SEO Guide](https://www.shopify.com/blog/shopify-seo)
- [WCAG Guidelines](https://www.w3.org/WAI/standards-guidelines/wcag/)

---

## Citations
- Shopify: Theme Customization
- Shopify: SEO Settings
- Shopify: Accessibility for Themes
- accessiBe: Shopify Integration
- Google: PageSpeed Insights
- WCAG: Understanding Guidelines
