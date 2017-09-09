enert
=====

miyagaw61's python library.

install
=======

```bash
mkdir /hoge  
git clone https://github.com/miyagaw61/enert /hoge/enert    
export PYTHONPATH=$PYTHONPATH:/hoge
```

Usage
=====

* import 
```python
from enert import *
```

## fileクラス
```python
file_name = "a.out"
f = file(file_name)
```
- 編集
```python
f.edit()
```

- 行数取得
```python
f.lines()
```

- データ読み込み
```python
f.data()
```

- 行ごとに読み込み
```python
f.linedata()
```

- 書き込み
```python
f.write("hoge\n")
```

- 追記
```python
f.add("hoge\n")
```

- 存在するかどうか調査
```python
f.exist()
```

- 削除
```python
f.rm()
```

- バイナリとして読み込み
```python
f.binary()
```

- バイナリをfmt文字ごとにsplitしてリスト化して読み込み
```python
fmt = 16
f.binary(fmt)
```

## shellクラス
```python
cmd = shell("ls | grep *.txt")
```
- コマンド実行
```python
cmd.call()
```

- コマンドの出力を取得
```python
stdout_str, stderr_str = cmd.get()
```

## その他

* 文字に色を付与
```python
red_hoge = red("hoge")
bold_green_fuga = green("hoge", "bold")
```

* valueをs桁の2の補数表現で表現
```python
complement(value, s)
```

* 文字列strをn文字ごとにsplit
```python
str = "hogefugapiyo"
n = 4
list = splitn(str, n)
print(list) # -> ["hoge", "fuga", "piyo"]
```

* ターミナルのサイズを取得
```python
size_x, size_y = get_term_size()
```

* clear(Ctrl+l)する
```python
clear()
```

* 文字列をファイルに書き込む
```python
buf = "hoge"
writefile(buf, "buf.txt")
```
