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

## セキュリティ強化

AWS アカウントを契約した際のメールアドレスが、**ルートアカウント** になります。  
ルートユーザーはアカウント内の全てのアクションを行うことができるので、アカウント内の神様とも言える権限があります。  

![ハッキング](./images/05_hack.png)

本ハンズオンでは、AWS アカウントの不正アクセスやアカウント乗っ取りなどの被害を防ぐため、**多要素認証（MFA）** を必須とさせていただいております。  

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

- アカウントの神様的存在であるルートユーザーを盗られると大変
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

[QR コードをスキャン] をタップ。画面の QR コードを読み込んでください。

![パスワード入力](./images/15_code_input.png)

Google Authenticator から発行されたコードを 2 つ入力して、[ **MFA の割り当て** ] ボタンをクリックしてください。

![パスワード入力](./images/16_mfa_done.png)

上記メッセージが表示されたら成功です。
