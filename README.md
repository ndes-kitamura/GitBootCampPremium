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
