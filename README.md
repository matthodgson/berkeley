BERKELEY THEME (A Zen 5 Sub-Theme)
----------------------

This is the Berkeley theme, developed by
IST Drupal <ist-drupal@lists.berkeley.edu> at UC Berkeley
for use with websites based on the Berkeley distribution.

*** REQUIRED DEPENDENCIES ***

The Berkeley theme requires Zen 7.x-5.x, available at http://drupal.org/project/zen.

If you want to use the drop-down menu functionality, you must download the Nice Menus
module, available at http://drupal.org/project/nice_menus. You can then enable this
functionality at appearance/settings/berkeley.

*** Important Theming Notes ***
*
* In Drupal 7, the theme system caches which template files and which theme
* functions should be called. This means that if you add a new theme,
* preprocess or process function to your template.php file or add a new template
* (.tpl.php) file to your sub-theme, you will need to rebuild the "theme
* registry." See http://drupal.org/node/173880#theme-registry
*
* Drupal 7 also stores a cache of the data in .info files. If you modify any
* lines in your sub-theme's .info file, you MUST refresh Drupal 7's cache by
* simply visiting the Appearance page at admin/appearance (or using Drush).
*

NOTES:

1. This Zen5-based theme uses Sass/Compass. If you want to edit the included Sass files
and recompile the existing css files, get the latest version of Sass (3.2 or later).
You do not need Sass to use this theme if you will not be changing the Sass files.

  For more information on using Sass/Compass, read sass/README.txt

2. Theme configuration settings can be set at admin/appearance/settings/berkeley.

3. Site information can be set at admin/config/system/site-information.

4. Sass files (.scss) are used to generate the associated css files.

  To edit the original .scss files:
  - Delete all CSS files by running: compass clean
  - Edit the config.rb file and change #environment = :development
  - Regenerate all the CSS files by running: compass watch (or compass compile)

5. Moving to Production
  Remember to change #environment = :production and turn on Drupal's CSS aggregation
  before moving to Production (see sass/README.txt).

6. Adding custom styles
  If you want to add custom CSS styles but do not need to override any PHP files,
  do the following:

  a. If using Sass/Compass:
     1. In the berkeley.info file, uncomment stylesheets[all][] = css/styles.css
        (remove the semi-colon)
     2. Create a new styles.scss file in the sass directory (sass/styles.scss)
     3. Add the following to the top of the file: @import "base";
     4. Add your custom styles to the sass/styles.scss file
     5. When you run compass watch (or compass compile), it will generate styles.css
     6. See the README.txt file in the SASS folder to learn more about using Sass and Compass

  b. If you don't want to use Sass/Compass:
     1. In the berkeley.info file, uncomment stylesheets[all][] = css/local.css
        (remove the semi-colon)
     2. Create a new local.css file in the css directory (css/local.css)
     3. Add your custom styles to the css/local.css
     4. Note: Do not create a sass/local.scss file, or it will remove any styles
        in the local.css when you run compass watch or compass compile


