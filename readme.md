# ISC Twenty Eleven

- Contributors: wordpressdotorg
- Requires at least: WordPress 3.2
- Tested up to: WordPress 5.0
- Requires PHP: 5.2.4
- Stable tag: 3.3
- License: GPLv2 or later
- License URI: http://www.gnu.org/licenses/gpl-2.0.html
- Tags: blog, one-column, two-columns, left-sidebar, right-sidebar, custom-background, custom-colors, custom-header, custom-menu, editor-style, featured-image-header, featured-images, flexible-header, footer-widgets, full-width-template, microformats, post-formats, rtl-language-support, sticky-post, theme-options, translation-ready

## Content editors guide

### Integrating the sandbox

#### Insert the sandbox launch/login/registration widget

Use this shortcode:

```
[iris_eval_creds][openid_connect_generic_login_button][/iris_eval_creds]
```

This will handle logging in or registering the user with InterSystems SSO, launching the sandbox, and showing configuration settings.

#### Use sandbox settings info throughout the page

Use this shortcode:

```
[iris_eval_settings][/iris_eval_settings]
```

attributes:

- setting: one of `sandbox_ide_url`, `sandbox_smp`, `sandbox_isc_ip`, `sandbox_isc_port`, `sandbox_expires`, `sandbox_username`, or `sandbox_password`
- linktext: if the setting is a link (i.e. `sandbox_ide_url` or `sandbox_smp`), an \<a> tag is created, and the setting value becomes the href and this text will be in the anchor
- fallback: if the setting isn't found, output this

content:

- anything bracketed by this shortcode will be output at the end of processing

## Notes on Raj ISC modifications


## For SSO

Use OAuth plugin: https://github.com/daggerhart/openid-connect-generic

In `openid-connect-generic-login-form.php` modify the function `function make_login_button()` to have class attributes that work for our theme.

## For sandbox startup

This ["Update user meta using with ajax"](https://wordpress.stackexchange.com/questions/216140/update-user-meta-using-with-ajax) question helped me figure out how to save data obtained via Javascript to the Wordpress PHP layer.

## Production checklist

### Before copying

- Uncomment Drift

### After copy

- Change WordPress address and site address (in General -> Settings)
- Change SSO URLs
- Allow search engine indexing
- Remove debug flag from wp-config.php

## Description

Based on the Wordpress 2011 theme.

The 2011 theme for WordPress is sophisticated, lightweight, and adaptable. Make it yours with a custom menu, header image, and background -- then go further with available theme options for light or dark color scheme, custom link colors, and three layout choices. Twenty Eleven comes equipped with a Showcase page template that transforms your front page into a showcase to show off your best content, widget support galore (sidebar, three footer areas, and a Showcase page widget area), and a custom "Ephemera" widget to display your Aside, Link, Quote, or Status posts. Included are styles for print and for the admin editor, support for featured images (as custom header images on posts and pages and as large images on featured "sticky" posts), and special styles for six different post formats.

For more information about Twenty Eleven please go to https://codex.wordpress.org/Twenty_Eleven.

