# 第5回課題 

## EC2にサンプルアプリケーションのデプロイ

 1. pumaでの動作確認

- systemdで起動
![puma_operation](task-image/lecture05/puma_operation.png)

 2. Unixsocketを利用したpumaでの動作確認

![puma_unixsocket_operation](task-image/lecture05/puma_unixsocket_operation.png)

 3. Nginx単体での動作確認

![nginx_operation](task-image/lecture05/nginx_operation.png)

 4. pumaとNginxをUnixsocketを利用した環境での動作確認

![puma_niginx_unixsocket_operation](task-image/lecture05/puma_niginx_unixsocket_operation.png)

## ELB経由でEC2への接続確認

 1. ALBの作成

![create_alb](task-image/lecture05/create_alb.png)

 2. ターゲットグループのヘルスステータスを確認

![ec2_health_check](task-image/lecture05/ec2_health_check.png)

 3. ALBのDNS名での動作確認

![alb_operation](task-image/lecture05/alb_operation.png)

## S3を画像データ保存先に利用しての動作確認

1. S3の作成

![create](task-image/lecture05/create_s3.png)

2. EC2にアタッチするIAMロールの作成

- AmazonS3FullAcces権限を付与
![create_iamrole](task-image/lecture05/create_iamrole.png)

3. IAMロールをEC2にアタッチ

![iamrole_attach_ec2](task-image/lecture05/iamrole_attach_ec2.png)

4. S3に画像が保存されているかの動作確認

- ブラウザでの確認
![s3_operation1](task-image/lecture05/s3_operation1.png)

- AWSコンソール画面での確認
![s3_operation2](task-image/lecture05/s3_operation2.png)

## 構築した環境の構成図の作成

![lecture05_diagram_ver3](task-image/lecture05/lecture05_diagram_ver3.png)

## 構築した環境の構成図の作成(修正版)

![lecture05_diagram_ver4](task-image/lecture05/lecture05_diagram_ver4.png)


## 今回の学習の感想
- 今回の環境構築にあたり、色々なファイルの設定内容の意味やどう関連しているのかの理解がとても難しかったです。
- エラーや問題にあたるたびに色々なブログ記事や公式ドキュメントを参考にしましたが、そもそもの知識量が乏しく記述内容を読み解く力がもっと必要だと感じました。
- 今回の課題で詰まった部分は、RDSへの接続、ブラウザで保存した画像が表示されない、画像が保存できないなど色々ありましたが、沢山のエラーや問題に対応したおかげで多少なりとも自信がついたように思います。