# CodeBtos

# CodeDeploy

## region
Tokyo ○

## 内容

その名の通り、コードをデプロイ自動化サービス
アプリケーションとデプロイグループの設定が必要。
※ CodeDeployの対象となるインスタンスにはCodeDeployAgentをインストール必要がある。このAgentがpolingしてるらしい。

### appspec
デプロイ内容を定義するもの
http://qiita.com/yukofeb/items/e077fc8755416c904032#appspec%E4%BD%9C%E6%88%90


http://dev.classmethod.jp/cloud/aws/cm-advent-calendar-2015-aws-re-entering-codedeploy/

# CodePipeline

## region
Tokyo ☓

## 内容

+ source
+ build
+ deploy

をやってくれるもの、視覚的にもわかりやすい。

### Source

S3 or Github
※S3はVersioning設定を有効にしておく必要がある
※pipeline自体が監視してくれる

### build

SolanoCI or jenkins
jenkinsに関しては自前で立てる必要あり。

### deploy

beanstalk or codedeploy

### わかりやすい
http://recipe.kc-cloud.jp/archives/tag/aws-codepipline

# CodeCommit

## region
Tokyo ☓

## 内容
要はGit。
IAMロールでの権限管理が可能。
現状できるのはTriggerで SNS or lamda 呼び出し
デフォルトではなにも繋がってない。
