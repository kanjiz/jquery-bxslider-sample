---
marp: true
theme: default
---

# jQueryの導入方法

## CDNを使用したシンプルな実装

---

# 目次

1. jQueryとは
2. CDNによる導入
3. 記述場所
4. 基本的な使用方法
5. よくある問題と解決策

---

# 1. jQueryとは

- JavaScriptライブラリ
- DOM操作を簡単に
- クロスブラウザ対応
- 豊富なプラグイン

---

# 2. CDNによる導入

```html
<script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
```

## CDN使用の利点

- **高速な配信**: 世界中のCDNサーバーから配信
- **キャッシュの活用**: ブラウザのキャッシュを利用
- **容易な導入**: 1行のコードで実装可能
- **セキュリティ**: SRI対応で安全

---

# 3. 記述場所

## 推奨: bodyタグの閉じタグ直前

```html
<body>
    <!-- コンテンツ -->
    <script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
    <script>
        $(function() {
            // jQueryのコード
        });
    </script>
</body>
```

- ページの読み込み速度が最適化される
- コンテンツの表示が優先される

---

# 3. 記述場所（続き）

## head内の場合

```html
<head>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
    <script>
        $(function() {
            // jQueryのコード
        });
    </script>
</head>
```

- 特定の機能が動作しない場合のみ使用
- ページの読み込みが遅くなる可能性あり

---

# 4. 基本的な使用方法

```javascript
// DOM読み込み完了後に実行
$(document).ready(function() {
    // jQueryコードをここに記述
});

// 短縮形
$(function() {
    // jQueryコードをここに記述
});
```

---

# 5. よくある問題と解決策

1. **読み込みエラー**
   - ネットワーク接続の確認
   - CDNのURLが正しいか確認

2. **動作しない**
   - プラグインを使用している場合、jQueryの読み込み順序を確認
   - コンソールエラーの確認

3. **バージョンの競合**
   - 複数のjQueryを読み込んでいないか確認

---

# 参考リンク

- [jQuery 公式サイト](https://jquery.com/)
- [jQuery CDN](https://code.jquery.com/)
- [jQuery API Documentation](https://api.jquery.com/)
