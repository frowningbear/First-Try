# demo-one
A simple test repo for learning purposes.
Hello, my name is Tedwood. Fuchsia will be joining us soon.


Useful WordPress Functions

This is a list of useful WordPress functions that I often reference to enhance or clean up my sites. Please be careful and make backups.

- [Section Title](#thelink)

## Hide WordPress Update Nag to All But Admins

```php
/**
 * Hide WordPress update nag to all but admins
 */
 
function something() {
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
 here</p>
    ';
}

function add_dashboard_widgets() {
    wp_add_dashboard_widget( 'custom_dashboard_widget', 'Custom Dashoard Widget', 'dashboard_widget_function' );
}
add_action( 'wp_dashboard_setup', 'add_dashboard_widgets' );
```

```javascript

function tedwood() {}

```
