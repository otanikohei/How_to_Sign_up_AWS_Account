summary: AWSアカウントを作成してみよう～ Presented by JAWS-UG 初心者支部 2022
id: docs
categories: AWS, Acount, Registration
environments: Web
status: Draft
feedback link: https://github.com/otanikohei/How_to_Sign_up_AWS_Account/settings

# AWSアカウントを作成してみよう～ Presented by JAWS-UG 初心者支部 ２０２２

## はじめに
Duration: 0:05:00

![扉絵](./images/01_title_image.gif)

本ハンズオンは以下のような方をターゲットにしています。

- AWS アカウントを契約して使いたいけど、具体的な手順が分からない
- 手順は知っているけど、操作方法が分からなくなったときに質問できないのは不安
- 課金システムが分からない、高額請求が怖い

### 前提や注意点

<aside class="negative">アカウント作成の注意点についてはできる限り配慮していますが、保証・補償をする物ではございません。 </aside>

<aside class="negative">アカウント作成した後、運用次第では費用が発生する可能性があります。</aside>

### ご用意いただきたいもの

![マストアイテム](./images/02_must_items.png)

- メールアドレス
- クレジットカード／デビットカード
- SMS (ショートメッセージサービス) が届く携帯電話やスマートホンなどの機器
- Google Authenticator

## AWS の無料利用枠について

AWS には無料利用枠があります。一部のサービスが一定額まで無料であったり、期間限定で無料で体験できます。

[https://aws.amazon.com/jp/free](https://aws.amazon.com/jp/free)

以下は、無料枠の一部ですが有効期限が 12 ヶ月のものが多いので使えるうちに色々試してしまいましょう！ 

![無料枠の例](./images/04_free_trial.png)

## AWS アカウント作成の流れ

Amazon Web Service (AWS) を利用するには、AWS アカウントの契約が必要です。

以下リンクをクリックすると、AWS アカウントを作る方法が画面のスクリーンキャプチャー付きで紹介されています。  
まずは、この手順に沿ってアカウントを作成してください。

[https://aws.amazon.com/jp/register-flow/](https://aws.amazon.com/jp/register-flow/)

## サインイン

アカウントができたらサインインしてみましょう。  
以下 URL からサインインできます。

[https://signin.aws.amazon.com/console](https://signin.aws.amazon.com/console)

![サインイン画面](./images/06_aws_management_console_sign_in.png)

上記画面がサインイン画面が表示されたら、

![サインイン画面](./images/07_signin_as_root.png)

「ルートユーザーの E メールを使用したサインイン」のリンクをクリックしてください。

![パスワード入力](./images/08_root_user.png)

上記画面に遷移しますので、[ **○ ルートユーザー** ] が選択されていることを確認し、メールアドレスを入力して、[ **次へ** ] をクリックしてください。

![パスワード入力](./images/09_root_pw.png)

先ほど設定したパスワードでサインインしてください。

![パスワード入力](./images/10_signin_toppage.png)

上記画面にサインインされたら、成功です。

他のハンズオンで「コンソール画面を開いて」と言われた場合は、この画面 またはこの画面から遷移する AWS サービスの画面を意味しています。

## マネジメントコンソールの構成

マネジメントコンソールの画面の構成について簡単に説明します。  

![AWS マネジメントコンソールの構成](./images/22_aws_management_console.png)

1. 左上の AWS のロゴをクリックすると、トップページが表示されます。  
  ![AWS マネジメントコンソールの構成](./images/23_management_console_01.png)
2. サービスをクリックすると、サービスの一覧が表示されます。  
  ![AWS マネジメントコンソールの構成](./images/24_management_console_02.gif)
3. テキストボックスにキーワードを入力すると候補が表示されます。例えば、api と入力すると、API Gateway が一番に表示され、次候補に API を記録する CloudTrail が表示されます。
  ![AWS マネジメントコンソールの構成](./images/25_management_console_03.png)
4. CloudShell のアイコンです。本ハンズオンでは取り上げませんが、AWS CLI を実行できます。
  ![AWS マネジメントコンソールの構成](./images/26_management_console_04.png)
5. パーソナルヘルスダッシュボードです。メンテナンスのお知らせや障害などが通知されます。
  ![AWS マネジメントコンソールの構成](./images/27_management_console_05.png)
6. サポートセンター へのリンクや、AWS IQ というエキスパートとコンタクトを取るためのツール、re:Post という新しいフォーラムなどにアクセスができます。
  ![AWS マネジメントコンソールの構成](./images/28_management_console_06.png)
7. リージョンを選択できます。
  ![AWS マネジメントコンソールの構成](./images/29_management_console_07.png)
8. アカウント名をクリックすると、請求情報やセキュリティ情報、アカウント情報にアクセスできます。
  ![AWS マネジメントコンソールの構成](./images/30_management_console_08.png)

## セキュリティ強化 - MFA

AWS アカウントを契約した際のメールアドレスが、**ルートアカウント** になります。  
ルートユーザーはアカウント内の全てのアクションを行うことができるので、アカウント内の神様とも言える権限があります。  

![ハッキング](./images/05_hack.png)

本ハンズオンでは、AWS アカウントの不正アクセスやアカウント乗っ取りなどの被害を防ぐため、**多要素認証（MFA）** を必須とさせていただいております。  

![ハッキング](./images/20_user_pw_mfa.png)

ユーザー名とパスワードに加えて、一時的な認証コードである MFA を合わせることでセキュリティを大幅に強化できます。
各自、App Store などで 「Google Authenticator」 で検索、ダウンロードをお願いします。

#### Google Authenticator
![Google Authenticator](./images/03_google_authenticator_icon.webp)

- Android の方：[Google Play](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=ja&gl=US)  
- iPhone の方： [App Store](https://apps.apple.com/jp/app/google-authenticator/id388497605)

<aside class="negative">ハンズオン終了後も、Google Authenticator は削除しないでください！
AWS アカウントにログインができなくなります。 </aside>

<aside class="positive">Microsoft Authenticator や Authy などでも対応可能ですが、本ハンズオンでは環境を統一するために Google Authenticator にてご案内します。</aside>

### 二段階認証の設定

まとめますと、二段階認証は以下のために設定をします。

- アカウントの神様的権限を持つルートユーザーを盗られると大変
- メールアドレス、パスワード以外にもログイン時に必要な情報を追加すべき

AWS マネジメントコンソールを操作して、二段階認証を設定していきます。

![パスワード入力](./images/11_security.png)

アカウント名をクリックして、[ **セキュリティ認証情報** ] をクリックします。

![パスワード入力](./images/12_mfa.png)

**セキュリティ認証情報** の画面に遷移するので、[ **多要素認証 (MDA)** ] にあります [ **MFA の有効化** ] ボタンをクリックしてください。

![パスワード入力](./images/13_virtual_mfa_device.png)

**MFA デバイスの管理** のダイヤログ画面が表示されるので、[ **仮想 MFA デバイス** ] が選択されていることを確認して、[ **続行** ] ボタンをクリックします。

![パスワード入力](./images/14_image_click.png)

**MFA デバイスの設定** の画面に遷移するので、[ **QA コードの表示** ] というリンクをクリックしてください。  
QR コードが表示されます。

![パスワード入力](./images/17_iphone_mfa_read.png)

Google Authenticator アプリを開き、で読み込んでください。右下の [+] アイコンをタップして、

![パスワード入力](./images/18_display_qr_code.png)

[QR コードをスキャン] をタップして、QR コードを読み込んでください。

![パスワード入力](./images/15_code_input.png)

Google Authenticator から発行されたコードを 2 つ入力して、[ **MFA の割り当て** ] ボタンをクリックしてください。

![パスワード入力](./images/16_mfa_done.png)

上記メッセージが表示されたら成功です。

## セキュリティ強化 - IAM ユーザー

### ユーザーを追加しましょう

![パスワード入力](./images/19_root_iam.png)

先ほど MFA を設定したルートユーザーはアカウントの神様的存在ですので、普段は使わないことがベストプラクティスとして推奨されています。  
普段使うユーザーは IAM というサービスから作成できます。

IAM ユーザーも盗られると権限によっては大きな被害を受けますので、MFA を設定してください。

### AWS IAM とは

![IAM](./images/94_IAM.png)

AWS Identity and Access Management (IAM) は、誰がどのサービスやリソースに、どのような条件でアクセスできるかを指定することができる権限コントロールのためのサービスです。  
誰がどのような操作を行ったか証跡を取ることにも貢献します。

IAM には、大きく分けて 4 つの機能があります。

#### **グループ**

ユーザーをとりまとめるための機能です。  
会社で例えると、部、課、チームのような概念です。

#### **ユーザー**

AWS を利用するユーザーを管理するための機能です。  
アプリケーションに操作を委ねるアクセスキーも発行できます。  
会社で例えるなら社員や社員証といったところです。

#### **ロール**

サーバーやプログラムに割り当てる権限情報です。  
会社で例えると、ID カードのようなものでしょうか。

#### **ポリシー**

上記、グループ、ユーザー、ロールに付与する具体的な権限の内訳です。  
操作を許可したり、禁止したりできます。  

#### **関係性**

![パスワード入力](./images/21_user_role_policy.png)

1. ポリシー A はユーザー A にのみ適用されます。
2. ポリシー B、C、D は、ユーザー A とユーザー B が含まれるグループに適用されます。
3. ポリシー E は、ロールにアタッチして、EC2 インスタンスにアタッチするとインスタンスにポリシー E の権限が付与できます。

#### IAM ユーザーを作成する

それでは、Administrator の権限を持つ IAM ユーザーを作成してみましょう。



## アカウントの確認とサインアウト

### AWS アカウントの確認

AWS アカウントは、数字 12 桁の数字で表現されます。  
画面上部でマイアカウントをクリックすると、確認できます。  

次作業で必要ですので、メモをしておいてください。

### サインアウト

AWS マネジメントコンソールでの操作を終えたらサインアウトをします。
画面上部をクリックして、サインアウトを選択します。

[https://aws.amazon.com/jp/cloudtrail/pricing/](https://aws.amazon.com/jp/cloudtrail/pricing/)


## オプション 1 AWS CloudTrail

![AWS CloudTrail](./images/90_AWS_CloudTrail.png)

### CloudTrail の仕組み

AWS の各種サービスは「マネージメントコンソール」、「AWS CLI」、「SDK」、「他AWSサービス」から操作ができますが、ほとんどは API エンドポイントへアクセスします。
CloudTrail はこの AWS アカウント内で実行された API アクションを記録するサービスです。
例えば EC2 インスタンスを削除した場合だと以下などが把握できます。

- **Who?**  
  誰が EC2 インスタンスを削除したか追跡できます。
- **What?**  
  何台の EC2 インスタンス削除したか追跡できます。
- **Where？**  
  どこから削除の API が発信されたか？追跡できます。
- **When？**  
  いつ削除の API が送信されたか？追跡できます。

CloudTrail は有事の際に障害切り分けに利用できたり、不正アクセスかどうか判断する材料になったりと大変有効なサービスです。

### 無料枠で取得できないアクティビティ

すべての管理イベント、データイベント、読み込み専用アクティビティを含むアカウントアクティビティの完全なレコードは CloudTrail の証跡を設定しなければ取得できません。

### CloudTrail の料金

CloudTrail はアカウントを作成した直後から有効になります。
証跡の取得自体は料金がかかりませんが、ログを S3 バケットに出力するため S3 バケットの料金がかかります。

詳細は以下サイトに記載されています。

https://aws.amazon.com/jp/cloudtrail/pricing/


## オプション 2 Budgets の設定

![AWS CloudTrail](./images/91_AWS_Budgets.png)

ルートユーザーでログインすることで利用可能です。


## オプション 3 Cost Explorer の設定

![AWS CloudTrail](./images/93_AWS_Cost_Explorer.png)

