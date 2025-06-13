# Prioritized Task List for HTML Improvements

This document outlines the key areas for improving the HTML codebase, based on a detailed analysis against project requirements.

## 1. Create Missing Pages

*   **Admin Panel:** Several critical pages are missing. The initial priority is to create basic HTML shells for:
    *   `3 Module Platform Operator Admin Panel/4 Asset Review & Approval Page.html`
    *   `3 Module Platform Operator Admin Panel/5 Token Issuance & Management Interface.html`
    *   `3 Module Platform Operator Admin Panel/6 Platform-Wide Transaction Monitoring.html`
    *   `3 Module Platform Operator Admin Panel/7 Reporting & Analytics Section.html`
    *   `3 Module Platform Operator Admin Panel/8 System ConfigurationSettings Page.html`
*   **Governance (Optional):** If proceeding with this module, pages like "Governance Proposal Listing" and "Proposal Detail & Voting Interface" would also need to be created.
*   **Solution for Missing Pages:** Develop basic HTML structures for these pages based on the detailed descriptions in `ui_tasks_and_stitch_prompts.md`.

## 2. Fix Critical Navigation & Implement Module Sidebars

*   **Issue:** Widespread use of placeholder links (`#` or `javascript:alert(...)`) prevents navigation. Module-specific sidebars are missing in Asset Owner and Investor dashboards.
*   **Solution:**
    *   Update `href` attributes in all HTML files to ensure correct relative linking between pages.
    *   Implement the described navigation sidebars in `1 Module Asset Owner Portal/0 Asset Owner Dashboard.html` and `2 Module Investor Portal & Marketplace/0 Investor Dashboard.html`.

## 3. Address Redundant Files

*   **Issue:** Duplicate files for the password reset flow in `0 Module User Authentication & Onboarding` (e.g., `2.1 Password Reset Flow.html` vs. `2.1 Password Reset Flow - Request.html`).
*   **Solution:** Consolidate by removing the generic versions and ensuring the more descriptively named files (`*- Request.html`, `*- Enter Code.html`, `*- Set New Password.html`) contain the complete and correct HTML.

## 4. Implement Core UI Features (Static or Minor JS enhancements)

*   **Issue:** Various static UI elements described in `ui_tasks_and_stitch_prompts.md` are missing or incomplete.
*   **Examples & Solutions:**
    *   **User Registration:** Add a visual placeholder for the password strength indicator.
    *   **Tokenization Configuration:** Change text inputs for "Sale Start/End Date" to `type="datetime-local"` for better usability.
    *   **Admin Tables (User Management, Asset Submissions):** Add input fields for missing date range filters.
    *   **Asset Submissions Queue:** Add a placeholder section for summary statistics.
    *   Ensure all forms have the input fields as detailed in the UI tasks.

## 5. Content & Structural Improvements (Recommendations & Placeholders)

*   **Issue:** Many pages lack specific content (images, chart visuals, detailed descriptive text) and could have accessibility enhancements.
*   **Solutions & Recommendations:**
    *   Insert HTML comments (`<!-- TODO: Add chart here -->` or `<!-- TODO: Insert image of asset -->`) in relevant sections to mark where dynamic content or specific visuals are needed.
    *   **Accessibility Note:** A future review for ARIA attributes (e.g., `aria-label`, `aria-describedby`) is recommended to improve accessibility, especially for forms and interactive elements.
    *   For pages like "Asset Status Tracking," where content changes based on status, ensure the HTML structure can accommodate these variations, even if the dynamic switching logic is future work.
