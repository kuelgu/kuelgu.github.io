---
layout: post
title: Cardboard Unity SDK & ハコスコ & あいぽん
---
# Cardboardとハコスコとあいぽんで遊ぶ

なんだかんだで結局休みにしてしまったのでキャンセルしてしまった
unrealフェスの実況ツイートなんかを横目に見ながら，届いたハコスコと
Cardboardで遊んで見る。

## demoからこつこつと

https://developers.google.com/cardboard/unity/guide?hl=ja

ここら参考に環境構築も兼ねてデモアプリの構築から入ってみた。
とりあえずの目標は自作のモデルを使用して，２眼で立体視できるところまで。
ちなみにunityもxcodeもちょこっと触った程度の知識しかないので変な事やってる
可能性もあり。

---

### リンカのエラー

```
ld: '/Users/***/***/***/Fabric.framework/Fabric(FABObfuscator.o)' does not contain bitcode. You must rebuild it with bitcode enabled (Xcode setting ENABLE_BITCODE), obtain an updated library from the vendor, or disable bitcode for this target. for architecture arm64
clang: error: linker command failed with exit code 1 (use -v to see invocation)
```

Xcodeでビルドした際にでたエラー。Build SettingsからAllを選択してENABLE_BITCODEで検索。
YESからNOに変更したらビルドできた。

理由はこのへん。ちゃんとは読んでない。

http://qiita.com/Takumi_Mori/items/ace01198c43c8bac6df0

---

### process launch failed: Security

XcodeでRunした時に発生。
iPhoneの設定→一般→プロファイル
から該当のプロファイルを選択して，「信頼する」をタップすることで
実行可能になる。

---

### そんなこんなで

実機表示はできた

![demo](/assets/images/IMG_1868.PNG)

とりあえずここまで。モデル作んないと続きができないので次はモデル作成をば。
