## ルートを作る

* `/`にアクセスするときは, 投稿一覧
* `/posts`にPOSTを送る時は, 新しい投稿
* `/posts`にDELETEを送る時は, 投稿を削除

```ruby
# config/routes.rb
Iwarksns::Application.routes.draw do
  root 'posts#index'

  resources :posts, only: [:create, :destroy]
end
```

`resources :posts`は以下の略

```ruby
get    '/posts',          to: 'posts#index'
get    '/posts/:id',      to: 'posts#show'
get    '/posts/new',      to: 'posts#new'
post   '/posts',          to: 'posts#create'
get    '/posts/:id/edit', to: 'posts#edit'
patch  '/posts/:id',      to: 'posts#update'
delete '/posts/:id',      to: 'posts#destroy'
```

`only`でその中の２つだけ選ぶ. 逆は`except`.
