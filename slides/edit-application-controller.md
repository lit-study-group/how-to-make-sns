##  様々なメソッドの実装

<br />

```ruby
# app/controllers/application_controller.rb
class ApplicationController < ActionController::Base
  protect_from_forgery with: :exception

  before_action :authenticate_user!
  before_action :set_new_user

  helper_method :current_user
  helper_method :user_signed_in?

  private

  def user_signed_in?
    !current_user.nil?
  end

  def current_user
    @current_user ||= User.find(session[:user_id]) if session[:user_id]
  end

  def authenticate_user!
    redirect_to anonymous_root_path unless user_signed_in?
  end

  def login(user)
    session[:user_id] = user.id
  end

  def set_new_user
    @user = User.new unless user_signed_in?
  end

end

```