## 関連モデル

* 投稿は1対た
  * ユーザは複数の投稿を持つ
  * 投稿一人にしか属しない
* 友達は他対他
  * ユーザは複数の友達を持つ
  * その友達は複数のユーザと友達

<br class="clear">

<div class="seventh left">
  <div class="half left">
      <table class="move-right">
        <caption>users</caption>
        <thead><tr><td>id</td><td>name</td></tr></thead>
        <tbody>
          <tr><td>1<td>Daniel
          <tr><td>2<td>Iwark
          <tr><td>3<td>Moe
        </tbody>
      </table>
  </div>
  <div class="half left">
      <table>
        <caption>posts</captin>
        <thead><tr><td>id</td><td>user_id</td><td>content</td></tr></thead>
        <tbody>
          <tr><td>1<td>3<td>Foo
          <tr><td>2<td>1<td>Bar
          <tr><td>3<td>2<td>Baz
        </tbody>
      </table>
  </div>
</div>

<div class="third right">
  <table>
    <caption>friendships</captin>
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

２重は避けられるけど, Railsでは使いづらい.
