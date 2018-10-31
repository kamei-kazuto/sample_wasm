## emscripten SDKのインストール
https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html

下記の内容でインストール
```
git clone https://github.com/juj/emsdk.git
./emsdk install latest
./emsdk activate latest
```

毎回、読み込むように設定する。
```
source ./emsdk_env.sh
```

## chromeの設定を切り替える

下記にアクセスしてwasm threadの項目を有効にする。
```
chrome://flags
```

## コンパイルのコマンド
```
emcc -O2 -s USE_PTHREADS=1 -s PTHREAD_POOL_SIZE=2 -o test.js test.c
```

## 開く

```
yarn open
```