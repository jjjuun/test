# 目的
Shopify CLIを使って独自テーマを開発するための手順。  
※shopifyの無料テーマであるDawnを元に開発を進める。  
※特定のストアからDawnテーマをpull,VScode上で開発,pushまで流れを含める。  

# 作成日
2023年2月4日

# 前提環境
OS：Windows10
エディター：Visual Studio Code

# 手順
1. Node.jsをインストールする
    https://nodejs.org/en/download/ にアクセスしインストールする。
    コマンド画面でnode -vと入力して、バージョンが表示されればインストール完了。

2. Rubyをインストールする
    https://rubyinstaller.org/downloads/ にアクセスしインストールする。
    ※インストールする際は、"WITH DEVKIT"を選択する。
    コマンド画面でruby -vと入力して、バージョンが表示されればインストール完了。

3. shopify CLIをインストール
    https://shopify.dev/themes/tools/cli/installにアクセスする。
    "Install Shopify CLI"の"Windows and Linux"に記載されているインストールコマンドを入力する。
    コマンド画面でshopify -versionと入力して、バージョンが表示されればインストール完了。

4. 開発用フォルダを作成し、VScodeで開く

5. shopifyの特定ストアからDawnテーマをpullする。
    VScodeのターミナル上で、shopify theme pull --store ****.myshopify.com
    ※****にはストア名のハンドルが該当する。
    ※ストア名のハンドルがexampleなら、shopify theme pull --store example.myshopify.com

6. コマンド画面上でpull対象のテーマを選択する。
    本書ではDawnを選択する。
    ※この段階でDawnを構成するフォルダ、ファイルがcd上にインストールされる。

7. ローカル環境で閲覧する(http://127.0.0.1:9292/)
    コマンド画面上でshopify theme divを入力する。
    http://127.0.0.1:9292/ でブラウザが開けば完了

8. ローカル環境の開発をshopifyストア（example）にpushする
    コマンド画面上でshopify theme pushを入力する
    https://example.myshopify.com/ にアクセスして開発内容が反映されていれば完了。


Git,Bundler,7-Zipはインストールしなくて独自テーマ開発には支障が出ていないので、インストール必須ではない。
参考文献：https://shopify.dev/themes/tools/cli/install

