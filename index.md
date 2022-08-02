summary: AWSアカウントを作成してみよう～ Presented by JAWS-UG 初心者支部 2022
id: docs
categories: AWS, Acount, Registration
environments: Web
status: Draft
feedback link: https://github.com/otanikohei/How_to_Sign_up_AWS_Account/settings

# AWSアカウントを作成してみよう～ Presented by JAWS-UG 初心者支部 ２０２２

## はじめに
Duration: 0:05:00

![扉絵](./images/01_title_image.png)

本ハンズオンは以下のような方をターゲットにしています。

- AWS アカウントを契約して使いたいけど、具体的な手順が分からない
- 手順は知っているけど、操作方法が分からなくなったときに聴ける環境がないと不安
- 課金システムが分からない
- 高額請求が怖い

### 前提や注意点

<aside class="negative">アカウント作成の注意点についてはできる限り配慮していますが、保証・補償をする物ではございません。 </aside>

<aside class="negative">アカウント作成した後、運用次第では費用が発生する可能性があります。</aside>

### ご用意いただきたいもの

![マストアイテム](./images/02_must_items.png)

- メールアドレス
- クレジットカード／デビットカード
- SMS (ショートメッセージサービス) が届く携帯電話やスマートホンなどの機器
- Google Authenticator

#### Google Authenticator について

![Google Authenticator](./images/03_google_authenticator_icon.webp)

本ハンズオンでは、AWS アカウントの不正アクセスやアカウント乗っ取りなどの被害を防ぐため、**多要素認証（MFA）** を必須とさせていただいております。  

![ハッキング](./images/05_hack.png)

AWS アカウントを契約すると、登録したメールアドレスが **ルートユーザー** になります。  
ルートユーザーはアカウント内の全てのアクションを行うことができるので、

各自、App Store などで 「Google Authenticator」 で検索、ダウンロードをお願いします。

- Android の方：[Google Play](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=ja&gl=US)  
- iPhone の方： [App Store](https://apps.apple.com/jp/app/google-authenticator/id388497605)

<aside class="negative">ハンズオン終了後も、Google Authenticator は削除しないでください！
AWS アカウントにログインができなくなります。 </aside>

## AWS の無料利用枠について

AWS には無料利用枠があります。一部のサービスが一定額まで無料であったり、期間限定で無料で体験できます。

[https://aws.amazon.com/jp/free](https://aws.amazon.com/jp/free)

以下は、無料枠の一部ですが有効期限が 12 ヶ月のものが多いので使えるうちに色々試してしまいましょう！ 

![無料枠の例](./images/04_free_trial.png)

## AWS アカウント作成の流れ

Amazon Web Service (AWS) を利用するには、AWS アカウントの契約が必要です。

以下リンクをクリックすると、AWS アカウントを作る方法が画面のスクリーンキャプチャー付きで紹介されています。  
本手順では、この手順にプラスして、MFA の設定など AWS を扱う上で欠かせないセキュリティ設定なども解説します。

[https://aws.amazon.com/jp/register-flow/](https://aws.amazon.com/jp/register-flow/)

<aside class="positive">このハンズオンは EC2 インスタンスのログイン操作が目的ではいため、必要最低限の設定にてインスタンスを起動しています。</aside>