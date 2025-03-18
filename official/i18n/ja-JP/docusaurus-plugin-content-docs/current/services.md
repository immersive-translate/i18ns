# Translation Services API Request

Immersive Translate Extension は多くの翻訳サービスをサポートしており、その中には使用する前に対応するサービスの API キーを申請する必要があるものもあります。私はウェブからこれらのサービスの申請チュートリアルをまとめました。もし抜けや更新が遅れている場合は、右上のボタンをクリックしてこれらのページを編集してください。

Translation Service API に関連するディスカッションは[こちら](https://github.com/immersive-translate/immersive-translate/issues/137)で行うことができます。

## Interpretation Service

1. [Deepl](./services/deepL.md)
2. [Caiyun Xiaoyi](./services/caiyun.md)
3. [Tencent Translator](./services/tencent.md)
4. [Volcano Engine](./services/volcano.md)
5. [Baidu Translate](./services/baidu.md)
6. [OpenL](./services/openL.md)
7. [Niu Translation](./services/niu.md)
8. [Youdao Translator](./services/youdao.md)
9. [Youdao Ziyue LLM Translator](./services/youdao-ziyue.md)
10. [Microsoft Translate](./services/azure.md)

## 免責または責任制限に関する声明

上記の翻訳サービスの料金はすべてサービスプロバイダーによって請求され、この拡張機能とは関係ありません。

予期しない請求を避けるために、各サービスプロバイダーの無料利用枠に注意してください。

## 文字数に関する簡単な説明

文字数は、翻訳元言語の文字の長さに基づいて計算されます。スペース、句読点なども文字としてカウントされます。ほとんどのサービスでは、中国語の文字、英語の文字、句読点、改行などが 1 文字としてカウントされます。例えば、Musk のこのツイートには 32 語と 196 文字があります。

> To be clear, I'm not someone who thinks lots of government agencies should be abolished (maybe a few), but we should always question our institutions, as this strengthens the bedrock of democracy. institutions, as this strengthens the bedrock of democracy.

このように読みにくい長い記事：[Algorithms Unlocked: How They're Shaping Our Everyday Lives | by Two Techie Vibes | Jan, 2023 | Medium](https://twotechievibes.medium.com/algorithms-unlocked-how-they're-shaping-our-everyday-lives-6261fa1dbad)は、約 10,000 文字の長さです。

これらの 2 つの例が文字数の感覚を与えることを願っています。