## 投稿とユーザをつなげる

次はモデルに関係を持たせる.

実際必須ではないが, 非常に使いやすくなる.

```
# app/models/user.rb
class User < ActiveRecord::Base
...
  has_many :posts
...
end
```

```
# app/models/post.rb
class Post < ActiveRecord::Base
...
  belongs_to :user
...
end
```

単数形と複数形に気をつける.

基本的に文法の正しい英語になれば良い.
