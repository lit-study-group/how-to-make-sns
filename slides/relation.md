## 関連モデル

友達関係を表す

<div class="half left">
  <table class="move-right">
    <caption>users</captin>
    <thead><tr><td>id</td><td>name</td></tr></thead>
    <tbody>
      <tr><td>1<td>Daniel
      <tr><td>2<td>Iwark
      <tr><td>3<td>Moe
    </tbody>
  </table>
</div>

<div class="half right">
  <table>
    <caption>frienships</captin>
    <thead><tr><td>user_id</td><td>other_id</td></tr></thead>
    <tbody>
      <tr><td>1<td>2
      <tr><td>2<td>1
      <tr><td>1<td>3
      <tr><td>3<td>1
    </tbody>
  </table>
</div>

<br class="clear">

２重は避けられるけど, Railsで使いづらい.
