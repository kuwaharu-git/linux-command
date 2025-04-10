
# cut

## 概要
ファイルや入力から指定した部分（列や文字）を切り出して表示するためのユーティリティ

## 基本構文
```
cut [オプション] [ファイル]
```

## 主なオプション
| オプション     | 説明                          |
|----------------|-------------------------------|
| `-b`          | バイト単位で切り出し位置を指定する |
| `-c`          | 文字単位で切り出し位置を指定する |
| `-f`          | フィールド（列）を指定して切り出す（デフォルトはタブ区切り） |
| `-d`          | フィールドの区切り文字を指定する（`-f`と一緒に使用） |
| `--complement` | 指定した部分以外を表示する |
| `-s`          | 区切り文字を含まない行を抑制する（`-f`と一緒に使用） |

## 使用例
### 基本例
```
cut -c 1-5 file.txt
```
`file.txt`の各行の1～5文字目を切り出して表示

### 応用例
```
cut -f 2 -d ',' data.csv
```
`data.csv`の各行をカンマで区切り、2番目のフィールドを切り出して表示

## 関連コマンド
- `awk`: より柔軟なテキスト処理が可能
- `sed`: テキストの置換や編集に特化

## 注意点
- 入力が指定されない場合、標準入力から読み込みます。
- `-b`や`-c`で範囲指定する際、範囲外の指定は無視されます。
- マルチバイト文字（例: UTF-8）を扱う場合、`-c`が期待通りに動作しない可能性があります。
