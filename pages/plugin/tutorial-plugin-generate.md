---
title: プラグインジェネレータの利用方法
keywords: plugin generate spec
tags: [plugin, tutorial]
sidebar: home_sidebar
permalink: plugin_tutorial-plugin-generate
summary: プラグインの雛型を簡単に作成できるプラグインジェネレーターについて説明します。
---

## プラグインジェネレータの導入

プラグインジェネレータとは、プラグインの雛形を自動で作成するプラグインです。  

[こちら](https://www.ec-cube.net/products/detail.php?product_id=1022){:target="_blank"}からプラグインをダウンロード・インストールを行って下さい。  

プラグインのインストール方法については、[プラグイン導入方法](/plugin_install)を参考にしてください。  

## プラグインの雛形を作成する

1. インストールが完了したら、雛形を生成してます。  
![プラグインジェネレータ](/images/plugin/plugin-generate-01.png)   
設定リンクを押下します。  

1. 設定画面が表示されます。  
![プラグインジェネレータ](/images/plugin/plugin-generate-02.png)  
必要な情報を入力し、設定ボタンを押下します。  
各設定項目の内容は以下のとおりです。  

| 項目                         | 説明                                                                                                                                                                                           |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| プラグイン名を入力           | プラグイン名を入力します。                                                                                                                                                                     |
| codeを入力                   | プラグインコードを入力します。                                                                                                                                                                 |
| バージョンを入力             | バージョンを入力します。EC-CUBEのバージョン定義に従い、x.y.zの形式で入力することが推奨されます。                                                                                               |
| 作成者を入力                 | 開発者名や会社名等を入力します。                                                                                                                                                               |
| 共通イベントの設定           | チェックをつけた場合、共通フックポイントの定義が生成されます。共通フックポイントについては、[プラグイン仕様書(PDF)](http://downloads.ec-cube.net/src/manual/v3/plugin.pdf){:target="_blank"}を参考にして下さい。 |
| 管理画面用フックポイント     | 管理画面用のフックポイントを生成します。                                                                                                                                                       |
| フロント画面用フックポイント | フロント画面用のフックポイントを生成します。                                                                                                                                                   |
| メール送信用フックポイント   | メール送信用のフックポイントを生成します。                                                                                                                                                     |

1. 完了すると、`[EC-CUBEルートディレクトリ]/app/Plugin`以下にプラグインが生成されます。  
以下のように作成されていれば成功です。

```
[EC-CUBEルートディレクトリ]
    +--app
        +--Plugin
            +--[プラグインコード]
            |    +--Controller
            |    +--Form
            |    +--Resouce
            |    +--ServiceProvider
            |    +--config.yml
            |    +--CustomizeEvent.php
            |    +--event.yml
            |    +--LICENSE
            |    +--PluginManager.php
            +--PluginGenerator
                 :
                 :
```