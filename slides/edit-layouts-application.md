##  ヘッダーの描画

<br />

<pre><code>
<!-- app/views/layouts/application.html.erb -->
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;&lt;%= t 'general.title' %&gt;&lt;/title&gt;
  &lt;%= stylesheet_link_tag    "application", media: "all" %&gt;
  &lt;%= javascript_include_tag "application" %&gt;
  &lt;%= csrf_meta_tags %&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class="container"&gt;
  &lt;div class="container"&gt;
    &lt;%= render 'layouts/header', user: @user %&gt;
    &lt;%= yield %&gt;
  &lt;/div&gt;
&lt;/div&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre></code>
