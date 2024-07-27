# Solicitação de API de Serviços de Tradução

A extensão Immersive Translate oferece suporte a diversos serviços de tradução. Alguns deles exigem que você solicite uma chave de API do serviço correspondente para poder usá-los. Compilei os seguintes tutoriais de solicitação para os serviços disponíveis na web. Caso haja omissões ou informações desatualizadas, fique à vontade para clicar no canto superior direito para editar estas páginas.

Discussões relacionadas à API do Serviço de Tradução podem ser realizadas [aqui](https://github.com/immersive-translate/immersive-translate/issues/137).

## Serviços de Tradução

Esta seção lista serviços de tradução compatíveis com o Immersive Translation. Clique no nome do serviço para acessar seu site oficial. Para saber como configurar cada serviço no Immersive Translation, consulte o guia correspondente.

1. [Claude](https://claude.ai/) | [Guia de Configuração](./services/claude.md) | **API:** `https://api.anthropic.com/v1/messages`
2. [DeepL](https://www.deepl.com/) | [Guia de Configuração](./services/deepL.md) | **API:** `https://api.deepl.com/v2/translate`
3. [DeepSeek](https://deepseek.com/) | [Guia de Configuração](./services/deepseek.md) | **API:** `https://api.deepseek.com/chat/completions`
4. [Gemini](https://aistudio.google.com/app/) | [Guia de Configuração](./services/gemini.md) | **API:** `https://generativelanguage.googleapis.com/v1beta/models/{model}:generateContent?key={key}`
5. [OpenL](https://www.openl.com/) | [Guia de Configuração](./services/openL.md) | **API:** `https://api.openl.club/services/${codename}/translate`
6. [OpenAI](https://platform.openai.com/) | [Guia de Configuração](./services/openai.md) | **API:** `https://openai-api.immersivetranslate.com/v1/chat/completions`
7. [Microsoft Translator](https://portal.azure.com/#home) | [Guia de Configuração](./services/azure.md) | **API:** `https://api.cognitive.microsofttranslator.com/translate?x=2`
8. [Aliyun - Bailian](https://cn.aliyun.com/product/bailian) | [Guia de Configuração](./services/aliyun-bailian.md) | **API:** `https://dashscope.aliyuncs.com/compatible-mode/v1/chat/completions`
9. [Aliyun](https://cn.aliyun.com/product/ai) | [Guia de Configuração](./services/aliyun.md) | **API:** `https://{service}.aliyuncs.com?{paramsString}`
10. [Baidu - Qianfan](https://console.bce.baidu.com/qianfan/overview) | [Guia de Configuração](./services/baidu-qianfan.md) | **API:** `https://aip.baidubce.com/rpc/2.0/ai_custom/v1/wenxinworkshop/chat/{model}?access_token={key}`
11. [Doubao](https://www.volcengine.com/product/doubao) | [Guia de Configuração](./services/doubao.md) | **API:** `https://ark.cn-beijing.volces.com/api/v3/chat/completions`
12. [Tencent Translator](https://fanyi.qq.com/) | [Guia de Configuração](./services/tencent.md) | **API:** `https://transmart.qq.com/api/imt`
13. [Baidu Translate](https://fanyi.baidu.com/) | [Guia de Configuração](./services/baidu.md) | **API:** `https://api.fanyi.baidu.com/api/trans/vip/translate`
14. [Caiyun Xiaoyi](https://fanyi.caiyunapp.com/) | [Guia de Configuração](./services/caiyun.md)| **API:** `https://api.interpreter.caiyunai.com/v1/translator`
15. [Volcano Engine](https://www.volcengine.com/products/machine-translation) | [Guia de Configuração](./services/volcano.md) | **API:** `https://translate.volcengine.com/crx/translate/v1/`
16. [Niu Translation](https://translate.niutrans.com/) | [Guia de Configuração](./services/niu.md) | **API:** `https://api.niutrans.com/NiuTransServer/translation`
17. [Youdao Translator](https://fanyi.youdao.com/) | [Guia de Configuração](./services/youdao.md) | **API:** `https://openapi.youdao.com/api`
18. [Interface de tradução personalizada](https://github.com/immersive-translate/ImmersiveL) | [Guia de Configuração](./services/custom.md)


## Aviso de isenção ou limitação de responsabilidade

Todas as tarifas dos serviços de tradução acima são cobradas pelo provedor do serviço e não têm relação com esta extensão.

Preste atenção à quantidade gratuita de cada provedor de serviço para evitar cobranças inesperadas.

## Uma breve nota sobre a contagem de caracteres

A contagem de caracteres é baseada no comprimento dos caracteres no idioma de origem traduzido. Espaços, pontuação etc. são contados como caracteres. Para a maioria dos serviços, um caractere chinês, letra inglesa, sinal de pontuação, quebra de linha etc. é contado como um caractere. Este tweet de Musk, por exemplo, tem 32 palavras e 196 caracteres.

> To be clear, I'm not someone who thinks lots of government agencies should be abolished (maybe a few), but we should always question our institutions, as this strengthens the bedrock of democracy. institutions, as this strengthens the bedrock of democracy.

Um artigo longo que parece difícil de ler: [Algorithms Unlocked: How They're Shaping Our Everyday Lives | by Two Techie Vibes | Jan, 2023 | Medium](https://twotechievibes.medium.com/algorithms-unlocked-how-they're-shaping-our-everyday-lives-6261fa1dbad), que tem cerca de 10.000 caracteres.

Espero que estes dois exemplos deem a você uma noção da contagem de caracteres.
