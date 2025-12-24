# Personal Portfolio Setup Guide

This document contains the technical details of the Jekyll setup for `devanshu06.github.io`. This file is named `.md` but not tracked as a page/post, so it won't appear on your site.

## Core Configuration
- **Theme:** [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) (Remote Theme).
- **Skin:** `default`.
- **Collections:** 
  - `projects`: Defined in `_config.yml`. Files are stored in `_projects/`.
  - `posts`: Standard Jekyll blog posts stored in `_posts/`.

## Custom Styling & UI Fixes
All custom CSS is located in `_includes/head/custom.html`. Current hacks include:
1.  **Hiding Navigation:** Previous/Next buttons on projects and blogs are hidden via `.pagination` and `.page__nav { display: none !important; }`.
2.  **Hiding RSS:** Removed RSS icons from the footer.
3.  **Favicon:** Replaced the profile photo with a terminal icon (`assets/images/favicon.svg`) with a `#00ff00` green stroke.

## Features & Integrations
- **Cloudflare Analytics:** Script added to `_includes/head/custom.html`.
- **Project Structure:**
  - `projects.md`: Uses a Liquid loop to fetch from `site.projects`.
  - `_config.yml`: `defaults` are set to ensure `wide` layout and `author_profile: true` for all pages.
- **Future-Dating Fix:** If a project or blog post doesn't show up (404), ensure the `date` in front matter is not in the future (Jekyll won't build future-dated posts by default).

## Content Management
- **Adding Projects:** Create a new `.md` file in `_projects/`. Ensure it has `title`, `excerpt`, and `date`.
- **Adding Blogs:** Create a new `.md` file in `_posts/` with the format `YYYY-MM-DD-title.md`.

## Troubleshooting
- **Missing Projects:** Check `_config.yml` to ensure the `projects` collection is defined under `collections:`.
- **Broken Links:** Check `permalink` settings in front matter vs. the `blog_url` used in project files.
