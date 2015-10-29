# GitBootCampPremium


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