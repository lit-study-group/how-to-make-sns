##  ヘッダ本体の作成

<br />

```html
<!-- app/views/layouts/_header.html.erb -->
<nav class="navbar navbar-default" role="navigation">
  <div class="container-fluid">
    <div class="navbar-header">
      <%= link_to t('general.title'), root_path, class: 'navbar-brand' %>
    </div>

    <div class="collapse navbar-collapse">
      <% if user_signed_in? %>
        <ul class="nav navbar-nav navbar-right">
          <li><%= link_to t('general.home'), root_path %></li>
          <li><%= link_to t('btn.logout'), sessions_path, method: :delete %></li>
        </ul>
      <% else %>
        <%= render 'sessions/form', user: user %>
      <% end %>
    </div>
  </div>
</nav>
```