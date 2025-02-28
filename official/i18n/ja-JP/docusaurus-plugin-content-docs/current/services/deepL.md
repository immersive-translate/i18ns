# DeepL

## [Immersive Translate Pro Membership](https://immersivetranslate.com/en/pricing/)を開設した後、DeepL翻訳サービスに直接アクセス（推奨）

[Learn More](https://immersivetranslate.com/en/pricing/)

## DeepL公式APIをDeepL経由で取得

1. 公式紹介：[DeepL API](https://www.deepl.com/en/pro#developer)

   - 注意：[DeepL API](https://www.deepl.com/en/pro#developer)と[DeepL Pro](https://www.deepl.com/pro)は異なるアカウントタイプであり、[DeepL API](https://www.deepl.com/en/pro/select-country#developer)アカウントです。

2. なぜ[DeepL](https://www.deepl.com/en/whydeepl)を選ぶのか？

   - 英語 ⇄ 中国語 5倍の精度
   - 英語 ⇄ 日本語 6倍の精度
   - 人工知能技術（ニューラルネットワーク）に基づく翻訳エンジン

3. Deepl APIは[Free APIとPro API](https://www.deepl.com/en/pro#developer)に分かれています

   - Free APIは月に500,000文字の無料提供があります。
   - Pro APIの[公式料金](https://www.deepl.com/en/pro#developer)は：1百万文字あたり25ドルです。
   - 高頻度ユーザーの場合、月に消費する文字数は約1千万文字で、価格は約250 USDです。

4. アカウントを登録し、[DeepL API](https://www.deepl.com/en/pro#developer)を開設します。

## 一般的な問題

### 1. 入力したキーが利用できません。

DeepL API ProとDeepL Proは2種類のアカウントで、Immersive Translateで使用できるAuth KeyはDeepL APIアカウントです。[DeepL API Pro](https://www.deepl.com/en/pro/select-country#developer)をクリックしてください。

### 2. 401、403認証エラーのトラブルシューティング

これらのエラーは通常、誤ったタイプの認証キーを使用している場合に発生します。注意してください：

1. DeepLは2つの異なる製品を提供しています：DeepL Pro（翻訳サービス）とDeepL API（開発者インターフェース）
2. DeepL Proアカウント設定で見つかるキーはAPI呼び出しと**互換性がありません**
3. APIキーを取得するには、特にDeepL APIアカウントを登録する必要があります
4. DeepL Free APIキーは`:fx`で終わることで識別されます
5. DeepL Pro APIキーには`:fx`サフィックスがなく、通常の文字列として表示されます

DeepL Pro翻訳サービスだけでなく、DeepL APIサービスに正しく登録されていることを確認してください。

### 3. 456、ユーザーのクォータが上限に達しました。

使用量がDeepLの公式ハードリミットを超えたため、DeepLの公正使用ポリシーに違反した可能性があります。このような行動を避けることをお勧めします。有料会員の場合、使用量は翌月に自動的にリセットされます。