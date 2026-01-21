# Open AI (Azure OpenAI)

[Immersive Translate プロメンバーシップ](https://immersivetranslate.com/en/pricing/)を開いて OpenAI 翻訳サービスに直接アクセス (推奨)

[プレゼンテーションはこちらをクリック](https://immersivetranslate.com/en/pricing/)

## 公式 OpenAI 開発者プラットフォームから API キーを取得

- [openAI API 公式アドレス](https://openai.com/api/)
  - 注意：現在、OpenAI は中国の携帯電話番号による登録を受け付けていません。
- OpenAI アカウントに登録後、[API Secret Key](https://platform.openai.com/account/api-keys)を開いて API Secret Key を作成
- その後、Immersive Translate 拡張機能の OpenAI 設定にキーを入力するだけです。

## 注意事項

1. **クレジットカードが紐付けられていない場合、または新しい OpenAI 5 刃ユーザーで 1 分間に最大 3 リクエストの場合**、基本的に使用できず、エラーが発生するのは正常です。[ここをクリックして API の頻度制限を確認できます](https://platform.openai.com/account/rate-limits)
2. OpenAI の API と ChatGPT は 2 つの異なるサービスです。Immersive Translate 拡張機能は OpenAI の API をサポートしており、ChatGPT の Web 版ではありません。そのため、ChatGPT plus を開くのではなく、OpenAI の API サービスを開き、開いた後に設定ページで API キーを入力する必要があります。
3. 429 エラーは、openai の頻度制限を超えたことを意味します。1 秒あたりの最大リクエスト数を減らすことをお勧めします。特に電子書籍を翻訳する場合、有料版であっても 1 秒あたりの最大リクエスト数を減らし、1 秒あたり 5 リクエストに調整してより安定させる必要があります。
4. OpenAI gpt-3.5-turbo モデルの価格は:$0.002 / 1K トークンで、66 万英単語の翻訳に約 1 ドル、17 万英単語の翻訳に 0.25 ドルかかります。
5. Immersive Translate 拡張機能は負荷分散のために複数の API キーをサポートしています。フォームに入力する際は、カンマ`,`を使用して異なるキーを区切ってください。

## 現在のリクエスト数の推奨

最近、OpenAI は有料ユーザーに対しても非常に制限的になっており、バージョン 0.5.0 の時点でデフォルトのリクエスト数が秒に変更され、デフォルトの 1 秒あたりの最大リクエスト数が 10 リクエストに変更されました。

## Azure OpenAI

OpenAI 翻訳サービスは Azure OpenAI インターフェースとも互換性があります。まず、Azure コンソールで OpenAI サービスを作成し、次に Azure AI Studio に移動します:https://oai.azure.com、gpt-35-turbo デプロイメントを作成し、デプロイメント名を覚えておいてください

gpt-35-turbo モデルをデプロイした後、Immersive Translate の OpenAI 設定ページを開きます：

1. Api Key には、Azure コンソールが提供するキーを入力してください
2. クリックして詳細設定を展開し、カスタマイズされたアドレスを次のように設定します：

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2024-07-01-preview`

`{your-custom-name}`を自分のサブドメインに、`{you-deployment-name}`を自分のデプロイメント名に変更してください。

3. モデル名は、カスタムモデルとして手動で選択する必要があります：`gpt-35-turbo`

> まだ質問がある場合は、Azure AI Studio 内に移動し、PlayGround を開き、[View Code]をクリックすると、下部に最終的な[EndPoint]と[Key]が表示されます：

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## OpenAI の API アドレスのカスタマイズ

- これは`詳細設定`で次のエントリポイントを使用して設定できます

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
