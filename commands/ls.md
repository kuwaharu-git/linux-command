
# ls

## 概要
ディレクトリの内容を一覧表示するコマンド。

## 基本構文
```
ls [オプション] [パス]
```

## 主なオプション
| オプション | 説明                          |
|------------|-------------------------------|
| `-l`       | 詳細情報付きで表示する         |
| `-a`       | 隠しファイルも含めて表示する   |
| `-h`       | 人間が読みやすい形式で表示     |
| `-t`       | 更新日時順に並べる     |
| `-r`       | 逆順に並べる (-t や -S との併用可能)     |
| `-S`       | ファイルサイズ順に並べる     |
| `-d`       | ディレクトリ自身の情報を表示し、中身は表示しない     |
| `-R`       | 再帰的にサブディレクトリを表示     |
| `-X`       | ファイルを拡張子ごとにまとめる     |


## 使用例
### 基本例
```
ls
```
現在のディレクトリの内容を一覧表示。

### 応用例
```
ls -lah
```
すべてのファイル（隠しファイル含む）を、人間が読みやすい形式の詳細情報付きで表示します。

## 関連コマンド
- `find`: ファイルやディレクトリを検索する。
- `tree`: ディレクトリ構造を階層的に表示する。

## 注意点
- 大量のファイルがあるディレクトリでは表示が煩雑になることがある。
- 権限がないディレクトリは表示できない。
