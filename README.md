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

ブランチに行った変更を取り込むコマンドです。
このコマンドでは、マージ対象ブランチがHEADの指しているブランチに取り込まれます。

```git merge <マージ対象ブランチ>```


参考サイト

[Qiita](http://qiita.com/LOUIS_rui/items/8e66f6f8f1a536830081)

[サルでもわかるGit入門](http://www.backlog.jp/git-guide/stepup/stepup2_4.html)

## git rebase -i

コミット内容を修正するコマンドです。
- コミットメッセージの変更
- コミット内容の変更
- コミットの分割
- コミットの統合
- コミットの削除

```git reabase -i <コミット番号>```

コマンドを実行するとエディタが起動するので、変更内容を記載していく。
* pick = use commit
* reword = use commit, but edit the commit message
* edit = use commit, but stop for amending
* squash = use commit, but meld into previous commit
* fixup = like "squash", but discard this commit's log message
* exec = run command (the rest of the line) using shell
* drop = remove commit

参考サイト

[あのコミットをなかった事に。git rebase -i の使い方](http://www.karakaram.com/git-rebase-i-usage)

[サルでもわかるGit入門](http://www.backlog.jp/git-guide/stepup/stepup7_6.html)

# 12 git reset
HEADの位置を変更するコマンド。
オプションによってインデックス、ワーキングツリーの内容も変更できる。
* --soft HEADの位置のみを変更する。インデックス、ワーキングツリーには影響なし
* --mixed HEADの位置とインデックスを変更する。ワーキングツリーには影響なし
* --hard HEADの位置、インデックス、ワーキングツリーをすべて変更する。  

インデックスはADDなどの情報。  
ワーキングツリーは現在の変更状態のこと  

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

## git init

git init は Git リポジトリを新たに作成するコマンドです。
このコマンドは、バージョン管理を行っていない既存のプロジェクトを Git リポジトリに変換する場合や、空の新規リポジトリを作成して初期化する場合に使用します。
このコマンドを除く他のコマンドはほとんどすべて初期化されたリポジトリ以外には適用することができないため、このコマンドは新規プロジェクトを開始する場合に通常最初に実行するコマンドです。

git init コマンドを実行すると、
リポジトリに付随するすべてのメタデータを有する .git サブディレクトリがプロジェクトの
ルートに作成されます。
この .git ディレクトリを除けば、既存プロジェクトには何の改変も行われません。

```git init```

カレントディレクトリを Git リポジトリに変換します。
このコマンドを実行するとカレントディレクトリに .git フォルダーが作成され、
プロジェクトのバージョンの管理を開始することができます。

```git init <directory>```

指定したディレクトリに空の Git リポジトリを作成します。
このコマンドを実行すると、.git サブディレクトリのみを含む <directory> という名称の新規フォルダーが作成されます。

```git init --bare <directory>```

作業ディレクトリを持たない空の Git リポジトリを作成して初期化します。
共有リポジトリは必ず --bare フラグを指定して作成しなければなりません (下の補足説明参照)。
--bare フラグを指定して作成したリポジトリの名称の最後には習慣的に .git を付加します。
例えば、my-project という名称のリポジトリのベアバージョンは、
my-project.git という名称のフォルダーに格納します。

[www.atlassian.com](https://www.atlassian.com/ja/git/tutorial/git-basics#!init)

## git clone

git clone は、既存の Git リポジトリのコピーを作成するコマンドです。
作業コピーは自分自身の履歴を持ち、自分自身でファイルを管理し、
元のリポジトリとは完全に独立した環境を提供します。

利用者の便宜のため、クローンを行うと、
元のリポジトリをポイントする origin という名称のリモート接続を自動的に作成します。
これにより、極めて簡単に中央リポジトリとの通信を行うことができます。

```git clone <repo>```

<repo> にあるリポジトリをローカルマシーンにクローンするコマンドです。
元のリポジトリはローカルマシーンに存在しても、
HTTP や SSH を用いてアクセスするリモートマシーンに存在しても構いません。

```git clone <repo> <directory>```

<repo> にあるリポジトリをローカルマシーン上の <directory> という名称のフォルダーに
クローンするコマンドです。
