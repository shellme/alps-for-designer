# alps-for-designer

デザイナー向け ALPSまとめ

# ALPSとは

ALPSはApplication-Level Profile Semanticsの略で、アプリケーションで用いられる語句や情報のドキュメントです。

1. 語句の定義（オントロジー）
2. 語句の分類（タクソノミー）
3. 語句の関係性（コレオグラフィー）

以上の観点でウエブ設計のためのIA(情報設計)に用いたり 、開発に関わる人たちの共通言語にする事ができます。
XMLまたはJSONで記述します。

![image](https://user-images.githubusercontent.com/18522005/128454657-4ec0f6dc-adfc-43d1-803f-7045a4b905e6.png)

- [参考: メディアタイプとALPSプロファイル](https://qiita.com/koriym/items/2e928efb2167d559052e)

# 利用準備

## エディタ（WebStorm）をインストールする

https://www.jetbrains.com/ja-jp/webstorm/nextversion/

インストール後、WebStormのアカウントを作成してください。

## ライブラリをインストール

下記の手順でダイアグラムが表示できるようにします。

https://github.com/koriym/app-state-diagram

### Homebrewをインストール

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

https://brew.sh/index_ja

### PHPをインストール

`php -v` でバージョンを確認し、バージョンが古い場合は下記のコマンドでインストールする。

```
brew install php@xx.x
```

### composerをインストール

https://getcomposer.org/download/ の4行をコピーして、開発用のディレクトリにインストール。

インストール後、下記のコマンドでパスを通します。

```
sudo mv composer.phar /usr/local/bin/composer
```

### dotをインストール

```
brew install graphviz
```

### Node.jsをインストール

`brew install node` もしくは、 `nodenv` や `nodebrew` を使って指定バージョンをインストールします。

### app-state-diagramをインストール

```
composer global require koriym/app-state-diagram
```

# 実際に書いてみる

## ファイルを作成

`.xml` または `.json` 拡張子のファイルを作成します。 最初は `.xml` がおすすめ。

```
touch sample.xml
```

## ファイルの監視

下記のコマンドで該当ファイルをwatchモードにします。

```
composer global exec asd -- -w ./sample.xml
```

## 内容を書く

郡山さん'sチュートリアル: https://hackmd.io/@koriym/quick-alps

サンプルは下記がおすすめ

- Blog
- TODOアプリ

# デザインプロセスへの組込みアイデア

UX5段階モデルで例えると、「構造」工程の手段として取り入れることができそうだが、具体的なやり方はこれから検討。

![image](https://user-images.githubusercontent.com/18522005/128459717-ffeb2795-d436-4d1e-845b-c47742e3210c.png)

