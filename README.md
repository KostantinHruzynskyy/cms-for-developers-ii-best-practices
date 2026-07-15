# CMS for Developers II: Best Practices — Practicum Theme

This theme extends the original CMS for Developers I practicum with performance,
accessibility, SEO, and theming best practices.

## What's in here

```
theme.json
fields.json                      # brand colors + header/footer bg (theme-level)
css/
  main.css                       # includes _layout.css
  _layout.css
templates/
  layouts/base.html              # base template with skip link + landmarks
  home-page.html                 # extends base.html, holds the 2 sections
partials/
  header.html
  footer.html
modules/
  image-and-text.module/         # your original module, unchanged
  team-member.module/            # NEW — includes required style field
sections/
  image-and-text-section.html
  team-members-section.html
images/
  sections-preview/              # placeholder screenshots — REPLACE THESE
```

## Things you still need to do

1. **Replace the placeholder screenshots** in `images/sections-preview/` with
   real screenshots taken from the HubSpot page editor once each section
   renders correctly — the practicum requires actual previews.
2. **Verify brand color inheritance.** The `fields.json` color fields are set
   up to reference your account's brand palette, but you should open each
   color field in the Design Manager and confirm the "Inherit from brand
   settings" option is toggled on — this is a UI setting as well as a JSON one.
3. **Swap in your real header/footer/base template** if your original CMS I
   practicum had custom navigation, logo handling, or footer content — the
   versions here are minimal scaffolds that satisfy the landmark/skip-link
   requirements but aren't customized to your brand.
4. **Add real team member content** (photos, names, roles, bios) via the
   page editor once the module is uploaded.
5. **Run Lighthouse + Axe DevTools** on the published page for accessibility,
   performance, and SEO, and fix anything that doesn't hit the required scores
   (100 accessibility, 90+ performance, pass SEO) on both desktop and mobile.
6. **Set page title + meta description** in the page editor's SEO tab.
7. Test 200% zoom reflow and tab order manually, as required.

## Uploading to HubSpot

Use the HubSpot CLI:
```
hs upload cms-devii-theme cms-devii-theme
```
