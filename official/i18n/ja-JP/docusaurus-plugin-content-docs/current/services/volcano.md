# 火山翻訳

## 簡単な説明

1. 公式サイト:[機械翻訳 - Volcano Engine](https://www.volcengine.com/product/machine-translation)
2. 公式料金説明:[製品課金機械翻訳 - Volcano Engine](https://www.volcengine.com/docs/4640/68515)
3. Volcano翻訳は毎月最初の200万文字まで無料で、超過分については100万文字あたり49ドルが課金されます。詳細は公式料金ドキュメントをご確認ください。

## 申請手順

1. [API アクセスプロセス概要機械翻訳 - Volcano Engine](https://www.volcengine.com/docs/4640/130872)に従って、公式ガイダンスに従ってアカウント登録、実名認証、サービス開始の3つのステップを完了します。コンソールから実行する必要があります。[Volcano Engineコンソール](https://console.volcengine.com/home)
2. キー取得の4番目のステップでは、Volcano Engineは2つのオプションを提供しています:
   1. 作成を続ける(メインアカウントを使用してキーを作成、より便利ですが、このキーはメインアカウントリソースを呼び出すことができ、セキュリティは低い)、「作成を続ける」を選択すると、テーブルに新しいデータが表示され、そこに必要な「Access Key ID」と「Secret Access Key」が含まれています。
   2. 新しいサブユーザーを作成する(より安全なため、サブユーザーを使用してキーを作成することを推奨)、「Access Key ID」と「Secret Access Key」を取得します。このサブアカウントには`TranslateFullAccess`権限が必要です。
3. Immersive Translateの基本設定 - 翻訳サービスを開き、Volcano翻訳オプションを見つけて入力します。
4. 完了です 🎉 疑問がある場合は、[こちら](https://github.com/immersive-translate/immersive-translate/issues/137)でフィードバックをお願いします。
