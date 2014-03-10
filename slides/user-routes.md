## ユーザ一覧と友達機能

### ルートの追加

```
# config/routes.rb
...
  resources :users, only: [:index, :create] do
    member do
      post 'friend', to: :friend
      delete 'friend', to: :unfriend
    end
  end
...
```

