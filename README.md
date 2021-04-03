# demo-one
A simple test repo for learning purposes.
Hello, my name is Tedwood. Fuchsia will be joining us soon.


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
A javascript code snippet

```js

function tedwood() {}

```
