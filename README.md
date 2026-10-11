# URL Mixtape

ページに載っているアルバム・曲を Spotify のプレイリストにまとめる Web アプリです。

## できること
- URL を入れるだけで、ページ内の Spotify リンク(アルバム・曲)を上から順に取得
- リンクがないページは「アーティスト - タイトル」のテキストを貼り付けて使用
- モード:全曲 / アルバムごとに人気上位N曲 / アーティストごとに人気上位N曲
- 「リストの上から何件使うか」「合計の曲数の上限」を指定可能
- 人気順は Last.fm の再生回数で判定

## 設定(管理者が1回だけ)
1. `config.js` に Spotify の Client ID と Last.fm の API key を書く(Client Secret は書かない)
2. GitHub Pages を有効化(Settings → Pages → Deploy from a branch → main / root)
3. Spotify 開発者ダッシュボードのアプリに Redirect URI `https://<ユーザー名>.github.io/url-mixtape/` を追加
4. 使う人(最大5人・Spotify Premium)を「User Management」に登録

## 注意
- Spotify の開発モードの制限で、登録した最大5人しか使えません
- URL の読み取りに外部サービス(r.jina.ai / allorigins)を使います。読めないページは「テキストから」を使ってください
