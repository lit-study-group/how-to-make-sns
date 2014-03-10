## ユーザ一覧

一覧のビュー

```html
<h1>ユーザ一覧</h1>
<%= render @users %>
```

ヘッダーにリンク追加

```html
...
<ul class="nav navbar-nav navbar-right">
  <li><%= link_to t('general.home'), root_path %></li>
  <li><%= link_to 'ユーザ一覧', users_path %></li>
  <li><%= link_to t('btn.logout'), sessions_path, method: :delete %></li>
</ul>
...
```
