## シェル

1. `alias='ls -al'`
2. `find / -name *.sh | xargs grep "alias ls='ls --color=auto'"`
3. `find / -name *.sh | xargs grep "alias ls='ls --color=auto'" > results.txt`
4. `sudo find /etc -type f | sudo xargs grep "UseDNS yes" 2>/dev/null`

## まとめ

```bash
#!/bin/bash

# backupディレクトリの確認と作成
if [ ! -d ~/backup ]; then
  mkdir ~/backup
fi

# 現在日時（ファイル名）の取得
datetime=`date +'%Y%m%d%H%M%S'`
filename="$datetime.tar.gz"

# ディレクトリの移動とバックファイルの作成
cd ~/
tar cvzf $filename .bash_profile .bash_history

# バックアップファイルの移動
mv $filename ~/backup
```
