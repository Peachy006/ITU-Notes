# Website Launch Checklist

## Before You Flip the Switch

- [x] Set a custom 404 page and check all internal links work
- [ ] Add a `robots.txt` and `sitemap.xml`
- [x] Set proper `<title>` and `<meta description>` tags on every page
- [ ] Add Open Graph / Twitter card meta tags
- [ ] Set up HTTPS (SSL certificate)
- [ ] Check mobile responsiveness and Core Web Vitals (Lighthouse in Chrome DevTools)
- [ ] Set up canonical URLs for duplicate/similar pages
- [ ] Add favicon

## Getting Indexed / Recommended by Google

- [ ] Register the site in Google Search Console (verify via DNS, HTML file, or meta tag)
- [ ] Submit `sitemap.xml` in Search Console
- [ ] Use "URL Inspection" tool to request indexing for main pages
- [ ] Register in Bing Webmaster Tools
- [ ] Add structured data (JSON-LD / schema.org markup) for rich snippets

## Analytics & Monitoring

- [ ] Set up Google Analytics 4 or privacy-friendly alternative (Plausible, Umami)
- [ ] Set up uptime monitoring (e.g. UptimeRobot)
- [ ] Set up error tracking for complex apps (e.g. Sentry)

## Security / Infra Basics

- [ ] Confirm no secrets/env variables exposed in client-side code or git history
- [ ] Configure CORS correctly for separate frontend/backend
- [ ] Add rate limiting on public API endpoints
- [ ] Configure backups for the database