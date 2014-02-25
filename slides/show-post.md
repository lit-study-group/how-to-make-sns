## 投稿を表示する

コントローラで投稿を取ってくる

```ruby
＃app/controllers/posts_controller.rb
...
  def index
    @post = Post.new
    @posts = Post.all
  end
...
```

投稿の部分テンプレートを作る.

```
<!-- app/views/posts/_post.html.erb -->
<div class="row post">
  <%= post.body %>
</div>
```

投稿を表示する.

```
<!-- app/views/posts/index.html.erb -->
....
<div class="posts">
  <%= render @posts %>
</div>
```
