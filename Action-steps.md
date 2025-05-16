# 10 Steps for Shopify Developers to Rebrand artcellarhouston.com

This guide provides Shopify developers with **10 actionable steps** to execute the SEO-focused rebranding and accessibility-driven redesign of **artcellarhouston.com** using the Dawn theme on Shopify. The steps focus on preserving SEO equity, optimizing for Houston-specific searches, ensuring WCAG compliance, and delivering a fast, user-friendly site. Each step includes technical details, Shopify-specific tools, and resources to streamline implementation.

---

## Objectives
- **Preserve SEO Performance:** Maintain rankings, traffic, and backlink value during the redesign.
- **Enhance Accessibility:** Ensure compliance with WCAG 2.1 Level AA for users with disabilities.
- **Optimize for Local SEO:** Boost visibility for Houston-based art and event searches.
- **Deliver a Fast, Mobile-Friendly Site:** Align with Google’s Core Web Vitals and mobile-first indexing.

---

## Key Considerations
Developers must address risks like broken redirects, crawl errors, and accessibility gaps. The Dawn theme’s clean structure supports SEO and accessibility but requires customization for contrast, alt text, and navigation. Shopify’s built-in tools (e.g., URL Redirects, SEO settings) and apps (e.g., accessiBe) simplify implementation.

---

## 10 Steps for Shopify Developers

### 1. Set Up the Dawn Theme in a Staging Environment
- **Action:** Install the Dawn theme and create a staging environment for development.
- **Details:**
  - Download Dawn from the Shopify Theme Store and apply it to a duplicate of the live store.
  - Use Shopify’s **preview mode** or a password-protected staging URL to test changes.
  - Initialize version control (e.g., Git) for theme files to track changes.
- **Why:** Staging prevents live site disruptions, and Dawn’s structure supports SEO and accessibility.
- **Tools/Resources:**  
  - [Shopify Theme Store: Dawn](https://themes.shopify.com/themes/dawn/styles/default)  
  - [Shopify: Preview Themes](https://help.shopify.com/en/manual/online-store/themes/preview)  
- **Timeline:** Day 1-2.

---

### 2. Implement Proper Heading Structure
- **Action:** Code a single `<h1>` tag per page and sequential `<h2>`, `<h3>` tags for sections.
- **Details:**
  - Edit Dawn’s Liquid templates (e.g., `main-page.liquid`, `product.liquid`) to ensure one `<h1>` for the main title (e.g., “Art Cellar Houston - Art Workshops”).
  - Use `<h2>` for section headers (e.g., “Upcoming Events”) and `<h3>` for subsections.
  - Validate with a screen reader (e.g., NVDA) to confirm logical navigation.
- **Why:** Proper headings improve SEO crawlability and accessibility for screen reader users.
- **Tools/Resources:**  
  - [Shopify: Liquid Templates](https://shopify.dev/docs/themes/liquid)  
  - [WCAG: Headings](https://www.w3.org/WAI/WCAG21/Understanding/info-and-relationships.html)  
- **Timeline:** Days 3-4.

---

### 3. Add Alt Text to Images
- **Action:** Implement descriptive alt text for all images in the theme and content.
- **Details:**
  - Update image tags in Liquid files (e.g., `{% render 'image' %}`) with `alt` attributes (e.g., `alt="Houston art class painting session"`).
  - For product images, use Shopify’s admin panel to add alt text via **Products > Media**.
  - For theme images (e.g., banners), edit `sections/image-banner.liquid` to include alt text dynamically.
- **Why:** Alt text boosts image SEO and ensures accessibility for visually impaired users.
- **Tools/Resources:**  
  - [Shopify: Add Alt Text](https://help.shopify.com/en/manual/products/product-media/add-alt-text)  
  - [Shopify: Theme Image Handling](https://shopify.dev/docs/themes/sections)  
- **Timeline:** Days 5-6.

---

### 4. Configure 301 Redirects for URL Changes
- **Action:** Set up 301 redirects for all changed URLs to preserve SEO equity.
- **Details:**
  - Use a redirect spreadsheet (from the SEO audit) mapping old URLs (e.g., `/painting-kits`) to new ones (e.g., `/art-kits`).
  - Implement redirects in Shopify Admin under **Online Store > Navigation > URL Redirects**.
  - Test redirects using a browser or **Redirect Checker** to ensure no 404 errors.
- **Why:** 301 redirects transfer link equity and prevent ranking losses.
- **Tools/Resources:**  
  - [Shopify: URL Redirects](https://help.shopify.com/en/manual/online-store/menus-and-links/url-redirects)  
  - [Redirect Checker](https://www.redirect-checker.org)  
- **Timeline:** Days 7-8.

---

### 5. Optimize Meta Tags and Structured Data
- **Action:** Add SEO-friendly meta tags and schema markup for pages and events.
- **Details:**
  - Edit `theme.liquid` to include dynamic meta titles and descriptions with Houston-specific keywords (e.g., `<title>Houston Art Classes | Art Cellar Houston</title>`).
  - Use Shopify’s **Metafields** to manage custom meta data for products and pages.
  - Add `LocalBusiness` and `Event` schema in JSON-LD format to `head` section (e.g., via `snippets/schema.liquid`).
- **Why:** Optimized meta tags and schema enhance click-through rates and rich snippet visibility.
- **Tools/Resources:**  
  - [Shopify: Metafields](https://help.shopify.com/en/manual/custom-data/metafields)  
  - [Schema Markup Generator](https://technicalseo.com/tools/schema-markup-generator)  
- **Timeline:** Days 9-10.

---

### 6. Ensure Mobile Responsiveness
- **Action:** Customize Dawn for mobile-first design and test responsiveness.
- **Details:**
  - Adjust CSS in `assets/base.css` to ensure fluid layouts (e.g., `max-width: 100%` for images).
  - Test on multiple devices using Shopify’s **Device Preview** or **BrowserStack**.
  - Verify mobile navigation (e.g., hamburger menu) is accessible via keyboard.
- **Why:** Mobile-first indexing is critical for SEO, and responsiveness improves UX.
- **Tools/Resources:**  
  - [Shopify: Theme Customization](https://shopify.dev/docs/themes/customization)  
  - [BrowserStack](https://www.browserstack.com)  
- **Timeline:** Days 11-12.

---

### 7. Enhance Page Speed
- **Action:** Optimize code and assets for fast loading times.
- **Details:**
  - Minify CSS/JavaScript in `assets/` folder using Shopify’s built-in minification or apps like **PageSpeed Optimizer**.
  - Convert images to WebP format and lazy-load them via `loading="lazy"` in `img` tags.
  - Test with **Google PageSpeed Insights** (aim for a score >80).
- **Why:** Page speed is a Google ranking factor and reduces bounce rates.
- **Tools/Resources:**  
  - [PageSpeed Optimizer](https://apps.shopify.com/page-speed-optimizer)  
  - [Google PageSpeed Insights](https://pagespeed.web.dev)  
- **Timeline:** Days 13-14.

---

### 8. Add Accessibility Features
- **Action:** Implement accessibility enhancements like skip-to-content links and ARIA landmarks.
- **Details:**
  - Add a skip-to-content link in `header.liquid` (e.g., `<a href="#main" class="skip-link">Skip to content</a>`).
  - Include ARIA landmarks in `theme.liquid` (e.g., `<nav role="navigation">`, `<main role="main">`).
  - Fix Dawn’s low-contrast navigation by updating `base.css` (e.g., `color: #000; background: #fff;` for 4.5:1 contrast).
- **Why:** Accessibility boosts SEO by improving UX and ensures WCAG compliance.
- **Tools/Resources:**  
  - [Shopify: Accessibility](https://help.shopify.com/en/manual/online-store/themes/customizing-themes/accessibility)  
  - [WCAG: Bypass Blocks](https://www.w3.org/WAI/WCAG21/Understanding/bypass-blocks.html)  
- **Timeline:** Days 15-16.

---

### 9. Integrate an Accessibility App
- **Action:** Install and configure an accessibility app like **accessiBe**.
- **Details:**
  - Add accessiBe via the Shopify App Store and embed its script in `theme.liquid` (e.g., in `<head>`).
  - Customize settings to auto-fix alt text, contrast, and keyboard navigation issues.
  - Test with **WAVE** to verify app effectiveness and address manual fixes.
- **Why:** Apps automate accessibility compliance, saving development time.
- **Tools/Resources:**  
  - [accessiBe for Shopify](https://accessibe.com/integrations/shopify)  
  - [WAVE](https://wave.webaim.org)  
- **Timeline:** Day 17.

---

### 10. Test and Deploy
- **Action:** Conduct thorough testing and deploy the redesigned site.
- **Details:**
  - Run SEO tests with **Google Search Console** (check crawl errors, sitemap submission).
  - Test accessibility with **WAVE** and keyboard navigation (Tab key).
  - Verify redirects, meta tags, and schema using **Redirect Checker** and **Rich Results Test**.
  - Deploy via Shopify Admin and monitor post-launch with **Google Analytics**.
- **Why:** Rigorous testing ensures a smooth launch with no SEO or accessibility issues.
- **Tools/Resources:**  
  - [Google Search Console](https://search.google.com/search-console)  
  - [Google Rich Results Test](https://search.google.com/test/rich-results)  
  - [Google Analytics](https://analytics.google.com)  
- **Timeline:** Days 18-20.

---

## Timeline Overview
- **Days 1-2:** Set up Dawn and staging environment.
- **Days 3-6:** Implement headings and alt text.
- **Days 7-10:** Configure redirects, meta tags, and schema.
- **Days 11-14:** Ensure mobile responsiveness and page speed.
- **Days 15-17:** Add accessibility features and app.
- **Days 18-20:** Test and deploy.

---

## Summary
These **10 steps** empower Shopify developers to rebrand **artcellarhouston.com** with minimal SEO disruption and maximum accessibility. By leveraging the Dawn theme, Shopify’s tools, and apps like accessiBe, developers can deliver a fast, mobile-friendly, and inclusive site optimized for Houston searches. Post-launch monitoring with Google Search Console and Analytics ensures ongoing success.

For additional guidance, consult:
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
