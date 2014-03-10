## 投稿のHTMLの更新

記者を表示させる.

```html
<!-- app/views/posts/_post.html.erb -->
<div class="row post">
  <span class="author">
    <%= post.user.name %>
  </span>
  <p>
    <%= post.body %>
  </p>
</div>
```
