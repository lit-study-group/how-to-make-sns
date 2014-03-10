##  日本語化

<br />

```yml
# config/locales/ja.yml
ja:
  btn:
    delete: 削除
    post: 投稿
    register: ユーザー登録
    login: ログイン
    logout: ログアウト
  general:
    title: Iwark SNS
    delete_confirmation: 本当に削除しますか?
    home: ホーム
  time:
    before: '%{time}前'
  posts:
    feed: タイムライン
    placeholder: 書き込んでみよう
    list: 投稿一覧
  errors:
    login: メールアドレスもしくはアドレスが正しくありません
```

言語を設定する

```
# config/application.rb
...
config.i18n.default_locale = :ja
...
```
