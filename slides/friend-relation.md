## 友達機能データベース更新

必要なデータベースのテーブルを作成.

```
$ bundle exec rails g migration CreateFriendships
```

繋げるためのテーブルに`id`の必要性ない.


```
# db/migrate/xxxx_create_friendships.rb
class CreateFriendships < ActiveRecord::Migration
  def change
    create_table :friendships, id: false do |t|
      t.belongs_to :user
      t.belongs_to :friend
    end
    add_index :friendships, :user_id
    add_index :friendships, [:user_id, :friend_id]
  end
end
```

変更を適用させる


```
$ bundle exec rake db:migrate
```

