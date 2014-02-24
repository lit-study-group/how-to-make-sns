## Boostrapの基礎

`div class="container"`で囲む.

```html
<!-- app/views/layouts/application.html.erb -->
<div class="container">
  <%= yield %>
</div>
```

gridを試す.

* 横は12マス
* 縦は決まっていない

```html
<!-- app/views/posts/index.html.erb -->
<h1>投稿一覧</h1>
<div class="row">
  <div class="col-lg-4">
    ４マス
  </div>
  <div class="col-lg-2">
    2マス
  </div>
  <div class="col-lg-6">
    6マス
  </div>
</div>
```
