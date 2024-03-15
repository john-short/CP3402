Learning Activities & Resources
-------------------------------
I read the WordPress developer documentation on child themes.

### Resources
 * [Child Themes – Theme Handbook](https://developer.wordpress.org/themes/advanced-topics/child-themes/)
 * [Main Stylesheet (style.css) – Theme Handbook](https://developer.wordpress.org/themes/core-concepts/main-stylesheet/)
 * [Including Assets – Theme Handbook](https://developer.wordpress.org/themes/core-concepts/including-assets/)
 * [Templates – Theme Handbook](https://developer.wordpress.org/themes/templates/)
 * [Block Patterns – Theme Handbook](https://developer.wordpress.org/themes/features/block-patterns/)

Estimated Hours
---------------
2 hours of learning.

Content Insights
----------------
The `functions.php` file in the child theme *does not* override the parent's `functions.php`. They're both loaded, with the child theme's `functions.php` being loaded first. Other files,
including [Templates](https://developer.wordpress.org/themes/templates/) and [Patterns](https://developer.wordpress.org/themes/features/block-patterns/), will be overridden if the child theme also includes said files, Templates or Patterns.

Information about the theme, such as its name, author, description, version, etc., is found in the `style.css` file and follows a [known format.](https://developer.wordpress.org/themes/core-concepts/main-stylesheet/)

Loading assets like javascript and stylesheets (including the `style.css` file) should be done using [`wp_enqueue_script()`](https://developer.wordpress.org/reference/functions/wp_enqueue_script/) and [`wp_enqueue_style()`](https://developer.wordpress.org/reference/functions/wp_enqueue_style/) respectively in the theme's `functions.php` file.

Career/Employability/Learning Insights
--------------------------------------
It's expected that you know how to make and use child themes when working with WordPress development professionally. They can be used to make modifications to a base theme without modifying the parent theme,
which makes it easy to customise the child theme on a per-customer basis without having to fork the entire theme every time.

Using child themes doesn't save development time compared to simply forking (both methods takes about equal amounts of time), but it makes the process of post-deployment support easier, specifically when
it comes to providing updates to the theme. If you fork instead of using child themes, you would have to update all deployments of all the forks one by one. With child themes, you only need update the
base theme, and all child themes will start using the new base theme without having to modify the child themes.
