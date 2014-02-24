## 部分テンプレート

* HTMLを長く・複雑にしたくない
* HTMLを再利用できるようにしたい

<br>

フォームを部分テンプレートに入れる.

部分テンプレートのファイル名は`_`から始まる.

```html
<!-- app/views/posts/_form.html.erb -->
<%= form_for post, html: { class: 'form post-form' } do |f| %>
  <div class="form-group row">
    <div class="col-lg-11">
      <%= f.text_area :body, class: 'form-control' %>
    </div>
    <div class="col-lg-1">
      <%= f.submit '投稿', class: 'btn btn-primary' %>
    </div>
  </div>
<% end %>
```

別のテンプレートで部分テンプレートを使う.

```html
<!-- app/views/posts/index.html.erb -->
<h1>投稿一覧</h1>
<%= render 'posts/form', post: @post %>
```
