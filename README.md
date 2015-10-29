# GitBootCampPremium

## git checkout

git checkoutは以下の3つの機能を有します。
* ファイルのチェックアウト
* コミットのチェックアウト
* ブランチのチェックアウト

```git checkout master```

master ブランチに戻るコマンドです。

```git checkout <commit> <file>```

ファイルの過去のリビジョンをチェックアウトするコマンドです。
このコマンドを実行すると、作業ディレクトリに存在する指定した <file> が、
指定した <commit> に含まれそのファイルの完全なコピーとなり、
さらにそれをステージングエリアに追加します。

```git checkout <commit>```

作業ディレクトリ内のすべてのファイルを指定したコミットと同一の状態に更新するコマンドです。
引数 <commit> にはコミットハッシュまたはタグを使用することができます。
このコマンドを実行すると、” detached HEAD” 状態になります。

[www.atlassian.com](https://www.atlassian.com/ja/git/tutorial/undoing-changes#!checkout)

## git merge

ブランチに行った変更を取り込むコマンドです

```git merge <マージ対象ブランチ>```


*参考サイト
[Qiita](http://qiita.com/LOUIS_rui/items/8e66f6f8f1a536830081)

## git rebase i

コミット内容を修正するコマンドです
- コミットメッセージの変更
- コミット内容の変更
- コミットの分割
- コミットの統合
- コミットの削除

```git reabase -i <コミット番号>```

*参考サイト
[あのコミットをなかった事に。git rebase -i の使い方](http://www.karakaram.com/git-rebase-i-usage)

# 12 git reset
HEADの位置を変更するコマンド。
オプションによってインデックス、ワーキングツリーの内容も変更できる。
* --soft HEADの位置のみを変更する。インデックス、ワーキングツリーには影響なし
* --mixed HEADの位置とインデックスを変更する。ワーキングツリーには影響なし
* --hard HEADの位置、インデックス、ワーキングツリーをすべて変更する。
[参考URL](http://d.hatena.ne.jp/murank/20110327/1301224770)

# 15 git fetch
リモートリポジトリの最新の履歴の取得だけを行うことができる。
取得したコミットは、名前の無いブランチとして取り込まれます。
このブランチはFETCH_HEADという名前でチェックアウトすることができる。
[参考URL](http://www.backlog.jp/git-guide/stepup/stepup3_2.html)

## git branch

ブランチとは独立な開発ラインを意味します。
ブランチは編集/ステージ/コミットプロセスに対する抽象概念です。
これは、作業ディレクトリやステージングエリア、プロジェクト履歴を
全く新しく作成する手段であると考えることもできます。
新規のコミットは、現在のブランチの履歴に記録され、プロジェクト履歴における分岐を形成します。

git branch は、ブランチの作成、一覧表示、リネーム、削除を行うコマンドです。
このコマンドにはブランチの切り替えを行う機能も、
分岐した履歴を統合して元に戻す機能もありません。
このため、git branch コマンドは多くの場合 git checkout コマンド
および git merge コマンドと併用されます。

```git branch```

リポジトリ内のすべてのブランチを一覧表示します。

```git branch <branch>```

<branch> という名称の新規ブランチを作成します。
新たに作成されたブラントのチェックアウトは行われません。

```git branch -d <branch>```

指定したブランチを削除します。
ブランチにマージされていない変更が残っている場合は Git が削除を拒否するため、
このコマンドは「安全な」操作です。

```git branch -D <branch>```

指定したブランチにマージされていない変更が残っていたとしてもそれを強制的に
削除するコマンドです。
このコマンドは、特定の開発ラインで行われたすべてのコミットを完全に破棄する場合に使用します。

```git branch -m <branch>```

現在のブランチの名前を <branch> に変更します。

[www.atlassian.com](https://www.atlassian.com/ja/git/tutorial/git-branches#!branch)

## git revert

git revert は、コミットされたスナップショットを元に戻すコマンドです。
ただし、プロジェクト履歴においてそのコミットがなかったものとするのではなく
そのコミットによって加えられた変更を元に戻す方法を見出してその結果を新しいコミットとして
追加するものです。
これは、Git の履歴を保全するためであり、
このことはバージョン履歴の完全性の維持とコラボレーションの信頼性の確保には必須です。

```git revert <commit>```

<commit>によって加えられたすべての変更を元に戻す新しいコミットを生成し、
それを現在のブランチに適用するコマンドです。

(www.atlassian.com)[https://www.atlassian.com/ja/git/tutorial/undoing-changes#!revert]
