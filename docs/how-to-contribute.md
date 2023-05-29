# ブラウザ上で編集作業を共同で行うための手順

## 1. 準備

1. GitHubアカウントをつくる
    - 参考：[GitHubにサインアップ(Sign up) - 新規ユーザ登録 - Qiita](https://qiita.com/mfunaki/items/e01762475967d4e05a1f)
1. 作成したアカウントでGitHubにログインする


## 2. 自分のアカウントにリポジトリをフォーク(fork)する

mayosuke/cult-of-slyflourishリポジトリのトップ画面右上にある「Fork」書かれたボタンをクリックします。
![](images/click_fork.png)


次の画面では、特に何も設定をいじらずに「Create Fork」をクリックします。
![](images/create_fork.png)


一見、元のリポジトリの画面と違いがわかりづらいですが、画面左上のアカウント名が自分のものになっていることで、元のリポジトリが自分のアカウントにフォークされたことがわかります。
![](images/forked_repository.png)

ここまでで、編集作業を開始できるようになりました。


## 3. ブラウザ上で編集を行う

[mayosuke/cult-of-slyflourish](https://github.com/mayosuke/cult-of-slyflourish)に戻り、[The Lazy GM's Resource Document-jp.md](../The%20Lazy%20GM's%20Resource%20Document-jp.md)をクリックします。
![](images/open_document.png)


下の画像の赤枠で囲まれている鉛筆型アイコンをクリックします。
![](images/start_edit.png)

鉛筆アイコンをクリックすると、編集モードに切り替わりドキュメントの編集が開始できます。

**注意：自分のアカウントにフォークしたリポジトリでも編集を行えますが、その場合元のリポジトリ(mayosuke/cult-of-slyflourish)に編集内容を統合（マージ）する作業が若干面倒になるため、自力でなんとかできる方以外は必ず元のリポジトリから編集を行うようにしてください。**
![](images/edit_mode.png)

編集の例として、オリジナルのドキュメントの最後のセクション「Lazy Solo 5e」の「Treasures」を日本語化した時の作業の流れを記載します。

「Treasures」はドキュメントの一番最後にあるので、画面を一番下までスクロールさせます。
![](images/translation_example1.png)

日本語化してみました。
![](images/translation_example2.png)

編集内容が期待どおりに表示されるか、プレビューモードで確認できます。エディットエリアの上部左側にある「Preview」ボタンをクリックします。
![](images/preview_button.png)

問題なく表示できているようです。

![](images/check_preview.png)

## 編集結果を提出する

編集内容が問題なさそうであれば、元のドキュメントに編集結果を提出しましょう。エディットエリアの上部右側にある「Commit Changes」ボタンをクリックします。
![](images/commit_change.png)

編集内容を記入するポップアップが表示されます。簡潔に編集内容を記入して、「Propose Changes」をクリックします。編集内容について補足などがあれば、「Extended Descriptions」に記入します。
![](images/propose_changes.png)

「Create pull request」をクリックすることで、編集結果の提出処理が開始されます。
![](images/create_pr.png)

「Create pull request」をクリックする画面を下にスクロールすると、編集差分を確認できます。プレビューで事前に確認してあれば、特にここを気にしなくても大丈夫です。
![](images/compare_changes.png)

「Create pull request」をクリックした先の画面で、もう一度「Creaate pull request」というボタンをクリックすると、編集結果が提出されます。
![](images/submit_changes.png)

編集結果が提出されました。
![](images/changes_submitted.png)

提出内容が問題無ければ、リポジトリ管理者(現在はmayosuke)によって編集内容がドキュメントにマージされます。


## 一度提出したプルリクエストを更新する

一度提出したプルリクエストに対して、他のメンバーから指摘を受けたり、自分で直したい箇所を見つけてしまった場合、提出した編集内容を更新することができます。

まず、更新したいプルリクエストを開きます。
![](images/open_pr.png)

開いたプルリクエストには、提出した編集内容の入れ物（ブランチ）が必ず紐づいています。このブランチを開きます。画像中の点線で囲われた部分をクリックします。
![](images/open_branch.png)

一見、オリジナルのリポジトリとの違いがわかりづらいですが、オリジナルをフォークしたリポジトリ上の、プルリクを提出した時に作成されたブランチが選択された状態になっています。この画面で編集対象の文書を開きます。
![](images/open_document_to_be_updated.png)

文書が開いたら、新規の編集を行うときと同じように鉛筆アイコンをクリックして編集を開始します。
![](images/start_edit_on_branch.png)

編集し終わったら、「Commit changes」を行うのも新規の編集時と同じです。「Commit Change」行うことで、提出済みのプルリクエストが更新されます。
![](images/submit_change.png)

更新し終わったので、オリジナルのリポジトリに戻ってプルリクエストに反映されたかどうかを確認します。画像中の赤線で囲われた箇所をクリックします。
![](images/open_original_repo.png)

オリジナルのリポジトリに戻ってきました。ここで「Pull requests」をクリックします。
![](images/check_updated_pr.png)

更新したプルリクエストを選択します。
![](images/open_pr.png)

先程行った「Commit Changes」の内容が、プルリクエストに追加されていることが確認できます。「Files changed」をクリックすると、更新内容が反映された状態の最新の提出内容が確認できます。
![](images/submitted_changed_appeared.png)

「Files changed」を開いてみたところです。
![](images/latest_submitted_change.png)

以上で、一度提出したプルリクエストの更新は完了です。


### マージ結果確認

提出内容がマージされたら、自分のアカウントのメールアドレス宛にマージされた事がメールされます。

[The Lazy GM's Resource Document-jp.md](The%20Lazy%20GM's%20Resource%20Document-jp.md)を開いて編集内容が反映されたことを確認して、一連の編集作業は完了です。

編集の履歴をここから辿ることもできます。
![](images/check_history.png)

![](images/merged_history.png)


## 参考

マークダウンの編集Tipsについては、以下などを参考にしてみてください。

- [Qiita Markdown 早見メモ - Qiita](https://qiita.com/iiokazuya/items/21ae40c1ee8ec9acd484)



## お断り

Git/GitHubの機能・仕組みなどについて、正確でない表現になっている可能性があります。Git/GitHubにあまり詳しくない方でも、なるべく戸惑わずに編集作業に参加できることを目的としているためですので、ご了承ください。
