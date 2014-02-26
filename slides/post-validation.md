## 投稿のバリデーション

空の中身の投稿を拒否する.

```ruby
# app/models/post.rb
class Post < ActiveRecord::Base
  ...
  validates :body, presence: true
  ...
end
```

エラーを表示する.

```
<!-- app/views/posts/index.html.erb -->
<h1>投稿一覧</h1>
<% if @post.errors.any? %>
  <h2>エラー</h2>
  <ul>
    <% @post.errors.full_messages.each do |msg| %>
      <li><%= msg %></li>
    <% end %>
  </ul>
<% end %>
...
```
