# 都道府県データ (Prefecture Data)

特定の用途で地域ごとにグループ化した都道府県データをJSON形式で作成したものです。

## データ構造

以下の地域ごとにグループ化

- area1: 北海道・東北地方
- area2: 関東地方
- area3: 中部地方
- area4: 近畿地方
- area5: 中国・四国地方
- area6: 九州・沖縄地方

## 使用方法

### CDN経由での利用

jsDelivr CDNを使用して、以下のURLからデータを取得できます：

```
https://cdn.jsdelivr.net/gh/siva-shimizu/prefecture-data@main/prefectures_v2.json
```
  
### 使用例

```javascript
async function fetchPrefectureData() {
  const response = await fetch('https://cdn.jsdelivr.net/gh/siva-shimizu/prefecture-data@main/prefectures_v2.json');
  const data = await response.json();
  return data;
}
```

## スプレッドシートの設定方法

Google スプレッドシートからデータを取得して表示することもできます。

ただしスプレッドシートを利用する場合は、閲覧されることを想定し機密情報や個人情報などを含めないように注意してください。  

スプレッドシートのサンプルはこちら
https://docs.google.com/spreadsheets/d/1CzMPGVefSwauIiXfDNm8IekrI-91pcjP5ZslLa6zSI0/edit?gid=0#gid=0

### 1. スプレッドシートの作成

1. Google スプレッドシートを新規作成します
2. 以下の地域ごとにシートを作成します：
   - 北海道・東北エリア
   - 関東・東京エリア
   - 中部エリア
   - 関西・大阪エリア
   - 中国・四国エリア
   - 九州・沖縄エリア

3. 各シートの1行目にヘッダーを設定します：
   ```
   都道府県名 | 店舗名 | 説明 | URL
   ```

4. 2行目以降にデータを入力します：
   ```
   北海道 | 札幌店 | 札幌駅から徒歩5分 | https://example.com
   ```

### 2. セキュリティと権限の設定

スプレッドシートのデータを保護するため、以下の設定を行うことをお勧めします：

1. **閲覧専用に設定する**：
   - スプレッドシートの「共有」ボタンをクリック
   - 「リンクを知っている人全員」を選択
   - 権限を「閲覧者」に設定 ※他者編集はできないようにしてください

2. **重要な注意点**：
   - スプレッドシートをウェブに公開すると、公開されたデータは誰でも閲覧できます
   - 機密情報や個人情報を含めないようにしてください

### 3. スプレッドシートをウェブに公開

1. スプレッドシートの「ファイル」メニューから「ウェブに公開」を選択します
2. 「ドキュメント全体」を選択し、「ウェブページ」形式にして「公開」ボタンをクリックします
3. スプレッドシートのURLからIDを取得します：
   - URLが `https://docs.google.com/spreadsheets/d/XXXXXXXXXXXXXXXXXXXX/edit` の形式の場合
   - `XXXXXXXXXXXXXXXXXXXX` の部分がスプレッドシートID

### 4. コードの設定

スプレッドシートIDをコード内に設定します：

```javascript
// スプレッドシートデータ取得用の設定
const SPREADSHEET_ID = "ここにスプレッドシートID"; // スプレッドシートのIDを設定してください
```

### 4. データ形式の注意点

- 都道府県名は正式名称（「北海道」「東京都」「大阪府」「京都府」「〇〇県」）を使用してください
- URLは完全なURL（https://から始まるもの）を入力してください
- データが存在しない都道府県は、地図上でクリックできなくなります（自動的に無効化されます）

## ご利用について

商用・非商用を問わず、自由に使用、変更、配布することができます。
＊このデータの使用によって生じたいかなる損害についても責任を負いません。
