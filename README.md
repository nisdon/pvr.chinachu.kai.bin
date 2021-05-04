# pvr.chinachu.kai.bin
## 1. はじめに
これはkodi(leia)用のPVRアドオンです。  
EPGStationをTVチューナーサーバーとして使用します。  
pvr.chinachuをベースにEPGStation対応したものです。  

## 2. pvr.chinachuとの主な違い
### ガイド
- 表示される番組名のフィルター条件が異なる。
- 番組表はkodiの仕様（デフォルト120分）に基いて定期的に更新されます。
- ガイドの表示日数、更新間隔は「PVR & TV放送」の「ガイド」で変更できます。

### ライブ視聴
- ストリーミングは無圧縮のみ（「ストリーミング」設定は無効）です。
- 処理するインターフェースが異なる。

### タイマー
- 新規の「手動予約」として開始、終了時間を指定した予約ができます。

### タイマールール
- ルールに紐づいたタイマーを表示。
- 設定された情報はkodi起動時に一度だけ読込みます。

### 録画
- 表示される録画名のフィルター条件が異なる。
- 録画開始の通知は即時に表示します。
- 録画終了の通知は当該時間の10秒後に表示します。
- 録画開始、終了時は当該時間の30秒後に録画情報を更新します。
- コンテキストメニュー「エンコードの実行」でEPGStationのencode設定（2番目の定義）を手動実行します。
- ルールにより追加されたタイマーも削除できます。
- サムネイルの取得位置は固定(「サムネイルの位置｣設定は無効)です。

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
- タイマールール追加時のバグ修正。
- 録画の開始、又は終了から３０秒後に通知する。

### 0.0.0.8
- 録画の時刻指定予約を実装。

### 0.0.0.9
- 録画予約終了時間を過ぎていても表示する。
- 録画開始、終了の通知は当該時間の60秒後に表示します。
- 録画終了時のサムネイルチェックを削除。

### 0.0.0.10
- ルールで追加されたタイマーを削除可能にする。

### 0.0.0.11
- 無効化された録画予約を一覧に表示する。
- 録画予約の属性allowEndLackをデフォルトでfalseに変更。

### 0.0.0.12
- EPG取得処理の修正。

### 0.0.0.13
- EPG取得処理のバグ修正。

### 0.0.0.14
- 録画開始、終了から通知等の時間を変更。
- スレッドのlock処理を変更。

### 0.0.0.15
- EPG取得時のlockを外す。

### 0.0.0.16
- データ別にlock処理を分散。

### 0.0.0.17
- 予約の登録をEPGの範囲内に制限。
- IsEPGTagPlayableの戻り値を常にfalseに変更。
- IsEPGTagRecordableを現在時間の前後で切り替え。

### 0.0.0.18
- 起動時にEPGStationの接続をチェックする。

### 0.0.0.19
- 録画コンテキストメニューに「ドロップログの表示」を追加。

### 0.0.0.20
- kodi 18.4以上のライブTV視聴問題に対応。

## 4. 使用条件
- EPGStationのconfig設定として"convertDBStr=twoByte"を定義。
- raspberry pi3、及びWindows 64bit。
- raspberry piで使用する場合、kodi v18.4以前を推奨。
