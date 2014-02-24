##  ヘッダーの描画

<br />

```html
<!-- app/views/layouts/application.html.erb -->
<!DOCTYPE html>
<html>
<head>
  <title><%= t 'general.title' %></title>
  <%= stylesheet_link_tag    "application", media: "all" %>
  <%= javascript_include_tag "application" %>
  <%= csrf_meta_tags %>
</head>
<body>

<div class="container">
  <%= render 'layouts/header', user: @user %>

  <%= yield %>
</div>

</body>
</html>
```