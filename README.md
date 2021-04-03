# demo-one
A simple test repo for learning purposes.
Hello, my name is Tedwood. Fuchsia will be joining us soon.


Useful WordPress Functions

This is a list of useful WordPress functions that I often reference to enhance or clean up my sites. Please be careful and make backups.

- [Hide WordPress Update Nag to All But Admins](#hide-wordpress-update-nag-to-all-but-admins)
- [Utilize Proper WordPress Titles](#utilize-proper-wordpress-titles)
- [Create Custom WordPress Dashboard Widget](#create-custom-wordpress-dashboard-widget)
- [Remove All Dashboard Widgets](#remove-all-dashboard-widgets)
- [Include Navigation Menus](#include-navigation-menus)
- [Insert Custom Login Logo](#insert-custom-login-logo)
- [Modify Admin Footer Text](#modify-admin-footer-text)
- [Enqueue Styles and Scripts](#enqueue-styles-and-scripts)
- [Enqueue Google Fonts](#enqueue-google-fonts)
- [Modify Excerpt Length](#modify-excerpt-length)
- [Change Read More Link](#change-read-more-link)
- [Change More Excerpt](#change-more-excerpt)
- [Disable Emoji Mess](#disable-emoji-mess)
- [Remove Comments](#remove-comments)
- [Change Media Gallery URL](#change-media-gallery-url)
- [Create Custom Thumbnail Size](#create-custom-thumbnail-size)
- [Add Categories for Attachments](#add-categories-for-attachments)
- [Add Tags for Attachments](#add-tags-for-attachments)
- [Add Custom Excerpt to Pages](#add-custom-excerpt-to-pages)
- [Create a Global String](#create-a-global-string)
- [Support Featured Images](#support-featured-images)
- [Support Search Form](#support-search-form)
- [Excluding pages from search](#excluding-pages-from-search)
- [Disable XMLRPC](#disable-xmlrpcphp)
- [Escape HTML in Posts](#escape-html-in-posts)
-  performance](#load-heavy-3rd-party-scripts-later-for-better-performance)

## Hide WordPress Update Nag to All But Admins

```php
/**
 * Hide WordPress update nag to all but admins
 */
 
function hide_update_notice_to_all_but_admin() {
    if ( !current_user_can( 'update_core' ) ) {
        remove_action( 'admin_notices', 'update_nag', 3 );
    }
}
add_action( 'admin_head', 'hide_update_notice_to_all_but_admin', 1 );
```

## Utilize Proper WordPress Titles

Make sure to remove the `<title>` tag from your header.

```php
/**
 * Utilize proper WordPress titles
 */

add_theme_support( 'title-tag' );
```

## Create Custom WordPress Dashboard Widget

```php
/**
 * Create custom WordPress dashboard widget
 */
 
function dashboard_widget_function() {
    echo '
        <h2>Custom Dashboard Widget</h2>
        <p>Custom content here</p>
    ';
}

function add_dashboard_widgets() {
    wp_add_dashboard_widget( 'custom_dashboard_widget', 'Custom Dashoard Widget', 'dashboard_widget_function' );
}
add_action( 'wp_dashboard_setup', 'add_dashboard_widgets' );
```

