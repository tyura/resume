# 職務経歴書

氏名  **上野 仁弘**

---

### 自己PR
SIerでの金融系システム開発、決済系事業会社での開発・運用を経て、現在はフリーランスとして活動中です。主にバックエンド開発やクラウドインフラ構築を担当し、要件の複雑な機能や仕様が未確定な領域でも、自律的に調査・設計・実装を行ってきました。

AWS・GCPといったクラウドサービスやTerraform・CloudFormationによるIaC構築、Go・TypeScript・Pythonなどを用いたアプリケーション開発、およびCI/CDの自動化に強みがあります。また、ブロックチェーンや自動運転システムなど、業界独自の技術や知識に対しても意欲的に学習し、習得してきました。

少人数のチームで裁量を持って動くことに適性があり、仕様策定から運用までを一貫して担うプロジェクトを得意としています。未経験技術でも速習し即戦力となる適応力が評価されており、参画先からは「どんなタスクでもそつなくこなす」との声を頂いています。

---

### 技術スキル一覧

#### 言語
- Go, TypeScript, Kotlin, Python, Java, JavaScript, Solidity, Bash, PHP, SQL

#### フレームワーク・ライブラリ
- Echo, Gin, Spring Boot, React, Node.js, Express, CakePHP,

#### インフラ・クラウド
- AWS（EC2, ECS, Fargate, RDS, Lambda, SQS, SNS, S3, Route53, ALB, AWS Batch, Step Functions, CloudWatch, EventBridge, KMS, CloudFormation, CDK）
- GCP（Cloud Pub/Sub, Cloud Spanner, Cloud Logging, Cloud Scheduler, Cloud Tasks, Cloud Storage, AppEngine）
- Docker, Terraform, Kubernetes, Ansible, Nomad

#### CI/CD・監視
- GitHub Actions, CircleCI, Grafana, Prometheus, CloudWatch, Datadog, Sentry

#### データベース・分析
- DynamoDB, MongoDB, MySQL, PostgreSQL, Oracle Database, Cloud SQL, Cloud Spanner, Firestore, Dune Query (列指向DB)

#### API・通信
- REST, GraphQL, OpenAPI (Swagger), gRPC

#### その他ツール
- Twilio, wire, gqlgen, Protobuf, Firebase Auth, systemd, Selenium（Selenide）, Jest, TypeORM, senarigo

---
<div style="page-break-before:always"></div>

### 職務経歴

### フリーランス（2019年10月～現在）

**期間：2024年12月～2025年5月**

**案件名：自動運転システム開発**

#### 担当業務
自動運転システム向けのデータパイプラインやAPI、CLIツールの設計・実装。
- 以下を並列で実行するパイプラインの構築。
  - 学習用データセットのメタデータの抽出・登録。
  - 学習用データセットの画像データから動画を生成。
- S3 Object VersionIDを用いて、学習用データの整合性を保つ対応。
- APIエンドポイント追加。
- CLIツール機能追加。

#### 習得スキル
- CloudFormationによるインフラ構築
- Step Functionsを用いたデータパイプライン構築
- AWS Batchジョブの設計・構築

#### 成果
- サービス間の依存関係の整理
  APIとパイプラインは別々のリポジトリで管理されていたが、循環依存になっていた。SQSとLambda経由でパイプラインを実行させるようにすることで、サービス間の依存関係を整理した。
- デプロイ時間の短縮
  GitHub Actionsでデプロイする際に、複数リソースのデプロイをまとめたmakeコマンドを呼び出すようになっていたため、順次のデプロイとなっており、時間がかかっていた。各リソースのデプロイをGitHub Actionsで並列に実行するように変更し、デプロイ時間を半分以下に短縮した。

#### 使用技術
Go | Python | Step Functions | Lambda | S3 | SQS | AWS Batch | ECS | ALB | Aurora | CloudFormation | Github Actions | Datadog | Sentry

---

**期間：2023年10月～2024年11月**

**案件名：ブロックチェーンゲーム開発**

#### 担当業務
ブロックチェーンゲームのブロックチェーンアクセス機能の構築。
- 企画サイドや他のゲーム機能チームと要件をすり合わせ、担当タスクを明確化。
- SQS、Lambda、ECS、DynamoDB、SNSなどを用いたインフラの構築。
- CloudWatch Alarmによる監視機能の構築。
- Github ActionsによるCI/CDの構築。
- Lambda関数やブロックチェーンイベントのリスナーをNode.jsで実装。
- NFTコントラクト、NFT制御用のコントラクトの作成。

#### 習得スキル
- Solidityによるコントラクト作成
- SQSとLambdaを用いた非同期処理の構築
- DynamoDBのテーブルおよびインデックス設計

#### 成果
- ブロックチェーンはトランザクションを実行するアドレス単位では直列実行になってしまうため、パフォーマンスに難があったが、アドレスを増やして並列で実行できる仕組みを構築し、パフォーマンスを改善した。

#### 使用技術
TypeScript | Solidity | SQS | Lambda | DynamoDB | CloudWatch | EventBridge | SNS | ECS | KMS | ALB | RDS | Terraform | Github Actions

---

**期間：2023年2月～2023年9月**

**案件名：暗号資産コピートレードシステム開発**

#### 担当業務
暗号資産インデックスファンド作成機能を担当。
- 追跡対象とするアドレスとそのウェイトを選びインデックスファンドを作成する機能の実装。
- ファンドのポートフォリオ割合や収益率を取得する機能の実装。
- Dune Queryにてファンドのポートフォリオや取引量、取引手数料を分析するためのクエリの作成。

#### 習得スキル
- Polygonネットワークやトランザクション仕様についての知識
- MongoDBを用いたサービス開発
- 列指向データベース (Dune Query) を用いたデータ分析

#### 成果
- 暗号資産インデックスファンドに係る機能は、仕様が複雑で処理量が多いものであったが、適切に共通化やコンポーネント分割を行っていたため、以後に発生した仕様変更にも迅速に対応できた。
- Dune Queryでデータ分析を行う際に、Polygonトランザクションの仕様を調査して集計に必要な情報を抽出し、クエリを構築できた。また、集計データ量は膨大なものであったが、列指向データベースの性質を理解し、最大でも10秒程度で値が返るようにクエリをチューニングできた。

#### 使用技術
TypeScript | Moralis | Alchemy | MongoDB | Redis | Fargate | Dune Query

---

**期間：2022年5月～2023年1月**

**案件名：暗号資産サービス開発**

#### 担当業務
業務用暗号資産ウォレットシステムの開発。
- 暗号資産XYM用の以下機能の実装。
  アカウントの作成、マルチシグアカウントへの昇格、マルチシグでの送金、ノードとウォレットシステムとの残高同期。
- 暗号資産IOST用の以下機能の実装。
  ノードとウォレットシステムとの残高同期。

#### 習得スキル
- Cloud Spannerを用いたサービス開発およびテーブル設計
- Cloud Pub/Subを用いたサービス開発
- ブロックチェーンや暗号資産に関するドメイン知識

#### 成果
- 対応通貨を追加する際に、その通貨のドキュメントが乏しい場合でも、公式のソースコードを読みながら粘り強く仕様を調査し、実装までこぎつけた。
- GoのSDKが用意されていない通貨の追加対応をする際に、ドキュメントやTypeScriptのSDKを参照しながらその通貨のプロトコルを理解し、署名やアドレスエンコード、ハッシュの生成、トランザクションのシリアライズなどを実装した。

#### 使用技術
Go | Kubernetes | Cloud Pub/Sub | Cloud Spanner | Cloud Logging | Cloud Scheduler

---

**期間：2021年10月～2022年5月 (週3日稼働)**

**案件名：クラウド会計アプリのバックエンド開発**

#### 担当業務
  - 追加機能開発
  - リファクタリング

#### 習得スキル
- マイグレーションツールの移行
- Terraformによるインフラのコード化

#### 成果
- リファクタリングの過程でマイグレーションツールが混在した状態になっていたものをTypeormに統一。
- Terraformでコードが冗長になっていた箇所をModule化するなどして改善したり、一部Terraform化されていなかったサービスをコード化したりとインフラ周りも改善も実施。

#### 使用技術
Go | TypeScript | Echo | Node.js | Kubernetes | Terraform

---

**期間：2021年10月～2022年5月 (週2日稼働)**

**案件名：求人アプリのバックエンド開発**

#### 担当業務
- 追加機能開発
- パフォーマンスチューニング
- リファクタリング

#### 習得スキル
- Kotlinでのバックエンド開発
- senarigoを用いたE2Eテストの作成

#### 成果
- リファクタリングや機能追加をしやすくするため、E2Eテストを作成。
- 機能が複雑なため、煩雑になってしまっていたUTコードを修正して可読性の向上に寄与。

#### 使用技術
Go | Kotlin | Gin | Spring Boot | Docker | AppEngine | Cloud SQL | Cloud Logging | Cloud Tasks | Cloud Storage | Firebase Auth | Cloud Firestore | GraphQL

---

**期間：2021年7月～2021年9月**

**案件名：オンライン1on1支援サービス開発**

#### 担当業務
- ビデオ通話機能実装
- SSO実装
- その他追加機能開発

#### 習得スキル
- Expressを用いたバックエンド開発
- Twilioを用いたビデオ通話機能開発

#### 成果
- Twilio APIの利用方法を調査し、ビデオ通話機能を実装した。
- Azure ADのSSOの実現方法を調査し、実装した。

#### 使用技術
TypeScript | Node.js | Express | Nomad | Azure AD | Github Actions | Jest | Twilio

---

**期間：2020年11月～2021年6月**

**案件名：求人アプリのバックエンド開発**

#### 担当業務
- 追加機能開発
- パフォーマンスチューニング
- リファクタリング
- 不具合調査・修正

#### 習得スキル
- GinによるREST APIおよびGraphQLの実装
- スロークエリのチューニング
- GCP上でのサービス開発
- Cloud Tasksを用いた非同期処理

#### 成果
- 要件が複雑であったため、レスポンスまで7秒程度かかっていたクエリを0.3秒程度まで改善した。
- 原因特定が難しく、しばらく残っていた不具合を積極的に調査して解決した。

#### 使用技術
Go | Kotlin | Gin | Spring Boot | Docker | AppEngine | Cloud SQL | Cloud Logging | Cloud Tasks | Cloud Storage | Firebase Auth | Cloud Firestore | GraphQL

---

**期間：2020年5月～2020年10月**

**案件名：クラウドファンディングシステム開発**

#### 担当業務
- メール送信システム・入金消込システム・マイナンバー管理システムの設計および実装
- 各システムのデプロイスクリプトの作成

#### 習得スキル
- GoによるWebアプリケーション・バッチの実装
- BuffaloによるWebアプリケーション開発
- PythonによるLambda関数実装
- EC2インスタンスを用いたサーバーの構築
- RDSを用いた DBインスタンスの作成
- CodeBuildとAnsibleによる自動ビルド・デプロイ処理の作成
- KMSによる暗号鍵の管理
- systemdによるアプリケーション起動処理の構築
- Prometheusによる監視システム構築
- AWS CDKによるインフラのコード化

#### 成果
- Goによる開発だけでなく、AWSやAnsible、systemdなどを用いた環境構築も幅広く担当し、少ない人員でサービスを構築することに貢献した。

#### 使用技術
Go | Buffalo | Amazon CDK | EC2 | RDS | Lambda | SES | KMS | CodeCommit | CodeBuild | Prometheus

---

**期間：2020年1月～2020年4月**

**案件名：マッチングアプリ開発**

#### 担当業務
- Sign in with Appleの設計開発
- リワード機能の設計開発
- コードレビュー
- 開発チーム改善活動

#### 習得スキル
- Dockerを用いた開発環境の構築
- DynamoDBを用いたデータ管理
- S3での各種ファイルの管理
- PHPでの管理システムの開発

#### 成果
- Sign in with Appleの開発の際は、公式ドキュメントなどを調査してiOS、Android、Web、APIの各対応内容を取りまとめて展開した。
- 追加機能の設計開発だけでなく、Docker Composeを用いた開発環境の改善など、各種改善活動にも積極的に取り組んだ。

#### 使用技術
Java | React/Redux | jQuery | CakePHP | S3 | Nginx | Memcached | Redis

---

**期間：2019年10月～2019年12月**

**案件名：不動産会社営業支援システム開発**

#### 担当業務
- クローラの設計・実装
- 営業支援WebシステムやAPIの実装

#### 習得スキル
- PlayFrameworkを用いたAPIの実装
- Spring Bootを用いたバッチ処理の実装
- TypeScriptを用いたフロントエンドの開発
- React/Reduxを用いたフロントエンドの開発
- スクラム開発

#### 成果
  - SPAでのフロントエンド開発は未経験であったが、React/Reduxの仕組みをすぐに理解して、タイトなリリーススケジュールに適応した。
  - 膨大な物件データをクローリングする際に、並列処理を用いて夜間に処理が終わるように実装した。

#### 使用技術
Java | TypeScript | React/Redux | PlayFramework | Spring Boot | selenium

---

### GMOペイメントゲートウェイ**株式会社**（2018年2月～2019年10月）

【事業内容：決済代行および金融関連事業　従業員数：710名　資本金：133億円】

**期間：2018年2月～2019年10月**

**案件名：デビットカードイシュイングシステム開発**

#### 担当業務
- 他システムからのデータ移行（2018年3月～2018年9月）
- 追加機能開発
- 運用・保守

#### 習得スキル
- Bashによる起動シェル・監視ツール等の作成
- SQLチューニング
- SQLでのデータ集計
- Selenium（Selenide）を用いた画面テストの自動化
- スケジュール管理
- 顧客折衝
- 仕様検討
- コードレビュー
- 工数（費用）見積
- 決済システムの業務知識

#### 成果
- 開発リーダーとして、顧客との要件定義から協力会社のマネジメントや実装まで幅広いタスクを手掛けた。
- 参画以前は顧客からの要望や不具合、内部課題などのタスクが溜まっていたが、それを優先順位をつけて整理・解決し、安定して運用できる状態に持っていった。その間、他システムからのデータ移行や、VISAデビットのタッチ決済対応などのプロジェクトも遂行した。
- WEB画面のリファクタリングにあたってSeleniumを使用して全パターンの無影響確認を行い、安全かつ効率的にソースを改修した。

---
<div style="page-break-before:always"></div>

### 日鉄日立システムエンジニアリング**株式会社**（2015年4月～2018年1月）

【事業内容：システムインテグレータ  従業員数：450名  資本金：2億5千万円】

**期間：2015年4月～2018年1月**

**案件名：クレジットカード会社システム統合**

#### 担当業務
- 債権回収機能の設計・実装・テスト

#### 習得スキル
- 設計スキル
- Java8によるビジネスロジックの実装
- Junitによる単体テスト（Mockライブラリ使用）

#### 成果
- JenkinsによってCIが実施されていたためUTにこだわり、可読性および保守性の高いテストコードを作成した。
- Java8の機能をすばやく理解して積極的に使用し、チーム内の技術水準を高めるのに貢献した。
- 協力会社のメンバーや新人の指導を担当し、開発メンバーのスキルを向上させた。

---

**期間：2015年9月～2017年12月**

**案件名：メガバンクシステム統合**

#### 担当業務
- ITシナリオ作成およびテスト実施
- バグ修正

#### 習得スキル
- Javaでの実装
- テストケース作成スキル
- VBA

#### 成果
- VBAを自分で学習して、テスト結果集計やドキュメントの編集・体裁チェック等を効率化した。
