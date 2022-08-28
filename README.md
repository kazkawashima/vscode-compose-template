# vscode-compose-template-node
VS Code Remote Containersのフロントエンド開発環境用テンプレート

## ベース使い方の話
https://zenn.dev/leftletter/articles/0969dcef061ff8

modified.
server service除外 from docker-compose.yml
base node:16
add node-gyp, gcloud SDK, firebase-tools, jre

## use
1. gcloud login
2. firebase login
3. cd ./ui
4. 既存プロジェクトgit clone～ or nuxt/reactして
