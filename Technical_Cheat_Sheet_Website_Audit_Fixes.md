# Technical Cheat Sheet: Website Audit Fixes

**Internal Guide for UK Business Automations**  
*How to identify, diagnose, and fix every issue found in website audits*

---

## Table of Contents

1. [SEO Issues & Fixes](#seo-issues--fixes)
2. [AEO (AI Engine Optimization) Issues](#aeo-ai-engine-optimization-issues)
3. [Performance & Speed Issues](#performance--speed-issues)
4. [Mobile Responsiveness Issues](#mobile-responsiveness-issues)
5. [Accessibility Issues](#accessibility-issues)
6. [Social Media Integration Issues](#social-media-integration-issues)
7. [Google Business Profile Issues](#google-business-profile-issues)
8. [Technical Infrastructure Issues](#technical-infrastructure-issues)
9. [Content & Copywriting Issues](#content--copywriting-issues)
10. [Conversion Optimization Issues](#conversion-optimization-issues)

---

## SEO Issues & Fixes

### 1. Missing or Poor Title Tags

**How to Identify:**
- View page source (Ctrl+U)
- Look for `<title>` tag in `<head>` section
- Check if it's missing, too short (<30 chars), too long (>60 chars), or generic

**How to Fix:**
```html
<!-- Bad -->
<title>Home</title>

<!-- Good -->
<title>AI Automation Services for UK Businesses | UK Business Automations</title>
```

**Best Practices:**
- 50-60 characters optimal
- Include primary keyword near the beginning
- Include brand name
- Make it compelling and click-worthy
- Unique for every page

**Pricing Guide:**
- DIY: Free (client can edit themselves)
- Basic fix (5-10 pages): £150
- Comprehensive (20+ pages): £400-600

---

### 2. Missing or Poor Meta Descriptions

**How to Identify:**
- View page source
- Look for `<meta name="description" content="...">` in `<head>`
- Check if missing, too short (<120 chars), too long (>160 chars), or duplicate across pages

**How to Fix:**
```html
<!-- Bad -->
<meta name="description" content="Welcome to our website">

<!-- Good -->
<meta name="description" content="Save time and reduce costs with AI automation solutions designed for UK small businesses. Free consultation available. Get started today.">
```

**Best Practices:**
- 150-160 characters optimal
- Include primary keyword naturally
- Include a call-to-action
- Accurately describe page content
- Unique for every page

**Pricing Guide:**
- DIY: Free
- Basic fix (5-10 pages): £150
- Comprehensive (20+ pages): £400-600

---

### 3. Missing or Incorrect Header Tags (H1, H2, H3)

**How to Identify:**
- Inspect page with browser DevTools (F12)
- Look for heading hierarchy
- Check for: Missing H1, multiple H1s, skipped levels (H1 → H3), keyword stuffing

**How to Fix:**
```html
<!-- Bad -->
<h3>Welcome</h3>
<h1>Our Services</h1>
<h1>About Us</h1>

<!-- Good -->
<h1>AI Automation Services for UK Businesses</h1>
<h2>Our Core Services</h2>
<h3>Workflow Automation</h3>
<h3>AI Chatbots</h3>
<h2>Why Choose Us</h2>
```

**Best Practices:**
- One H1 per page (main topic)
- Logical hierarchy (H1 → H2 → H3)
- Include keywords naturally
- Describe content accurately

**Pricing Guide:**
- DIY: Free
- Restructure entire site: £300-800

---

### 4. Missing Alt Text on Images

**How to Identify:**
- Right-click images → Inspect
- Check for `alt=""` or missing alt attribute
- Use browser extension like WAVE or Axe

**How to Fix:**
```html
<!-- Bad -->
<img src="photo.jpg">
<img src="photo.jpg" alt="">

<!-- Good -->
<img src="ai-automation-dashboard.jpg" alt="AI automation dashboard showing workflow analytics and performance metrics">
```

**Best Practices:**
- Describe what's in the image
- Include keywords naturally (don't stuff)
- Keep under 125 characters
- Decorative images: use `alt=""`

**Pricing Guide:**
- DIY: Free
- Fix 20-50 images: £100-200
- Fix 100+ images: £300-500

---

### 5. Broken Links (404 Errors)

**How to Identify:**
- Use tools: Screaming Frog, Ahrefs, Google Search Console
- Manually click through site navigation
- Check for 404 errors in browser console

**How to Fix:**
- Update link to correct URL
- Remove link if page no longer exists
- Create 301 redirect from old URL to new URL

**Implementation:**
```html
<!-- Update broken link -->
<a href="/old-page">Link</a>
<!-- to -->
<a href="/new-page">Link</a>
```

**For redirects (in .htaccess for Apache):**
```apache
Redirect 301 /old-page https://example.com/new-page
```

**Pricing Guide:**
- Fix 1-10 links: £50-100
- Fix 20-50 links: £150-300
- Comprehensive audit + fix: £400-800

---

### 6. Missing or Incorrect Schema Markup (Structured Data)

**How to Identify:**
- Use Google's Rich Results Test: https://search.google.com/test/rich-results
- Check page source for `<script type="application/ld+json">`
- Look for missing Organization, LocalBusiness, Product, or Article schema

**How to Fix:**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "UK Business Automations",
  "image": "https://ukbusinessautomations.com/logo.png",
  "address": {
    "@type": "PostalAddress",
    "addressCountry": "GB"
  },
  "telephone": "+44-XXX-XXX-XXXX",
  "url": "https://ukbusinessautomations.com",
  "priceRange": "££"
}
</script>
```

**Best Practices:**
- Add Organization schema to homepage
- Add LocalBusiness schema if they have physical location
- Add Product schema for e-commerce
- Add Article schema for blog posts
- Validate with Google's tool

**Pricing Guide:**
- Basic schema (homepage): £200-300
- Comprehensive schema (all pages): £500-1,000

---

### 7. Missing Canonical Tags

**How to Identify:**
- View page source
- Look for `<link rel="canonical" href="...">`
- Check if missing or pointing to wrong URL

**How to Fix:**
```html
<head>
  <link rel="canonical" href="https://ukbusinessautomations.com/services">
</head>
```

**Best Practices:**
- Every page should have a canonical tag
- Point to the preferred version of the URL
- Use absolute URLs (not relative)
- Especially important for duplicate content

**Pricing Guide:**
- DIY: Free (add to template)
- Implementation: £150-300

---

### 8. Missing Sitemap or Robots.txt

**How to Identify:**
- Visit: `https://example.com/sitemap.xml`
- Visit: `https://example.com/robots.txt`
- Check Google Search Console for sitemap submission

**How to Fix:**

**Create sitemap.xml:**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://ukbusinessautomations.com/</loc>
    <lastmod>2026-02-14</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://ukbusinessautomations.com/services</loc>
    <lastmod>2026-02-14</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
</urlset>
```

**Create robots.txt:**
```
User-agent: *
Allow: /
Sitemap: https://ukbusinessautomations.com/sitemap.xml
```

**Pricing Guide:**
- Create sitemap + robots.txt: £100-200
- Submit to Google Search Console: £50

---

## AEO (AI Engine Optimization) Issues

### 9. Content Not Optimized for AI Search Engines

**How to Identify:**
- Test site in ChatGPT: "Tell me about [business name]"
- Test in Perplexity.ai: Search for business
- Check if AI can find and accurately describe the business

**How to Fix:**

**Add clear, structured content:**
```html
<section>
  <h1>What We Do</h1>
  <p>UK Business Automations helps small businesses in the United Kingdom implement AI-powered automation solutions. We specialize in workflow automation, AI chatbots, and business process optimization.</p>
  
  <h2>Our Services Include:</h2>
  <ul>
    <li>AI Chatbot Development - Custom conversational AI for customer service</li>
    <li>Workflow Automation - Streamline repetitive tasks with Make and Zapier</li>
    <li>Business Process Optimization - Identify and eliminate inefficiencies</li>
  </ul>
</section>
```

**Best Practices:**
- Use clear, descriptive language (not marketing fluff)
- Answer common questions directly on the page
- Use structured data (Schema.org)
- Include FAQ sections
- Write in complete sentences (not just keywords)
- Provide context (who, what, where, why, how)

**Pricing Guide:**
- Content audit + recommendations: £300-500
- Rewrite homepage for AEO: £400-600
- Comprehensive site rewrite: £1,500-3,000

---

### 10. Missing FAQ Section

**How to Identify:**
- Look for FAQ page or section
- Check if common questions are answered
- Test: Can AI find answers to "How much does [service] cost?"

**How to Fix:**
```html
<section class="faq">
  <h2>Frequently Asked Questions</h2>
  
  <div class="faq-item">
    <h3>How much do your services cost?</h3>
    <p>Our services start at £47 for self-paced courses, with done-for-you automation projects ranging from £500 to £5,000 depending on complexity. We offer a free consultation to discuss your specific needs.</p>
  </div>
  
  <div class="faq-item">
    <h3>How long does implementation take?</h3>
    <p>Simple automation projects typically take 1-2 weeks, while comprehensive business process automation can take 4-8 weeks. We provide a detailed timeline during the consultation.</p>
  </div>
</section>
```

**Add FAQ Schema:**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "How much do your services cost?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Our services start at £47 for self-paced courses..."
    }
  }]
}
</script>
```

**Pricing Guide:**
- Write 5-10 FAQs: £200-300
- Write 20+ FAQs with schema: £500-800

---

## Performance & Speed Issues

### 11. Slow Page Load Time (>3 seconds)

**How to Identify:**
- Use Google PageSpeed Insights: https://pagespeed.web.dev/
- Use GTmetrix: https://gtmetrix.com/
- Check Core Web Vitals in Google Search Console

**Common Causes & Fixes:**

**A. Unoptimized Images**
- Compress images (use TinyPNG, Squoosh)
- Convert to WebP format
- Use responsive images with `srcset`
- Lazy load images below the fold

```html
<img src="image.webp" 
     srcset="image-small.webp 400w, image-medium.webp 800w, image-large.webp 1200w"
     sizes="(max-width: 600px) 400px, (max-width: 1200px) 800px, 1200px"
     loading="lazy"
     alt="Description">
```

**B. Too Many HTTP Requests**
- Combine CSS files
- Combine JavaScript files
- Use CSS sprites for icons
- Remove unused plugins/scripts

**C. No Browser Caching**
Add to .htaccess:
```apache
<IfModule mod_expires.c>
  ExpiresActive On
  ExpiresByType image/jpg "access plus 1 year"
  ExpiresByType image/jpeg "access plus 1 year"
  ExpiresByType image/gif "access plus 1 year"
  ExpiresByType image/png "access plus 1 year"
  ExpiresByType text/css "access plus 1 month"
  ExpiresByType application/javascript "access plus 1 month"
</IfModule>
```

**D. No GZIP Compression**
Add to .htaccess:
```apache
<IfModule mod_deflate.c>
  AddOutputFilterByType DEFLATE text/html text/plain text/xml text/css application/javascript
</IfModule>
```

**Pricing Guide:**
- Image optimization (20-50 images): £150-300
- Full performance optimization: £500-1,200
- Ongoing monitoring (monthly): £100-200/month

---

### 12. Poor Core Web Vitals

**How to Identify:**
- Check Google Search Console → Core Web Vitals report
- Use PageSpeed Insights
- Metrics to check:
  - LCP (Largest Contentful Paint) - should be <2.5s
  - FID (First Input Delay) - should be <100ms
  - CLS (Cumulative Layout Shift) - should be <0.1

**How to Fix:**

**LCP (Slow Loading):**
- Optimize largest image/element
- Use CDN
- Implement lazy loading
- Reduce server response time

**FID (Slow Interactivity):**
- Minimize JavaScript execution
- Remove unused JavaScript
- Use code splitting
- Defer non-critical JavaScript

**CLS (Layout Shift):**
- Set width/height on images
- Reserve space for ads/embeds
- Avoid inserting content above existing content
- Use CSS aspect-ratio

```html
<!-- Prevent CLS -->
<img src="hero.jpg" width="1200" height="600" alt="Hero image">

<style>
  .video-container {
    aspect-ratio: 16 / 9;
  }
</style>
```

**Pricing Guide:**
- Fix one metric: £200-400
- Fix all Core Web Vitals: £600-1,200

---

## Mobile Responsiveness Issues

### 13. Not Mobile-Friendly

**How to Identify:**
- Use Google's Mobile-Friendly Test: https://search.google.com/test/mobile-friendly
- Manually test on phone
- Check for: Text too small, links too close, horizontal scrolling, viewport not set

**How to Fix:**

**Add viewport meta tag:**
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**Use responsive CSS:**
```css
/* Mobile-first approach */
.container {
  width: 100%;
  padding: 1rem;
}

/* Tablet */
@media (min-width: 768px) {
  .container {
    max-width: 750px;
    margin: 0 auto;
  }
}

/* Desktop */
@media (min-width: 1200px) {
  .container {
    max-width: 1140px;
  }
}
```

**Make buttons/links touch-friendly:**
```css
.button {
  min-height: 44px; /* Apple's recommended touch target */
  min-width: 44px;
  padding: 12px 24px;
}
```

**Pricing Guide:**
- Add viewport tag: £50
- Make existing site responsive: £800-2,500
- Build new responsive site: £2,000-8,000

---

## Accessibility Issues

### 14. Poor Color Contrast

**How to Identify:**
- Use WAVE tool: https://wave.webaim.org/
- Use browser extension: Axe DevTools
- Check contrast ratio (should be 4.5:1 for normal text, 3:1 for large text)

**How to Fix:**
```css
/* Bad - insufficient contrast */
.text {
  color: #999999;
  background: #ffffff;
}

/* Good - sufficient contrast */
.text {
  color: #333333;
  background: #ffffff;
}
```

**Use contrast checker:** https://webaim.org/resources/contrastchecker/

**Pricing Guide:**
- Fix color scheme: £200-500

---

### 15. Missing Form Labels

**How to Identify:**
- Inspect forms
- Check if every input has a `<label>` element
- Test with screen reader

**How to Fix:**
```html
<!-- Bad -->
<input type="text" placeholder="Name">

<!-- Good -->
<label for="name">Name:</label>
<input type="text" id="name" name="name" placeholder="Enter your name">
```

**Pricing Guide:**
- Fix all forms: £150-300

---

## Social Media Integration Issues

### 16. Missing Open Graph Tags

**How to Identify:**
- Share URL on Facebook/LinkedIn
- Check if correct image, title, description appear
- Use Facebook Sharing Debugger: https://developers.facebook.com/tools/debug/

**How to Fix:**
```html
<head>
  <!-- Open Graph -->
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://ukbusinessautomations.com/">
  <meta property="og:title" content="AI Automation Services for UK Businesses">
  <meta property="og:description" content="Save time and reduce costs with AI automation solutions.">
  <meta property="og:image" content="https://ukbusinessautomations.com/og-image.png">
  
  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:url" content="https://ukbusinessautomations.com/">
  <meta name="twitter:title" content="AI Automation Services for UK Businesses">
  <meta name="twitter:description" content="Save time and reduce costs with AI automation solutions.">
  <meta name="twitter:image" content="https://ukbusinessautomations.com/twitter-card.png">
</head>
```

**Image Requirements:**
- OG image: 1200x630px
- Twitter card: 1200x675px
- Format: JPG or PNG
- Max size: 8MB

**Pricing Guide:**
- Add OG tags: £100-200
- Create social media images: £150-300

---

## Google Business Profile Issues

### 17. Incomplete or Missing Google Business Profile

**How to Identify:**
- Search "[Business Name] near me" on Google
- Check if business appears in map results
- Check profile completeness

**How to Fix:**

**Claim/Create Profile:**
1. Go to https://business.google.com/
2. Search for business or create new
3. Verify ownership (postcard, phone, email)

**Optimize Profile:**
- Add complete business information
- Choose correct categories
- Add high-quality photos (10+)
- Write compelling description (750 chars)
- Add services with prices
- Enable messaging
- Post weekly updates
- Respond to all reviews

**Pricing Guide:**
- Setup + optimization: £300-600
- Monthly management: £200-400/month

---

## Technical Infrastructure Issues

### 18. No HTTPS (SSL Certificate)

**How to Identify:**
- Check if URL starts with `https://`
- Look for padlock icon in browser
- Check for "Not Secure" warning

**How to Fix:**
- Purchase SSL certificate from hosting provider (often free with Let's Encrypt)
- Install certificate
- Update all internal links to HTTPS
- Set up 301 redirects from HTTP to HTTPS

**Pricing Guide:**
- SSL certificate: Free-£100/year
- Installation + setup: £100-300

---

### 19. Missing Google Analytics

**How to Identify:**
- View page source
- Search for "gtag" or "analytics"
- Check if Google Analytics tracking code exists

**How to Fix:**
1. Create Google Analytics 4 property
2. Get Measurement ID (G-XXXXXXXXXX)
3. Add tracking code to all pages:

```html
<head>
  <!-- Google tag (gtag.js) -->
  <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
  <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-XXXXXXXXXX');
  </script>
</head>
```

**Pricing Guide:**
- Setup: £150-300
- Custom event tracking: £300-600

---

## Content & Copywriting Issues

### 20. Weak or Missing Call-to-Action (CTA)

**How to Identify:**
- Review homepage and key pages
- Check if clear next step is provided
- Look for: Generic CTAs ("Click here"), no urgency, no value proposition

**How to Fix:**
```html
<!-- Bad -->
<a href="/contact">Click Here</a>

<!-- Good -->
<a href="/contact" class="cta-button">
  Get Your Free AI Automation Audit (Worth £500)
</a>
```

**Best Practices:**
- Use action-oriented language
- Create urgency ("Limited spots available")
- Show value ("Free", "Save £500", "Get instant access")
- Make buttons stand out visually
- Place CTAs above the fold and throughout page

**Pricing Guide:**
- CTA copywriting: £150-300
- Design + implementation: £200-400

---

### 21. Thin or Duplicate Content

**How to Identify:**
- Check word count (should be 300+ words minimum)
- Use Copyscape to check for duplicate content
- Check if content provides value or is just filler

**How to Fix:**
- Expand thin content with useful information
- Rewrite duplicate content to be unique
- Add examples, case studies, data
- Answer user questions
- Include relevant keywords naturally

**Pricing Guide:**
- Rewrite single page: £200-500
- Comprehensive content audit: £500-1,000
- Full site content rewrite: £2,000-10,000

---

## Conversion Optimization Issues

### 22. No Contact Form or Difficult to Find

**How to Identify:**
- Try to find contact information
- Check if form exists and works
- Test form submission

**How to Fix:**
- Add contact form to every page (footer or header)
- Make "Contact" prominent in navigation
- Use form service (Web3Forms, Formspree, etc.)

```html
<form action="https://api.web3forms.com/submit" method="POST">
  <input type="hidden" name="access_key" value="YOUR_ACCESS_KEY">
  
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  
  <label for="message">Message:</label>
  <textarea id="message" name="message" required></textarea>
  
  <button type="submit">Send Message</button>
</form>
```

**Pricing Guide:**
- Add contact form: £150-300
- Custom form with validation: £300-600

---

### 23. Slow or No Response to Inquiries

**How to Identify:**
- Test by submitting form
- Check if confirmation email is sent
- Check response time

**How to Fix:**
- Set up email notifications
- Create auto-responder email
- Set up CRM integration (High Level, HubSpot)
- Implement chatbot for instant response

**Pricing Guide:**
- Email automation setup: £200-400
- Chatbot implementation: £500-1,500

---

## Quick Reference: Pricing Tiers

### DIY Tier (£0-50)
- Client implements fixes themselves with guidance
- Provide documentation and video tutorials

### Basic Fixes (£150-500)
- Title tags and meta descriptions
- Alt text for images
- Fix broken links
- Add contact form
- Install SSL certificate

### Standard Package (£500-1,500)
- All basic fixes
- Performance optimization
- Mobile responsiveness fixes
- Schema markup
- Google Analytics setup
- Social media integration

### Comprehensive Package (£1,500-5,000)
- All standard fixes
- Content rewrite for AEO
- Advanced performance optimization
- Accessibility compliance
- Google Business Profile optimization
- Ongoing support (3 months)

### Enterprise Package (£5,000+)
- Complete site rebuild
- Custom automation
- Advanced integrations
- Dedicated account manager
- 12 months support

---

## Tools & Resources

### Free Tools:
- Google PageSpeed Insights
- Google Search Console
- Google Analytics
- WAVE Accessibility Tool
- Mobile-Friendly Test
- Rich Results Test
- Contrast Checker

### Paid Tools (Worth Investing In):
- Screaming Frog (£149/year) - Technical SEO audits
- Ahrefs (£99+/month) - Comprehensive SEO tool
- SEMrush (£119+/month) - SEO & competitor analysis
- Hotjar (£39+/month) - User behavior tracking

---

**Last Updated:** February 2026  
**Version:** 1.0  
**Maintained by:** UK Business Automations
