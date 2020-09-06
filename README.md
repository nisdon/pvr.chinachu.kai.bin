# pvr.chinachu.kai.bin
## 1. はじめに
これは、pvr.chinachu（kodi用のPVRアドオン）に対してepgstation（ＴＶサーバー）対応の修正を加えたものです。

## 2. pvr.chinachuとの主な違い
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
- 起動時のクラッシュ対策を追加。
- 録画コンテキストメニューに「エンコードの実行」を追加。（EPGStation-config内に定義した2番目のエンコード設定）

## 3. 使用条件
- EPGStationのconfig設定として"convertDBStr=twoByte"を定義。
