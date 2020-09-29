# amplify-sample

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
npx create-next-app next-amplified
cd next-amplified/
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
