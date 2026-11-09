# YourCookieBanner for Google Tag Manager

The official [YourCookieBanner](https://yourcookiebanner.com) tag template for Google Tag Manager, with Google Consent
Mode v2.

## What it does

- Sets every consent type (`ad_storage`, `analytics_storage`, `ad_user_data`, `ad_personalization`,
  `functionality_storage`, `personalization_storage`, `security_storage`) to **denied** before any other tag runs.
- Loads the YourCookieBanner banner for your website.
- Passes each visitor's choice to Tag Manager (`updateConsentState`), also a choice stored on an earlier visit, so
  Google tags and tags with consent settings follow it.

## Installation

1. In Google Tag Manager, add the template from the Community Template Gallery (search for "YourCookieBanner"), or
   import `template.tpl` under **Templates → Tag templates → New → ⋮ → Import**.
2. Create a tag of the type **YourCookieBanner**.
3. **Site ID:** the part of your YourCookieBanner install code between `/s/` and `.js` (for example
   `cb_abc123def456`). You find it in your dashboard, on your website's page under *Installation*.
4. Trigger: **Consent Initialization - All Pages**. Not "All Pages": the banner must run before every other tag.
5. Give other tags (LinkedIn, Hotjar, …) the right consent under *Advanced settings → Consent settings*.
6. Preview with Tag Assistant, then publish.

Scripts that sit in your website outside Tag Manager (for example from a WordPress plugin) cannot be held back from
within Tag Manager. Load those through Tag Manager, or place the YourCookieBanner code first in your site's `<head>`
instead of using this template.

## Settings

| Setting | Default | Meaning |
|---|---|---|
| Site ID | – | Your website's id at YourCookieBanner (required). |
| Wait for the visitor's choice (milliseconds) | 500 | How long Google tags wait for the banner before they use the defaults. |
| Ads data redaction | on | Removes ad identifiers from Google Ads requests while ads consent is denied. |
| URL passthrough | off | Passes click identifiers through links while consent is denied. |

## Support

https://yourcookiebanner.com · info@yourcookiebanner.com
