## 第3回課題

### 1.サンプルアプリケーションの起動

   ![sample](lecture03image/sample.png)
   
   ブラウザで起動し、メロンの画像を登録した状態

### 2.APサーバーについて

1. APサーバーの名前とversionの確認

　　'puma ver6.4.2'

  ![puma](lecture03image/puma.png)

2. APサーバーを終了させた場合のアクセスの確認

  ![puma-stop](lecture03image/puma-stop.png)

   APサーバーを終了させた場合、アクセスできなくなる

3. 再度アプリケーションを起動出来るかを確認

  ![puma-reboot](lecture03image/puma-reboot.png)

### 3.DBサーバーについて

1. DBサーバーの名前とCloud9 で動作しているversionの確認

  'mysqlver 8.4.0'
   
  ![mysql-version](lecture03image/mysql-version.png)

2. DB サーバーを終了させた場合のアクセス確認

  ![mysql-stop](lecture03image/mysql-stop.png)
   DBサーバーを終了させた場合、アクセスできなくなる

3. Railsの構成管理ツールの名前

   'Bundler'

### 4. 今回の課題の学習と感想

- 本課題のようなシンプルなアプリケーションを動かすのに、こんなに多くのシステムが組み込まれているのは驚きだった。
- デプロイまでの過程で、録画講義では出なかったエラーやファイルの修正を行なったが、一つ一つの単語の意味を調べたりで思うより時間が掛かってしまった。
- 今回は自力でデプロイまで進められたが、エラーの修正などで対応する際、自分で調べすぎていたりで時間をかけすぎてしまったので、discordで質問するなどサポートツールを活用していきたいと思った。