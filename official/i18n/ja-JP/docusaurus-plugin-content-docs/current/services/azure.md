# マイクロソフト Azure 翻訳

## 簡単な説明

1. 公式ウェブサイト：[マイクロソフト Azure 翻訳](https://learn.microsoft.com/ja-jp/azure/cognitive-services/translator/text-translation-overview)
2. 公式説明：毎月200万文字までの翻訳は無料です。毎月200万文字を超える場合は、10ドル/100万文字の料金がかかります。詳細は[価格説明](https://azure.microsoft.com/ja-jp/pricing/details/cognitive-services/translator/)を参照してください。

## 登録プロセス

登録プロセスは他の翻訳サービスに比べてやや複雑で、忍耐が必要です。

参考リンク：[マイクロソフト Azure 翻訳入門ドキュメント](https://learn.microsoft.com/ja-jp/azure/cognitive-services/translator/document-translation/quickstarts/get-started-with-rest-api?pivots=programming-language-csharp)

## Azure アカウントの登録

第一歩として、[Azure](https://azure.microsoft.com/ja-jp/free/cognitive-services/) アカウントを登録します。国際クレジットカード（Visa/Master）の紐付けが必要です。これがないと登録できません。

## Azure Blob ストレージアカウントの登録

第二段階では、[Azure Blob](https://portal.azure.com/#create/Microsoft.StorageAccount) ストレージアカウントを登録します。

1. 新しいリソースグループを作成し、ストレージアカウント名を入力します。
2. 地域は、最も近い地域を選択します。例えば、香港地域であれば `East Asia` です。
3. 残りのプロセスは、直接次へ進むだけです。最後のページで、デプロイが完了したら、左下の青いボタン「作成」をクリックします。

## 翻訳ツールの作成

第三段階では、[翻訳ツール](https://portal.azure.com/#create/Microsoft.CognitiveServicesTextTranslation) を作成します。
1. 地域は、最も近い地域を選択します。例えば、香港地域であれば `East Asia` です。
2. 課金層は、ニーズに応じて選択します。無料ユーザーは `Free F0` を選択できます。無料層は文書翻訳をサポートしていません。必要に応じて、標準の S1 を試用できます。
3. 残りのプロセスは、直接次へ進むだけです。最後のページで、デプロイが完了したら、左下の青いボタン「作成」をクリックします。

## アクセスキー

デプロイが成功した後、[Azureダッシュボード](https://portal.azure.com/#home)にアクセスし、**翻訳ツール**のページに入ります。左側のメニューからリソース管理の`キーとエンドポイント`を選択し、キーを見つけます。Microsoftは2つのキーを提供しており、どちらか一方を選択して、沈没型エクステンション - Microsoft翻訳の`APIKEY`に入力します。

キーの下には`位置/リージョン`の情報もあります。例えば`eastasia`など、これも沈没型エクステンション - Microsoft翻訳の`region`に入力する必要があります。

## よくある質問

疑問がある場合は、[こちら](https://github.com/immersive-translate/immersive-translate/issues/137)でフィードバックしてください。