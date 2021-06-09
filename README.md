# pvr.chinachu.kai.bin
## 1. はじめに
これはkodi v18(leia)用のPVRアドオンです。  
pvr.chinachuをベースにカスタマイズしたものです。  
TVチューナーサーバーはEPGStation v2を対象としています。

## 2. 主な特徴
### ガイド
- 基本的にkodiの設定に従い表示します。
- 番組データの取得はEPGStationから最大日数を取得します。
- 設定「EPGの範囲内で表示」をOFFすることでkodi設定の範囲外にある予約情報を表示できます。

### ライブ視聴
- EPGStationのm2tsで定義されたものを視聴できます。
- 使用するモードは設定「m2tsモード」で指定します。

### タイマー
- 「手動予約」に対応しています。
- allowEndLackは設定「番組頭切れ防止」で指定します。

### タイマールール
- 「手動予約ルール」に対応しています。
- 設定はkodi起動時にのみ読込みます。

### 録画
- 録画開始、終了は即時通知します。
- コンテキストメニュー「ドロップ表示」でドロップの有無を表示します。

## 3. 設定項目
### 基本設定
| 項目 | 説明 |
----|----
|EPGStation WUIのURL|例 http://localhost:8888|

### 予約
| 項目 | 説明 |
----|----
|EPGの範囲内で表示|kodiで設定されている範囲内の情報を表示。|
|番組頭切れ防止|予約オプションのallowEndLackを設定。|
|m2tsモード|EPGStationで定義されているm2tsモードを指定。|

### 録画
| 項目 | 説明 |
----|----
|サムネイルを表示する|録画データのイメージにサムネイルを用いる。|

## 4. 使用条件
- raspberry pi3、及びWindows 64bit。
