# GitHub Actions入門

このリポジトリでは、GitHub Actionsを初めて触る方向けに、実際に簡単なGitHub Actionsワークフローをセットアップする手順を紹介します。

## この演習を通して学べること

 - GitHub Actionsを有効化する手順
 - Java、Mavenを使ったコードベースに対して自動ビルド、自動テスト、リンターをセットアップする方法

## 事前準備

1. まず下図のように、このテンプレートリポジトリからリポジトリの作成を選択します。

![テンプレートからのリポジトリ作成](./images/prep-step1.png)

2. 作成するリポジトリの情報を入力します。
  - ここで、"Owner"はどこにリポジトリを作成するかを選択します。今回は自分のアカウント名を選択します（つまり、個人リポジトリを作ることになります）。
  - "Repository name"にはリポジトリの名前を指定します。名前は何でも構いませんが、今回は"sample-actions-repo"という名前にします。
  - "Owner"を選択すると、画面下部に"Public"、"Private"という2つの選択肢が出ます。"Public"を選択すると、誰でも見れるリポジトリとなります。"Private"を選択すると、明示的に他の人にアクセスを許可する設定をしない限り自分以外は見れないリポジトリとなります。"Public"の場合、GitHub Actionsは無償で利用可能です。"Private"の場合は[実行時間に応じた料金が発生](https://docs.github.com/ja/billing/managing-billing-for-github-actions/about-billing-for-github-actions#per-minute-rates)しますが、毎月[無料枠](https://docs.github.com/ja/billing/managing-billing-for-github-actions/about-billing-for-github-actions#included-storage-and-minutes)が付与されているので、今回の演習だけであれば無料枠の範囲内で収まります。どちらを選ぶかはお任せします。

![リポジトリ作成画面](./images/prep-step2.png)

3. 以後の作業は、作成したリポジトリのページで行います。まずは、リポジトリのページを開きます。

## GitHub Actionsの有効化

1. リポジトリのページを開いたら、画面上部のメニューから"Actions"を選択します。