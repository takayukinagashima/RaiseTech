# 第10回課題

## 構成
* 第五回課題で作成した構成図の環境になるよう構築を進めた。
* 下の図のスタック単位でYMLファイルを作成した。

| スタック名 | テンプレートのリンク先 | リソース | 備考など |
|:----------------:|:----------------:|:----------------:|:----------------:|
|RAISETECH-VPC-2|[CF_NETWORK.yml](lecture10_yml/CF_NETWORK.yml)|VPC<br>IGW<br>PublicSubnet<br>PrivateSubnet<br>RouteTable</br>|VPCのID<br>Public2つとPrivate2つのID<br>PubricSubnet内のリソースをインターネット接続可にする|
|RAISETECH-SG-2|[CF_SG.yml](lecture10_yml/CF_SG.yml)|ALBSecurityGroup<br>EC2SecurityGroup<br>RDSSecurityGroup| 各リソース用のSecurityGroup|
|RAISETECH-EC2-2|[CF_EC2.yml](lecture10_yml/CF_EC2.yml)|EC2Instance<br>EC2InstanceProfile<br>S3BucketAccessRole|EC2インスタンスのID<br>キーペアは事前にマネジメントコンソールで作成したものを使用|
|RAISETECH-RDS-2|[CF_RDS.yml](lecture10_yml/CF_RDS.yml)|RDSInstance<br>RDSSecret<br>RDSSubnetGroup|MYSQLでDB作成|
|RAISETECH-ELB-2|[CF_ELB.yml](lecture10_yml/CF_ELB.yml)|LoadBalancer<br>HTTPListener<br>TargetGroup|EC2インスタンスとの紐付け|
|RAISETECH-S3-2|[CF_S3.yml](lecture10_yml/CF_S3.yml)|S3Bucket|フルアクセスを許可|

## 作成したスタックの一覧

![Stack_List](task-image/lecture10/Stack_List.png)

## 構築したVPCの環境確認

![VPC](task-image/lecture10/VPC.png)

## 構築したSecurityGroupの環境確認

* EC2インバウンドルール
![EC2_Inbound_Rule](task-image/lecture10/EC2_Inbound_Rule.png)

* EC2アウトバウンドルール
![EC2_Outbound_Rule](task-image/lecture10/EC2_Outbound_Rule.png)

* RDSインバウンドルール
![RDS_Inbound_Rule](task-image/lecture10/RDS_Inbound_Rule.png)

* RDSアウトバウンドルール
![RDS_Outbound_Rule](task-image/lecture10/RDS_Outbound_Rule.png)

* ALBインバウンドルール
![ALB_Inbound_Rule](task-image/lecture10/ALB_Inbound_Rule.png)

* ALBアウトバウンドルール
![ALB_Outbound_Rule](task-image/lecture10/ALB_Outbound_Rule.png)

## 構築したEC2の環境確認

* EC2の概要
![EC2_1](task-image/lecture10/EC2_1.png)

* EC2の詳細
![EC2_2](task-image/lecture10/EC2_2.png)

* IAMrole
![IAM_Role](task-image/lecture10/IAM_Role.png)

## 構築したRDSの環境確認

![RDS](task-image/lecture10/RDS.png)

## 構築したELBの環境確認

* ALB
![ALB](task-image/lecture10/ALB.png)

* ターゲットグループ
![ALB_TargetGroup](task-image/lecture10/ALB_TargetGroup.png)

* ヘルスチェック
![ALB_HelthCheck](task-image/lecture10/ALB_HelthCheck.png)

## 構築したS3の環境確認

![S3](task-image/lecture10/S3.png)

## EC2へのSSH接続確認

![SSH_connection](task-image/lecture10/SSH_connection.png)

## EC2からRDSへの接続確認

![RDS_connection](task-image/lecture10/RDS_connection.png)

## 感想
* スタックの分割をどの基準でするか悩みましたが、今回は各テンプレートでの記述内容を理解することを目的としていたため、主要なリソース毎にわけてスタックを作成しました。
* 構築の仕方は実際の現場などでケースバイケースだと思うので、今後CloudFormationで構築する際は、その時の最適解を考えて利用していきたいと思いました。
* スタック作成時にインデントなどyamlファイルの構成が間違っていることでエラーが出てそれを解消することが多く苦労しました。
* これまでの課題で構築した環境を改めてCloudFormationで自動構築することで、各サービスやリソースの紐付けに関しての理解が深まりました。
* テンプレート作成の際、様々な公式ドキュメントや技術ブログに触れましたが、多種多様な方法があり、取り入れたい記述方法や機能を探す・決めることが難しく感じました。
