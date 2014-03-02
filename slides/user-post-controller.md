## 投稿とユーザをつなげる

最後に, ユーザ作成時にログインユーザのものにする.

そのために, 以下の変更を行う.

```
# app/controllers/post_controller.rb
...
  def create
    # @post = Post.new(post_params)を以下の行に変える
    @post = current_user.posts.build(post_params)
  end
...
```

コンソールで確認する. `bundle exec rails console`

```
> Post.last.user
> User.first.posts
```
