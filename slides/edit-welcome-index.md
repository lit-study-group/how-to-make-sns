##  ビューの編集

```html
<!-- app/views/welcome/index.html.erb -->
<h1>ぼくらのSNS</h1>
<p>ぼくらのSNSだよ。皆、参加してね。</p>

<hr>
<h2>ユーザー登録</h2>
<div class="col-md-8">
  <%# image_tag("study3.jpg") %>
</div>
<div class="col-md-4">
  <%= render 'users/form', user: @new_user %>
</div>
```