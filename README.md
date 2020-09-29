# amplify-sample

## AWS Amplify

- フレームワークは無料
- [ホスティング](https://aws.amazon.com/jp/amplify/pricing/)はほぼ無料
- AWS AppSync, Amazon Cognitoなどは別料金

## インストール

```
npm install -g @aws-amplify/cli
```

## 設定

```
amplify configure
```

webでサインイン求められたり、region聞かれたり、iam要求されたり...するので設定していく

## サンプルアプリ作成

[ここ](https://aws-amplify.github.io/media/ui_library)でいろいろみれる
今回はnextアプリを作成する

```
npx create-next-app sample-app
cd sample-app/
npm run dev
```

## amplifyの初期化

```
amplify init
```

設定をいろいろ聞かれるので答えていく

- Amplify Console
- S3
- CloudFormation
- IAM

にリソースが作成される

ディレクトリは下記のような形式になる

```
├── README.md
├── amplify
│   ├── #current-cloud-backend
│   ├── backend
│   ├── cli.json
│   └── team-provider-info.json
├── node_modules
├── package.json
├── pages
├── public
├── src
├── styles
└── yarn.lock
```

## hosting

```
amplify add hosting
```

hosting方法, deploy方法を聞かれるので回答する

`/amplify/backend/`下にhosting設定が追加される

```
./amplify/backend/
├── amplify-meta.json
├── backend-config.json
├── hosting
│   └── amplifyhosting
└── tags.json
```

## 環境の追加

```
amplify init
```

上記で環境を聞かれるので `prod` など適当な環境名を追加する

## デプロイ

```
amplify publish
```

## 削除

```
amplify delete
```
