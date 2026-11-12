# 公開用リポジトリの作成

このフォルダは過去のGit履歴を含まない、新しいリポジトリです。
作成者・コミッターは `Project Maintainer <maintainer@example.invalid>` に設定しています。

## GitHubに新規作成

展開した `helidon-school-app-public` フォルダで実行します。GitHub CLIが必要です。

```bash
cd helidon-school-app-public
gh auth login
gh repo create bull2023x/helidon-school-app-public --public --source=. --remote=origin --push
```

同名のリポジトリが既に存在する場合は、別の新しい名前を指定してください。
ZIP内の `.git` も含めて展開してください。Git履歴は匿名の初回コミット1件のみです。
Web画面へのファイルのドラッグだけでは、このGit履歴・作成者設定は引き継がれません。

## デプロイ

Renderの接続先を新しいリポジトリに変更し、ビルド・起動を確認してください。
環境変数・Secretsはファイルに保存せず、サービスの設定画面で登録してください。

## 旧リポジトリについて

新しいリポジトリを作っても、旧リポジトリの内容・履歴は変わりません。
旧リポジトリが公開中なら、GitHubのSettingsで非公開に変更するか削除してください。
既存のフォークや第三者のコピーまで消えるわけではありません。

## 確認状況

ソースと新しいGit履歴を検査し、個人のローカルパスと指定された文字列が残っていないことを確認しています。
DockerfileのJava 21イメージをEclipse Temurinに変更しました。Dockerビルドと実サービスの動作確認は未実施です。
