##  投稿のモデル

[モデル][model]と[マイグレーション][migration]の自動生成

```
bundle exec rails generate model Post body:text
```

```ruby
# db/migrate/xxxxx_create_posts.rb
class CreatePosts < ActiveRecord::Migration
  def change
    create_table :posts do |t|
      t.text :body

      t.timestamps
    end
  end
end
```

* `CreatePosts`は`generate model Post`で作成
* `t.text :body`は`body:text`と指定して作成
* `t.timestamps`は自動作成. 作成・更新日用

```ruby
# app/models/post.rb
class Post < ActiveRecord::Base
end
```

[migration]: http://lit.tuvistavie.com/rails-intro/#/11
[model]: http://lit.tuvistavie.com/rails-intro/#/10
