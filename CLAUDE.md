# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains HTML email templates for SFR (religious organization). The templates are standalone HTML files with embedded CSS designed for email client compatibility.

## Project Structure

- **Email Templates**: Standalone HTML files in the root directory
  - `SFR_Calendar_email.html` - Calendar/event announcement template
  - `SFR_IMPACT_AUG16-2025_pastors.html` - Impact weekend template for pastors
  - `SFR_IMPACT_AUG16-2025_volunteers.html` - Impact weekend template for volunteers
- **Assets**: Image files used in templates
  - `banner.jpg`, `banner.png` - Header/banner images
  - `sfr_bg.png` - Background image

## Email Template Guidelines

### HTML/CSS Constraints
- Use inline CSS for better email client compatibility
- Tables for layout (email clients have limited flexbox/grid support)
- Max width of 600px for email containers
- Include MSO conditional comments for Outlook compatibility
- Use web-safe fonts (Arial, sans-serif fallbacks)
- Responsive design using media queries for mobile devices

### Template Structure
Each email template follows this pattern:
1. DOCTYPE html declaration
2. Meta tags including viewport for mobile
3. MSO conditional comments for Outlook
4. Embedded styles in `<style>` tag
5. Main container with max-width 600px
6. Table-based layout for content sections

### Testing Recommendations
When modifying templates:
1. Preview in browser at different viewport sizes
2. Test with actual email clients if possible
3. Ensure images have proper alt text
4. Verify all links are absolute URLs when deployed

## Common Tasks

### Creating New Email Template
- Copy an existing template as base
- Maintain the email-container structure
- Keep CSS embedded in the head
- Test responsive breakpoints at 600px

### Updating Event Information
- Event details are typically in table cells or styled divs
- Date containers use 50% width table cells for side-by-side layout
- Headers use dark blue background (rgb(9, 26, 59)) with white text

### Image Updates
- Banner images should maintain current dimensions
- Use appropriate image formats (PNG for graphics, JPG for photos)
- Consider file size for email delivery