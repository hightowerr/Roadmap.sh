# Semantic CV Foundation

This project provides a foundation for creating a semantically structured and machine-readable HTML CV that serves as a professional digital identity hub.

## Overview

A single HTML file that is:
1. **Semantically Structured**: Using HTML5 tags that convey meaning (`<header>`, `<section>`, `<article>`).
2. **Machine-Readable**: Enriched with Schema.org microdata so search engines and other tools can understand the content's context.
3. **Discoverable & Shareable**: Contains all necessary metadata for good SEO and rich social media previews.
4. **Future-Proof**: Built as a "template-ready" document that can be easily styled with CSS or integrated into static site generators.

## Setup

1. Clone this repository
2. Customize the `index.html` file with your personal information
3. Replace the profile image in the `images/` directory
4. Update the favicon if desired
5. Test the HTML with a validator
6. Deploy to your preferred hosting platform

## Detailed Setup and Customization Instructions

### Customizing Personal Information
1. Open `index.html` in a text editor
2. In the `<header>` section, update:
   - The `<h1>` element with `itemprop="name"` to your name
   - The paragraph with `itemprop="jobTitle"` to your current or target title
   - The contact information in the `<address>` element (email, LinkedIn, GitHub links)

### Customizing Career History
1. In the `<section id="career">`:
   - For each `<article itemprop="worksFor" itemscope itemtype="http://schema.org/Organization">`:
     - Update the `<h3 itemprop="name">` with the company name
     - Update the date range in the paragraph
     - Update the list items with your actual responsibilities and achievements

### Customizing Education
1. In the `<section id="education">`:
   - For each `<article itemprop="alumniOf" itemscope itemtype="http://schema.org/EducationalOrganization">`:
     - Update the `<h3 itemprop="name">` with your degree
     - Update the institution and dates in the paragraph

### Customizing Skills
1. In the `<section id="skills">`:
   - Update the definition list (`<dl>`) with your own skill categories and skills
   - Add or remove `<dt>` and `<dd>` pairs as needed

### Updating Metadata and SEO Elements
In the `<head>` section of `index.html`:
- Update the `<title>` tag with your name and title
- Update the meta description to reflect your professional summary
- Update the Open Graph tags (og:title, og:description, og:url, og:image) with your own information
- Update the canonical URL to your actual domain

### Adding Your Profile Image
1. Replace `images/profile.jpg` with your own professional headshot
2. Ensure the image is 1200x630px for optimal social sharing
3. Make sure the file is named `profile.jpg` or update the og:image meta tag accordingly

### Updating Last Updated Date
- In the footer, update the `<time>` element's `datetime` attribute and text content with the current date

## Validation and Testing

### HTML Validation
- Use the W3C HTML Validation Service at https://validator.w3.org/
- Ensure there are no errors or warnings

### Schema.org Validation
- Use Google Rich Results Test at https://search.google.com/test/rich-results
- Verify that your Person schema is correctly recognized

### Accessibility Testing
- Use the axe-core accessibility testing tool
- Test with screen readers to verify semantic structure

### Social Sharing Preview
- Use Facebook Sharing Debugger: https://developers.facebook.com/tools/debug/
- Use LinkedIn Post Inspector: https://www.linkedin.com/post-inspector/
- Verify that title, description, and image appear correctly

## Deployment

### GitHub Pages (Recommended)
1. Push your customized files to a GitHub repository
2. In repository settings, go to "Pages" and select the main branch
3. Your CV will be available at `https://<username>.github.io/<repository-name>/`

### Other Static Hosting
- Netlify, Vercel, or any static file hosting service
- Traditional web hosting (upload the `index.html` and associated assets)

### Local Testing
- Open `index.html` directly in your browser for local preview
- For more accurate testing, serve via a local web server

## Maintaining Your CV

Since this is a static implementation:
- Manual editing of HTML is required to update content
- For regular updates, consider keeping your information in a structured format (JSON) and using a simple script to regenerate the HTML

## Features

- **Semantic HTML5 structure** using proper header, main, section, article elements
- **Schema.org microdata** for enhanced search engine visibility
- **SEO optimization** with meta tags and descriptions
- **Social sharing support** with Open Graph tags
- **Responsive design** through viewport meta tag
- **Accessibility compliant** with proper heading structure and semantic markup
- **Cross-browser compatible** with standards-compliant HTML