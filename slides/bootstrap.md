## Bootstrapの導入

Gemfileで次の行があるかを確認.

```
gem 'bootstrap-sass', '~> 3.1.1'
```

スタイルシートをSCSSに変える.

```
mv app/assets/stylesheets/application.css app/assets/stylesheets/application.css.scss
```

Bootstrapをインポートする.

```
/* app/assets/stylesheets/application.css.scss */
....
 *= require_self
 *= require_tree .
 */

@import "bootstrap";
```

JSでもBootstrapを導入

```
// app/assets/javascripts/application.js
...
//= require jquery
//= require jquery_ujs
//= require bootstrap 
//= require_tree .
```
