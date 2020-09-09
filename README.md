# wordpress_theme
them for work


## how to display a menu 

1.  in setup.php add this function ```php register_nav_menu( 'enter_any_menu_id', __( 'Menu Name', 'theme_name' ) ); ```
2.  in the header or the page you need to add inside it the menu use this block of code fell free to edit values but use same id 
```php
            if( has_nav_menu( 'enter_any_menu_id' ) ){
                wp_nav_menu([
                    'theme_location'        =>  'enter_any_menu_id',
                    'container'             =>  false,
                    'fallback_cb'           =>  false,
                    // depth is nav can't contain nested list only dirct link else use 0 for all or 2,3 etc
                    'depth'                 =>  1,
                    'walker'                =>  new JU_Custom_Nav_Walker()
                ]);
            }

```

3. we can now use menu on appearnce create new menu best practice to name it same id 
4. last very important part  (Menu Settings) display location select the name (Menu Name) and save it and congrats
