# Open AI (Azure OpenAI)

[Immersive Translateプロメンバーシップ](https://immersivetranslate.com/en/pricing/)を開いてOpenAI翻訳サービスに直接アクセス(推奨)

[プレゼンテーションはこちらをクリック](https://immersivetranslate.com/en/pricing/)

## 公式OpenAI開発者プラットフォームからAPIキーを取得

- [openAI API公式アドレス](https://openai.com/api/)
  - 注意：現在、OpenAIは中国の携帯電話番号による登録を受け付けていません。
- OpenAIアカウントに登録後、[API Secret Key](https://platform.openai.com/account/api-keys)を開いてAPI Secret Keyを作成
- その後、Immersive Translate拡張機能のOpenAI設定にキーを入力するだけです。

## 注意事項

1. **クレジットカードが紐付けられていない場合、または新しいOpenAI 5刃ユーザーで1分間に最大3リクエストの場合**、基本的に使用できず、エラーが発生するのは正常です。[ここをクリックしてAPIの頻度制限を確認できます](https://platform.openai.com/account/rate-limits)
2. OpenAIのAPIとChatGPTは2つの異なるサービスです。Immersive Translate拡張機能はOpenAIのAPIをサポートしており、ChatGPTのWeb版ではありません。そのため、ChatGPT plusを開くのではなく、OpenAIのAPIサービスを開き、開いた後に設定ページでAPIキーを入力する必要があります。
3. 429エラーは、openaiの頻度制限を超えたことを意味します。1秒あたりの最大リクエスト数を減らすことをお勧めします。特に電子書籍を翻訳する場合、有料版であっても1秒あたりの最大リクエスト数を減らし、1秒あたり5リクエストに調整してより安定させる必要があります。
4. OpenAI gpt-3.5-turboモデルの価格は:$0.002 / 1K トークンで、66万英単語の翻訳に約1ドル、17万英単語の翻訳に0.25ドルかかります。
5. Immersive Translate拡張機能は負荷分散のために複数のAPIキーをサポートしています。フォームに入力する際は、カンマ`,`を使用して異なるキーを区切ってください。

## 現在のリクエスト数の推奨

最近、OpenAIは有料ユーザーに対しても非常に制限的になっており、バージョン0.5.0の時点でデフォルトのリクエスト数が秒に変更され、デフォルトの1秒あたりの最大リクエスト数が10リクエストに変更されました。

## Azure OpenAI

OpenAI翻訳サービスはAzure OpenAIインターフェースとも互換性があります。まず、AzureコンソールでOpenAIサービスを作成し、次にAzure AI Studioに移動します:https://oai.azure.com、gpt-35-turboデプロイメントを作成し、デプロイメント名を覚えておいてください

gpt-35-turboモデルをデプロイした後、Immersive TranslateのOpenAI設定ページを開きます:

1. Api Keyには、Azureコンソールが提供するキーを入力してください
2. クリックして詳細設定を展開し、カスタマイズされたアドレスを次のように設定します:

`https://{your-custom-name}.openai.azure.com/openai/deployments/{you-deployment-name}/chat/completions?api-version=2024-07-01-preview`

`{your-custom-name}`を自分のサブドメインに、`{you-deployment-name}`を自分のデプロイメント名に変更してください。

3. モデル名は、カスタムモデルとして手動で選択する必要があります:`gpt-35-turbo`

> まだ質問がある場合は、Azure AI Studio内に移動し、PlayGroundを開き、[View Code]をクリックすると、下部に最終的な[EndPoint]と[Key]が表示されます:

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/azure-openai-key.jpg)

## OpenAIのAPIアドレスのカスタマイズ

- これは`詳細設定`で次のエントリポイントを使用して設定できます

---

<img width="951" alt="Snipaste_2023-04-08_19-29-18" src="https://user-images.githubusercontent.com/5794691/230718739-ff661ce3-04af-4391-8efc-9a5a1c8374b0.png"/>

---
