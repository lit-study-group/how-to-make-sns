##  認証機能の実装①

<br />

まずはユーザーのモデルを生成する。

<br />

```
bundle exec rails generate model user name:string email:string password_digest:string
bundle exec rake db:migrate
```

<br />
