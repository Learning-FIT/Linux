## 簡単なシェルスクリプトの作成

```bash
#!/bin/bash

echo "Hello, $1-san!"
ls -al ~/ > "$1-ls.txt"
```

## コマンドの実行

```bash
#!/bin/bash

datetime=`date +'%Y%m%d%H%M%S'`
echo $datetime
```

## 条件分岐

```bash
#!/bin/sh

if [ $1 -gt 10 ]; then
  echo "$1 > 10"
elif [ $1 -eq 10 ]; then
  echo "$1 == 10"
else
  echo "$1 < 10"
fi
```

## ファイル／ディレクトリの存在確認

```bash
#!/bin/bash

if [ -f hello.sh ]; then
  echo "file exitsts"
else
  echo "file not exists"
fi
```

## 終了ステータス

```bash
#!/bin/bash

if [ -f hello.sh ]; then
  exit 0
else
  exit 1
fi
```

## 繰り返し処理

```bash
#!/bin/bash

sum=0
for i in `seq 1 1 $1` ; do
  let 'sum=sum+i'
done
echo $sum
```
