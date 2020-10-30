# pvr.chinachu.kai.bin
## 1. はじめに
これはkodi(leia)用のPVRアドオンです。  
EPGStationをTVチューナーサーバーとして使用します。  
pvr.chinachuをベースにEPGStation対応したものです。  

## 2. pvr.chinachuとの主な違い
### ガイド
- 表示される番組名のフィルター条件が異なる。
- 番組表はkodiの仕様（デフォルト120分）に基いて定期的に更新されます。
- ガイドの更新間隔は「PVR & TV放送」の「ガイド」で変更できます。

### ライブ視聴
- ストリーミングは無圧縮のみ（「ストリーミング」設定は無効）です。
- 処理するインターフェースが異なる。

### タイマー
- 同じです。

### タイマールール
- ルールに紐づいたタイマーを表示。
- 設定された情報はkodi起動時に一度だけ読込みます。

### 録画
- 表示される録画名のフィルター条件が異なる。
- 録画開始、終了の通知は当該時間の30秒後に表示します。
- 番組の途中録画、キャンセルの通知は5秒後に表示します。
- コンテキストメニュー「エンコードの実行」でEPGStationのencode設定（2番目の定義）を手動実行します。
- 録画のサムネイルは、録画終了後の通知表示時に設定します。
- 録画終了時にサムネイルが作成されない場合は１０分間隔でチェック。

### クライアント固有の設定
- 全ての項目が機能。

## 3. 更新履歴
### 0.0.0.1
- ライブ視聴処理で使用する関数を変更。
- ライブ視聴のストリーミングは無圧縮のみ有効。
- ルールと、それにより予約された情報を紐づけて表示させる。
- クライアント固有の設定で用意された処理を機能させる。
- 番組表の取得をＴＶガイドの設定に準拠する。
- 録画の開始と同時に通知する。
- 録画終了から１０秒後に通知する。
- 途中録画開始から５秒後に通知する。
- 録画キャンセルから５秒後に通知する。
- 録画終了時にサムネイルが表示されない場合は１０分間隔でチェック。

### 0.0.0.2
- 録画の開始から１０秒後に通知する。
- 稼働中のクラッシュ対策を追加。

### 0.0.0.3
- 録画コンテキストメニューに「エンコードの実行」を追加。（EPGStation-config内に定義した2番目のエンコード設定）
- 起動時のクラッシュ対策を追加。

### 0.0.0.4
- 稼働中のクラッシュ対策を追加。

### 0.0.0.5
- 録画の開始から１５秒後に通知する。
- 録画の終了から３０秒後に通知する。
- スレッドのlock時間を改善。

### 0.0.0.6
- 録画開始、終了時の処理を軽減。

### 0.0.0.7
- タイマールール追加時のバグ修正録。
- 録画の開始、又は終了から３０秒後に通知する。

## 4. 使用条件
- EPGStationのconfig設定として"convertDBStr=twoByte"を定義。
- raspberry pi3、及びWindows 64bit。
- raspberryで使用する場合、kodi v18.4以前を推奨。
