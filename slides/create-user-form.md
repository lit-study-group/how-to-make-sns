##  ユーザー登録フォーム作成

<br />

```html
<!-- app/views/users/_form.html.erb -->
<%= form_for user, html:{role:'form'} do |f| %>
  <% if user.errors.any? %>
    <div class="error_messages">
      <h2>エラー</h2>
      <ul>
        <% for message in user.errors.full_messages %>
          <li><%= message %></li>
        <% end %>
      </ul>
    </div>
  <% end %>
  <div class="form-group">
    <%= f.label :name, '名前' %>
    <%= f.text_field :name, class: "form-control" %>
  </div>
  <div class="form-group">
    <%= f.label :email, 'メール' %>
    <%= f.text_field :email, class: "form-control" %>
  </div>
  <div class="form-group">
    <%= f.label :password, 'パスワード' %>
    <%= f.password_field :password, class: "form-control" %>
  </div>
  <div class="form-group">
    <%= f.label :password_confirmation, 'パスワード確認' %>
    <%= f.password_field :password_confirmation, class: "form-control" %>
  </div>
  <div><%= f.submit t('btn.register'), class: "btn btn-primary" %></div>
<% end %>
```
