## 投稿機能

コントローラで空の投稿から始める.

```
# app/controllers/posts_controller.rb
...
  def index
    @post = Post.new
  end
...
```

投稿のためのフォームを作る.

```
<!-- app/views/index.html.erb -->
....
<%= form_for @post, html: { class: 'form post-form' } do |f| %>
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

`create`は書いてないので, 投稿を押すとエラーが出る.
