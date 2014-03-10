## ユーザ一覧と友達機能

### アクションを追加

```
# app/controllers/users_controller.rb
class UsersController < ApplicationController
  skip_before_action :authenticate_user!, only:[:create]
  before_action :set_user, except: [:index, :create]

  def index
    @users = User.all
  end

  def friend
    current_user.add_friend(@user) unless current_user.friend?(@user)
    redirect_to :back
  end

  def unfriend
    current_user.remove_friend(@user) if current_user.friend?(@user)
    redirect_to :back
  end


  private
    def user_params
      params.require(:user).permit(:name, :email, :password, :password_confirmation)
    end

    def set_user
      @user = User.find(params[:id])
    end
end
```
