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
*内容
ブランチに行った変更を取り込む
*オプション
'''git merge <マージ対象ブランチ>'''


※参考サイト
[Qiita](http://qiita.com/LOUIS_rui/items/8e66f6f8f1a536830081)

10. git rebase i

*内容
コミットを修正する
- コミットメッセージの変更
- コミット内容の変更
- コミットの分割
- コミットの統合
- コミットの削除

*オプション
'''git reabase -i <コミット番号>'''

※参考サイト
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
