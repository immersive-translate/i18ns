# DeepL

## [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/)を開設した後、DeepL 翻訳サービスに直接アクセス（推奨）

[Learn More](https://immersivetranslate.com/en/pricing/)

## DeepL 公式 API を DeepL 経由で取得

1. 公式紹介：[DeepL API](https://www.deepl.com/en/pro#developer)

   - 注意：[DeepL API](https://www.deepl.com/en/pro#developer)と[DeepL Pro](https://www.deepl.com/pro)は異なるアカウントタイプであり、[DeepL API](https://www.deepl.com/en/pro/select-country#developer)アカウントです。

2. なぜ[DeepL](https://www.deepl.com/en/whydeepl)を選ぶのか？

   - 英語 ⇄ 中国語 5 倍の精度
   - 英語 ⇄ 日本語 6 倍の精度
   - 人工知能技術（ニューラルネットワーク）に基づく翻訳エンジン

3. Deepl API は[Free API と Pro API](https://www.deepl.com/en/pro#developer)に分かれています

   - Free API は月に 500,000 文字の無料提供があります。
   - Pro API の[公式料金](https://www.deepl.com/en/pro#developer)は：1 百万文字あたり 25 ドルです。
   - 高頻度ユーザーの場合、月に消費する文字数は約 1 千万文字で、価格は約 250 USD です。

4. アカウントを登録し、[DeepL API](https://www.deepl.com/en/pro#developer)を開設します。

## 一般的な問題

### 1. 入力したキーが利用できません。

DeepL API Pro と DeepL Pro は 2 種類のアカウントで、Immersive Translate で使用できる Auth Key は DeepL API アカウントです。[DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)をクリックしてください。

### 2. 401、403 認証エラーのトラブルシューティング

これらのエラーは通常、誤ったタイプの認証キーを使用している場合に発生します。注意してください：

1. DeepL は 2 つの異なる製品を提供しています：DeepL Pro（翻訳サービス）と DeepL API（開発者インターフェース）
2. DeepL Pro アカウント設定で見つかるキーは API 呼び出しと**互換性がありません**
3. API キーを取得するには、特に DeepL API アカウントを登録する必要があります
4. DeepL Free API キーは`:fx`で終わることで識別されます
5. DeepL Pro API キーには`:fx`サフィックスがなく、通常の文字列として表示されます

DeepL Pro 翻訳サービスだけでなく、DeepL API サービスに正しく登録されていることを確認してください。

### 3. 456、ユーザーのクォータが上限に達しました。

使用量が DeepL の公式ハードリミットを超えたため、DeepL の公正使用ポリシーに違反した可能性があります。このような行動を避けることをお勧めします。有料会員の場合、使用量は翌月に自動的にリセットされます。
