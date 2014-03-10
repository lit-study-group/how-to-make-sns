##  ビューの編集

```html
<!-- app/views/welcome/index.html.erb -->
<h1>ぼくらのSNS</h1>
<p>ぼくらのSNSだよ。皆、参加してね。</p>

<hr>
<h2>ユーザー登録</h2>
<div class="col-md-8">
  <%= image_tag("study3.jpg"), class: 'wide-image' %>
</div>
<div class="col-md-4">
  <%= render 'users/form', user: @new_user %>
</div>
```

```
/* app/assets/stylesheets/application.css.scss */
....
@import "bootstrap";

.wide-image {
  width: 100%;
}
```

```
$ wget http://iwarksns.herokuapp.com/assets/study3-19a2cebfc168b4f8b6a5fd786c7bc14b.jpg -o app/assets/images/study3.jpg
```
