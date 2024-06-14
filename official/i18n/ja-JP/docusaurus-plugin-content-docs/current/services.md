# 翻訳サービス API の申請

沈没型翻訳拡張機能は多くの翻訳サービスをサポートしていますが、一部の翻訳サービスでは、該当するサービスの API キーを申請する必要があります。インターネットから以下のサービスの申請チュートリアルをまとめました。何か漏れがある場合や、最新の情報に更新されていない場合は、右上の角をクリックしてこれらのページを編集してください。

翻訳サービス API に関する議論は[こちら](https://github.com/immersive-translate/immersive-translate/issues/137)で行うことができます。

## 翻訳サービス

- [Claude](./services/claude.md)
- [Deepl](./services/deepL.md)
- [DeepSeek](./services/deepseek.md)
- [Gemini](./services/gemini.md)
- [OpenL](./services/openL.md)
- [Open AI (Azure OpenAI)](./services/openai.md)
- [マイクロソフト Azure 翻訳](./services/azure.md)
- [アリババクラウド バイリアンモデル](./services/aliyun-bailian.md)
- [アリババクラウド 翻訳](./services/aliyun.md)
- [バイドゥ チェンファン モデル](./services/baidu-qianfan.md)
- [バイトダンス ドウバオモデル](./services/doubao.md)
- [バイドゥ 翻訳](./services/baidu.md)
- [彩雲翻訳](./services/caiyun.md)
- [ボルケーノエンジン](./services/volcano.md)
- [テンセント翻訳](./services/tencent.md)
- [小牛翻訳](./services/niu.md)
- [有道翻訳](./services/youdao.md)
- [カスタムAPI翻訳](./services/custom.md)

## 免責事項

上記のすべての翻訳サービスの料金は、完全にサービス提供者が請求するものであり、この拡張機能とは関係ありません。

各サービス提供者の無料枠に注意し、予期せぬ請求を避けてください。

## 文字数についての簡単な説明

文字数は、翻訳の元の言語の文字の長さを基準に計算されます。スペース、句読点なども文字数に含まれます。ほとんどのサービスでは、漢字、英字、句読点、改行記号などがすべて1文字としてカウントされます。例えば、マスクのこのツイートは32語、196文字あります。

> To be clear, I’m not someone who thinks lots of government agencies should be abolished (maybe a few), but we should always question our institutions, as this strengthens the bedrock of democracy.

このように、読み終わるのが難しそうな長文：[Algorithms Unlocked: How They’re Shaping Our Everyday Lives | by Two Techie Vibes | Jan, 2023 | Medium](https://twotechievibes.medium.com/algorithms-unlocked-how-theyre-shaping-our-everyday-lives-6261fa1dbad)は、約1万文字あります。

これら2つの例が、文字数についての感覚的な理解を深めるのに役立つことを願っています。
