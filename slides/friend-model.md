##  友達機能のモデル

* `has_and_belongs_to_many`は多対多を表す.
    * `join_table`で予め作ったテーブルを指定
    * `association_foreign_key`で中身を指定


```
# app/models/user.rb
class User < ActiveRecord::Base
 has_and_belongs_to_many :friends, join_table: 'friendships',
                                    class_name: 'User',
                                    association_foreign_key: 'friend_id'
...
  def become_friend(friend)
    User.transaction do
      self.friends << friend
      friend.friends << self
    end
  end

  def remove_friend(friend)
    User.transaction do
      self.friends.delete(friend)
      friend.friends.delete(self)
    end
  end
...
end
```
