## 投稿とユーザをつなげる

投稿に`user_id`を追加する.

```
rails g migration AddUserIdToPost user_id:integer
subl db/migrate/xxxxx_add_user_id_to_post.rb
```

インデックスを手動で追加.

```
class AddFooToPost < ActiveRecord::Migration
  def change
    add_column :posts, :user_id, :integer
    add_index :posts, :user_id
  end
end
```

適用させて, コメントを自動でつける.

```
bundle exec rake db:migrate
bundle exec annotate
```
