# portfolio-template
ポートフォリオサイト

## 開発方法
### セットアップ
```bash
$ git clone git@github.com:FromAtom/portfolio-template.git
$ cd portfolio-template
$ bundle install --path vendor/bundle
```

### 開発サイクル
これを叩くとサーバが立ち上がる。

```bash
$ bundle exec middleman server
$ open 'http://localhost:4567'
```

サイト内のファイルを編集するたびにブラウザが自動リロードされるので便利です。

### 新しいページの増やし方
`source/works` ディレクトリの中に `hoge.html.slim` という名前でファイルを作れば、新しいページになる。このページへのリンクは

```ruby
= link_to "リンク名", "/works/hoge"
```

と書けば良い。

## BASIC認証
下記2つの環境変数を設定することで、BASIC認証を有効化できます。

```ruby
ENV["PORTRAIT_USER"] #ユーザ名
ENV["PORTRAIT_PASSWORD"] #パスワード
```

## License
[MIT](LICENSE)