## 投稿機能（作成ロジック）

`PostsController`の`create`メソッドを実装する.

そのために, まず受け取りたいパラメータの設定.

```ruby
# app/controllers/posts_controller.rb
class PostsController < ApplicationController
  ....

  private
  def post_params
    params.require(:post).permit(:body)
  end
end
```

`post_params`を使って`create`メソッド実装.

```ruby
# app/controllers/posts_controller.rb
class PostsController < ApplicationController
  ...
  def create
    @post = Post.new(post_params)
    if @post.save
      redirect_to root_path, notice: 'Post created'
    else
      render :index
    end
  end
  ...
```
