# 都道府県データ (Prefecture Data)

このリポジトリは日本の都道府県データをJSON形式で作成したものです。
特定の用途で地域ごとにグループ化しております。

## データ構造

データは以下の地域ごとにグループ化されています：

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
https://cdn.jsdelivr.net/gh/siva-shimizu/prefecture-data@main/prefectures.json
```

### 使用例

```javascript
async function fetchPrefectureData() {
  const response = await fetch('https://cdn.jsdelivr.net/gh/siva-shimizu/prefecture-data@main/prefectures.json');
  const data = await response.json();
  return data;
}
```

## ライセンス

このデータセットは[MITライセンス](https://opensource.org/licenses/MIT)の下で公開されています。商用・非商用を問わず、自由に使用、変更、配布することができます。

## 免責事項

このデータは情報提供のみを目的としています。データの正確性や完全性は保証されません。このデータの使用によって生じたいかなる損害についても責任を負いません。
