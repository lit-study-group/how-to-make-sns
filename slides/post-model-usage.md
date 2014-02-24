##  投稿のモデルを使う

マイグレーションをデータベースに反映

```
bundle exec rake db:migrate
```

コメントを自動的につけて, `app/models/post.rb`を確認.

```
bundle exec annotate
```

コンソールで使ってみる

```
bundle exec rails console
> Post
> Post.count
> Post.create(body: "新しいポスト")
> Post.count
> Post.first
> Post.last
> Post.create(body: "２つ目のポスト")
> Post.count
> Post.first
> Post.last
> Post.all
```
