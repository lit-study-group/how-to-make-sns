## ユーザ一覧

ユーザの部分テンプレートを作成.

```html
<!-- app/views/users/_user.html.erb -->
<div class="row">
  <div class="col-xs-8">
    <%= user.name %>
  </div>
  <% if user_signed_in? && current_user.id != user.id %>
  <div class="col-xs-4">
    <% if current_user.friend?(user) %>
      <%= link_to '友達から外す', friend_user_path(user), method: :delete, class: 'btn btn-danger' %>
    <% else %>
      <%= link_to '友達に追加', friend_user_path(user), method: :post, class: 'btn btn-primary' %>
    <% end %>
  </div>
  <% end %>
</div>

```
