---
sidebar_position: 6
---

# Registro de Alterações

## 1.12.3 (2024-12-13)

- Adicionado: **Tradução Contextual com IA** pode melhorar a precisão da tradução de conteúdo profissional. (Disponível apenas para membros Pro) **Opções** -> **Geral** -> **Ativar Tradução Contextual com IA**
- Correção: Alguns bugs no efeito de tradução multilinha no Twitter.
- Correção: Problemas com a tradução de certas fórmulas devido ao texto rico
- Melhoria: Ao traduzir no **x.com**, vídeos com legendas terão automaticamente legendas bilíngues traduzidas.
- Melhoria: Vídeos sem legendas exibirão um ícone de tradução e fornecerão um motivo pelo qual a tradução não é possível.

## 1.11.7 (2024-11-25)

- Adicionado: Bing/Google agora suporta Khmer (Cambojano).
- Adicionado: Permitir que arquivos ePub incompletos continuem traduzindo de onde pararam após reimportação.
- Corrigido: Problema com a tradução de imagens do Twitter no navegador Safari.
- Corrigido: Teclas de atalho se tornando ineficazes ao alternar o recurso "**Tradução ao Passar o Mouse**".
- Melhorado: Aprimorada a exibição de tradução bilíngue multilinha no Twitter e Youtube.
- Melhorado: Tradução de texto rico está desativada por padrão no modo bilíngue para melhorar a qualidade da tradução.
- ~~Melhorado: Adicionada a opção de personalizar "**Ativar Tradução de Barra Lateral e Navegação**" em "**Configurações Avançadas**".~~
- Melhorado: Imagens não são mais traduzidas no modo "**Passar o Mouse - traduzir este parágrafo imediatamente**".

## 1.11.4 (2024-11-16)

- Corrigido: Problema com tradução de fórmulas causado pela "Melhoria de Tradução do Twitter" na versão 1.11.2.

## 1.11.2 (2024-11-13)

- Corrigido: Problema onde o conteúdo desaparece após clicar em "ver mais" no modo somente tradução do Facebook.
- ~~Melhorado: Aprimorada a exibição de traduções bilíngues multilinha no Twitter.~~
- Melhorado: Atualizada a interface do usuário da lista suspensa de serviços de tradução no painel.

## 1.11.1 (2024-11-05)

- Adicionado: **Tradução de Legendas** em reuniões em tempo real agora suporta ativação via "bola flutuante", disponível no Zoom, Google Meet e Microsoft Teams.
- Corrigido: Problemas de sincronização de tempo das legendas no YouTube após assistir anúncios.
- Corrigido: Problemas de exibição do menu de tradução do botão direito no Safari no MacOS 15.
- Corrigido: Problemas com a funcionalidade de desfazer Ctrl+Z no **Input Aprimorado** em certos sites.

## 1.10.6 (2024-10-25)

- Corrigido: Problema com teclas de atalho do **Input Aprimorado** não acionando
- Melhorado: Redução do tamanho do pacote de instalação
- Melhorado: Solução de exibição de legendas da Netflix

## 1.10.5 (2024-10-23)

- Adicionado: Exibir um aviso quando o idioma de origem e o idioma de destino são os mesmos
- Corrigido: Problema de tradução de caracteres de espaço em branco em texto rico [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Melhorado: Aprimoramento de entrada e funcionalidade de mouse hover dentro de iframes incorporados em páginas web

## 1.10.2 (2024-10-11)

- Adicionado: Tradução de imagens (versão Beta)
- Adicionado: Modo de Suporte ao Mouse Forçado (Ative este recurso apenas se a função de hover do mouse não estiver disponível em dispositivos tablet) **Configurações** -> **Configurações Avançadas** -> **Forçar Ativação do Suporte ao Mouse**
- Adicionado: Exibir mensagem de erro quando a tradução de legendas de vídeo falhar
- Corrigido: Problema de tradução de texto rico [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Melhorado: Resolvidos problemas onde o botão de tradução poderia não funcionar durante a tradução de PDF
- Melhorado: Aprimorada a renderização de fórmulas traduzidas
- Melhorado: Lista de seleção de idiomas

## 1.9.8 (2024-09-28)

- Adicionado: Serviço de tradução "Zhipu BigModel"
- Removido: Modelo "SiliconCloud" qwen1.5-7B-chat (devido à descontinuação oficial)
- Corrigido: Resolvido problema de compatibilidade de login com o plugin Safari no macOS 15

## 1.9.7 (2024-09-20)

- Melhorado: Suporte aprimorado para campos de entrada do Baidu, Gmail e outros
- Adicionado: Suporte ao cabeçalho de requisição anthropic-dangerous-direct-browser-access para API Claude Anthropic
- Adicionado: Suporte para download de legendas de vídeos do Hulu, Bloomberg e Domestika
- Melhorado: DeepX agora suporta tradução de texto rico
- Corrigido: Problema de não sincronização de especialistas AI personalizados

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) agora suporta cópia de fórmulas (clique com o botão direito na fórmula para ver o menu de cópia)
- Corrigido: Problema de exibição de legendas bilíngues para múltiplos vídeos na mesma página do Twitter
- Corrigido: Alguns bugs

## 1.9.3 (2024-09-05)

- A opção para exibição de comparação bilíngue/apenas tradução foi movida para as configurações gerais.
- Por padrão, o sistema lembrará o modo alternado ao clicar no ícone no painel para exibição de comparação bilíngue ou apenas tradução. Para alternar temporariamente, clique em "Mais" -> "Alternar para exibição apenas de tradução" no painel.
- Por padrão, a tradução do Chinês Simplificado para Tradicional e vice-versa usará o modo apenas tradução, em vez do modo de comparação bilíngue.
- Corrigido: Alguns bugs.

## 1.9.1 (2024-09-03)

- Suporte para configurar exceções para idiomas e sites no modo de contraste bilíngue ou apenas tradução (configure na página de Configurações -> Configurações Avançadas). Por exemplo: Se seu modo de tradução padrão é contraste bilíngue, mas você não deseja que o Chinês Tradicional também use contraste bilíngue, então você pode adicionar o Chinês Tradicional às línguas de exceção para contraste bilíngue, assim o Chinês Tradicional usará o modo apenas tradução para tradução. Da mesma forma, se seu modo de tradução padrão é apenas tradução, mas você deseja que um determinado idioma ou site use o modo de contraste bilíngue, você também pode adicionar esse idioma ou site às línguas de exceção.
- Corrigido: Problema onde a caixa de entrada na interface de mensagem privada do Tiktok era traduzida incorretamente
- Corrigido: Problema onde quadrinhos no Read Comic Online não podiam ser traduzidos
- Corrigido: Problema onde a 【Configurações Avançadas -> Número mínimo de caracteres necessários para traduzir um parágrafo】 não tinha efeito em alguns casos

## 1.8.4 (2024-08-30)

- O serviço de tradução DeepL agora suporta oficialmente o Chinês Tradicional como idioma de destino (anteriormente, traduzir para o Chinês Tradicional com DeepL envolvia um processo adicional de conversão de terceiros do Chinês Simplificado para Tradicional).
- Otimizado: Desempenho da tradução de texto rico.

## 1.7.9

- Corrigido o problema com traduções de texto rico nos serviços de tradução Google, DeepL, etc. (por exemplo, a página exibe diretamente `<button>`, etc.)
- Corrigido o problema de atalhos em vídeos bilíngues do YouTube que não fechavam

## 1.7.8

- Os serviços de tradução DeepL, Microsoft Translator, Google Translate, OpenAI, Claude e Gemini agora preservam a formatação original do texto traduzido (como links, negrito, etc.).
- Ao selecionar um texto, o menu de contexto agora exibe a opção "Traduzir este texto", que redireciona automaticamente para a página de tradução do Immersive Translate.
- Adicionado serviço de tradução gratuito utilizando modelo de linguagem de grande porte (SiliconCloud), agora disponível para todos os usuários.
- Adicionado serviço de tradução com modelo de linguagem de grande porte da ZeroOneEverything. Os usuários podem se cadastrar na plataforma ZeroOneEverything e inserir sua API Key para utilizar o serviço.
- Adicionado botão para feedback do usuário sobre a qualidade da tradução de quadrinhos. Após a tradução do quadrinho, clique no botão "Feedback", localizado à direita do balão de fala, para enviar sua avaliação.

## 1.7.7

- Adoção do algoritmo de divisão de frases inteligente por IA para legendas em inglês geradas automaticamente no YouTube 【Disponível para Pro】
- Otimização da tradução por clique com o botão direito para "Traduzir para xx idioma de destino"
- Suporte à integração imersiva do [JS SDK](https://immersivetranslate.com/docs/js-sdk/) para sites de terceiros
- Otimização da exibição de legendas do Hulu
- Suporte à tradução de legendas em reuniões da versão web do ZOOM

## 1.7.6

- Suporte à personalização de especialistas em IA, o acesso está na parte inferior da página [Configurações] -> [Especialista em IA].
- Otimização do carregamento de legendas no site TED.
- Português (Brasil) agora é suportado como idioma de plug-in.
- Sites suportados para tradução de quadrinhos:
- [Antbyw](https://www.antbyw.com)
- [Zerobywzz](https://www.zerobywzz.com)
- [动漫之家](https://www.idmzj.com)
- [Jmanga](https://jmanga.org)

## 1.7.5

- Ativada a cópia de legendas do YouTube
- Otimizada a exibição de legendas em alguns sites de vídeo
- Melhorada a velocidade de tradução de mangás

## 1.7.2

- Corrigida a falha na tradução de quadrinhos no navegador Firefox.

## 1.7.1

- Melhorada a velocidade de tradução de quadrinhos
- Adicionado suporte a novos sites na tradução de quadrinhos:
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- Adicionado suporte a novos sites para tradução de quadrinhos:
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- As legendas bilíngues do YouTube agora suportam divisão inteligente de frases (Beta) (Somente ao ativar manualmente a tradução imersiva das legendas do YouTube em [Configurações] - [Legendas de Vídeo], e as legendas originais do vídeo são legendas em inglês geradas automaticamente)
- Adicionado serviço de tradução Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Corrigidos problemas de layout de texto de traduções de quadrinhos para idiomas com alfabeto latino.
- Novos sites suportados para tradução de quadrinhos:
  - [COMIC FUZ](https://comic-fuz.com/)
  - [MangaDex](https://mangadex.org/)
  - [KuaiKanComics](https://www.kuaikanmanhua.com/)
- Corrigido um problema em que os serviços de IA personalizados não conseguiam selecionar especialistas em IA.

## 1.6.4

- Quando especialistas em IA são usados ​​para "Seleção Inteligente", diferentes especialistas em IA podem ser personalizados para diferentes sites. Isso pode ser definido em [Configurações] -> [Especialistas em IA] -> [Inserir qualquer especialista].
- Corrigido o problema em que as legendas não eram exibidas no YouTube no modo "Apenas Tradução".
- Corrigido o problema de legendas bilíngues não funcionarem no Mubi.
- Compatível com PDFs abertos com o plugin Adobe Acrobat.
- Todos os usuários podem [contribuir online](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) para a tradução multilíngue da interface de tradução imersiva.

## 1.6.3

- Novo recurso: Tradução de mangás (Beta). Em sites de mangás compatíveis, um botão de tradução de mangás aparecerá abaixo do botão flutuante de tradução rápida da página da web. Ao clicar nele, a tradução de mangás será ativada. Este recurso está disponível para membros Pro (500 páginas por mês, pacotes adicionais podem ser adquiridos), atualmente suportando os seguintes sites:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Novo recurso: Tradução de mangás (Beta). Em sites de mangás compatíveis, um botão de tradução de mangás aparecerá abaixo do botão flutuante de tradução rápida da página da web. Ao clicar nele, a tradução de mangás será ativada. Este recurso está disponível para membros Pro (500 páginas por mês, pacotes adicionais podem ser adquiridos), atualmente suportando os seguintes sites:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Novo recurso: A tradução de IA suporta o [grande modelo Doubao](https://www.volcengine.com/product/doubao)
- Novo recurso: Suporte para modo de comparação bilíngue com tradução primeiro e texto original em seguida, que pode ser ativado na página de configurações -> configurações avançadas.
- A lista de modelos personalizados de IA suporta a sintaxe `-all`, que pode excluir todos os modelos predefinidos.
- Nas legendas bilíngues de vídeo, quando o idioma de destino for chinês simplificado e o texto original for chinês tradicional, o texto original será automaticamente convertido para chinês simplificado e vice-versa.
- Corrigido o problema em que o atalho de bola flutuante não podia ser traduzido no iOS 18.
- Corrigido o problema em que os prompts personalizados eram ineficazes quando muitos eram usados.

## 1.6.1

- Suporte para as plataformas de grandes modelos Baidu Qianfan, Alibaba Bailian e DeepSeek.
- Corrigido o problema em que a modificação do idioma de destino e outras configurações no painel pop-up eram redefinidas ao clicar no botão flutuante de tradução.

## 1.5.8

- Os especialistas em IA agora suportam o modo "Seleção Inteligente", onde o sistema seleciona automaticamente o especialista em IA mais adequado com base no site atual (por exemplo, especialistas em IA relacionados à tecnologia serão selecionados automaticamente para The Verge e Hacker News, enquanto a otimização de tradução do Twitter será selecionada automaticamente para o Twitter).

## 1.5.7

- Suporte para adicionar serviços de tradução de IA personalizados compatíveis com OpenAI, acessível na parte inferior da página 【Configurações】->【Serviços de Tradução】.
- Corrigido um problema em que as legendas bilíngues não funcionavam na plataforma de vídeo Domestika no Safari.

## 1.5.6

- Otimizado significativamente o desempenho da tradução de páginas da web grandes, criação de ePub e arquivos de legenda.
- Corrigido o bug de sincronização multi-dispositivo no Pro.

## 1.5.4

- Membros Pro agora têm suporte imediato aos serviços de tradução Claude e Gemini (Beta).
- Legendas bilíngues do YouTube agora permitem configurar fonte e espessura da fonte.
- Corrigido problema de quebra de palavras ao ajustar parágrafos longos ([#86](https://github.com/immersive-translate/immersive-translate/issues/86)).
- Corrigido reconhecimento de idiomas japonês e coreano.
- Corrigido problema de páginas do Reddit em dispositivos móveis não serem traduzidas ao rolar.
- Corrigido problema de algumas páginas não serem traduzidas com o DeepL.
- Corrigida dessincronização de tempo em dispositivos múltiplos para usuários Pro.
- Otimizado problema de abrangência das configurações de sincronização em nuvem.
- Otimizadas palavras de prompt para serviços de tradução por IA.

## 1.5.2

- Corrigido problema em que alterações no prompt geral do especialista sobrescreviam o prompt do especialista em IA específico ([#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)).
- O nome do modelo personalizado de IA agora suporta sintaxe avançada, use + para adicionar um modelo, use - para ocultar um modelo e use model_name=display_name para personalizar o nome de exibição do modelo, por exemplo: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super.
- Corrigido o erro retornado por Gemini.
- O botão flutuante agora é ocultado ao imprimir a página.
- Corrigido o problema em que o tamanho da fonte não era dimensionado proporcionalmente quando o YouTube estava em tela cheia ([#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)).

## 1.5.1

- Suporte para serviços de tradução de IA definirem [Especialista em IA] para especificar a estratégia de tradução, atualmente um recurso beta, que pode ser ativado em [Configurações do desenvolvedor](https://dash.immersivetranslate.com/#developer) após ativar o Beta, e o menu [Especialista em IA] pode ser visto após a atualização.
- Os serviços de tradução de IA agora podem personalizar a lista de modelos, como [OpenAI], o sistema possui apenas alguns dos modelos mais utilizados integrados. Ao clicar na lista suspensa de modelos, o último item que você vê é [Definir mais modelos], após a configuração, ele será automaticamente memorizado para a conveniência dos usuários testarem diferentes modelos personalizados.
- Otimizada a inconsistência no layout das traduções em alguns casos.
- Adicionado um botão de reset para o estilo de legenda do Youtube, que pode restaurar rapidamente para o estilo padrão.
- Corrigido o problema em que as legendas em chinês não podiam ser baixadas no Youtube.
- Cópia da interface em chinês tradicional otimizada.

## 1.4.12

- Corrigido problema da caixa de diálogo de mensagem não traduzida ao abrir a página do Reddit.
- Adicionado um recurso temporário para habilitar a edição de tradução na entrada "Mais" do painel.
- Corrigido problema em que o YouTube Shorts sem legendas sempre exibia legendas do vídeo anterior ([#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)).
- Corrigido problema em que as legendas bilíngues do YouTube não podiam ser ajustadas para cima e para baixo em tela cheia ([#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)).
- Suporte a legendas bilíngues em [VK Video](https://vk.com/video).
- Suporte para configurações de ativação independentes para legendas bilíngues de vídeo do YouTube (ativado por padrão para novos usuários).
- Otimizados os prompts de erro para a tradução de legendas bilíngues locais.

## 1.4.11

- Compatível com a tradução da caixa de entrada da página do Bing Copilot.
- O controle de estilo de legenda do YouTube agora suporta estilo de borda.
- Suporte para selecionar o serviço de tradução padrão na página Configurações -> Serviço de Tradução.
- Corrigida a substituição de espaço reservado do OpenAI SystemPrompt.
- Corrigido problema de mesclagem de regras personalizadas do usuário.
- Corrigida exibição anormal de legendas para alguns vídeos da Netflix ([#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)).
- Corrigido o problema em que alterações frequentes na cor da tradução através da paleta de cores eram ineficazes ([#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)).

## 1.4.9

- Os serviços de tradução agora estão organizados de forma distinta em uma guia separada, permitindo uma visão geral abrangente de todos os serviços de tradução disponíveis. Além disso, os usuários têm a flexibilidade de personalizar quais serviços de tradução são exibidos. Por padrão, apenas uma seleção limitada de serviços de tradução é mostrada, mas os usuários podem personalizar suas preferências de exibição na seção [Mais Serviços](https://dash.immersivetranslate.com/#services).
- A página de configurações agora acomoda ajustes aos [estilos de legenda do YouTube](https://dash.immersivetranslate.com/#subtitle).
- Melhorias foram feitas para resolver o problema em que as legendas bilíngues imersivas não eram exibidas quando os usuários definiam o idioma da legenda para chinês no site do YouTube.
- Um novo atalho foi introduzido para tradução temporária chamado Claude, que pode ser configurado na [página Configurações de Atalho](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Otimizar o desempenho de tradução para arquivos grandes em PDF-Pro.
- Aprimorar o desempenho de tradução para páginas de conteúdo longo.
- Implementar suporte à internacionalização (i18n) para navegação de documentos de página.
- O YouTube apresenta um recurso para habilitar temporariamente legendas bilíngues.
- O YouTube suporta o download de legendas bilíngues (somente para membros).
- O celular adiciona controle por gestos, aprimorando a entrada por meio de [configurações de atalho](https://dash.immersivetranslate.com/#shortcuts).
- Suporte à tradução bilíngue para o Google Docs.

## 1.4.7

- Correção de falha na tradução ao trocar as palavras de prompt personalizadas do OpenAI sob o botão de teste.
- Correção de exibição do ícone de atalho de legenda do YouTube.
- Otimização do reconhecimento de idioma da extensão.

## 1.4.6

- Correção de ineficácia de palavras de prompt definidas pelo usuário.
- Adição de opções de 50% e 150% para o tamanho da fonte das legendas do Youtube.

## 1.4.5

- Correção de estilos de legenda do Youtube não salvos.
- Correção de desaparecimento de legendas em tela cheia no Safari iOS.
- Otimização adicional da velocidade de tradução das legendas do Youtube.
- Opção "Mais" no painel agora suporta [entrada de tradução de texto](https://app.immersivetranslate.com/text/).

## 1.4.2

- Suporte para o serviço de tradução Claude.
- Otimização de palavras de prompt múltiplas do OpenAI, suportando formato YAML.
- Otimização significativa da velocidade de tradução de legendas do Youtube, com suporte para alternar entre ordem de chinês e inglês, personalizar cor e tamanho da fonte, etc.
- Plataforma de legendas de vídeo suporta [University of Southampton](https://southampton.cloud.panopto.eu).
- Legendas bilíngues do Udemy compatíveis com exibição em dispositivos móveis.
- Serviço de tradução Gemini oculto por padrão, pode ser ativado nas configurações do desenvolvedor para mostrar a versão beta.

## 1.3.4

- Suporte para o serviço de tradução gratuito Yandex.
- Otimização de palavras de prompt do Gemini.
- Tradução de legendas de vídeo com suporte para configuração de exibição bilíngue/original e tradução.
- Suporte para espaço entre chinês e inglês nos resultados de tradução do OpenAI.
- Alteração do painel para exibir apenas o botão de tradução modificado para ter efeito apenas na página atual.

## 1.3.3

- Otimização da exibição de legendas de vídeo CC do Twitter.
- Serviço DeepL com suporte adicionado para árabe.
- Serviço Colorful Clouds agora suporta coreano, espanhol, francês e russo.
- Serviço OpenAI com suporte adicionado para dialeto do nordeste da China.
- O painel de detecção automática agora exibe o idioma original.
- Ajuste na descrição do atalho para o painel móvel.

## 1.3.2

- Correção do problema de fechamento do painel de controle em dispositivos móveis.

## 1.3.1

- Suporte para tradução de legendas de vídeo na plataforma [DeepLearning.ai](https://learn.deeplearning.ai).
- Suporte para tradução de páginas da web e legendas de vídeo em idiomas como árabe e hebraico, resolvendo problemas de exibição RTL (da direita para a esquerda).
- Correção da tradução do Gemini para hebraico.
- Correção da exibição de legendas em chinês tradicional no YouTube.
- Correção da exibição de legendas do Twitter no Safari.
- Correção do atalho para tradução imediata para o final da página.

## 1.2.4

- Correção do problema de substituição incorreta de espaços reservados na criação de ePub.
- Suporte à tradução de legendas de vídeo na plataforma [Unreal Sensei](https://www.unrealsenseiacademy.com/).

## 1.2.3

- Otimização do controle de frequência de solicitações de serviço de tradução.
- Detecção automática de serviço de tradução disponível em caso de instabilidade nas solicitações do serviço de tradução da Microsoft originadas da China.
- Otimização da mensagem de erro para erros de rede.
- Correção do problema de configuração de cor de texto que não suportava visualização RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435).
- Correção do problema de atualização do plugin do Safari que sempre exibia a página de sucesso da instalação.
- Microsoft adicionou suporte para vietnamita.
- Correção do problema de legendas traduzidas no site edx que não eram exibidas.

## 1.2.2

- Tradução de legendas de vídeo com suporte para [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/) e [movie-web](https://movie-web.app/). Também suporta a tradução de alguns vídeos com legendas CC no Twitter.
- Otimizados pop-ups de erro, pop-ups de erro de problema de rede detectam automaticamente serviços de tradução gratuitos válidos.
- Corrigido suporte do aplicativo Immersive iOS para reprodução em tela cheia no YouTube.
- Corrigido problema de tradução de parágrafo com Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Tradução de legendas de vídeo com suporte para [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/) e [Three.js Journey](https://threejs-journey.com/).
- Corrigido um problema em que alguns usuários Pro não podiam modificar as configurações no navegador Chrome.
- Suporte para exibição de legendas bilíngues no modo de tela cheia do YouTube em iOS.

## 1.2.0

- Suporte para tradução de legendas de vídeo nas plataformas [LinkedIn](https://www.linkedin.com/) e [Viu](https://www.viu.com/).
- Adicionado acesso rápido a mais legendas de vídeo para plataformas adicionais.
- Suporte para definir sites/idiomas específicos para exibir apenas o texto traduzido.
- Corrigido um problema em que a página de configurações exibia o carregamento continuamente em alguns casos no Safari.
- Suporte para tradução de nós de tag de entrada.
- Otimizada a interface do usuário do pop-up de erro.

## 1.1.9

- Tradução de legendas com suporte para YouTube Live e a plataforma [Mubi](https://mubi.com/).
- Otimização: página de configurações, interface de interação da lista de URLs (para evitar ambiguidade, as caixas de seleção não são exibidas por padrão).
- Suporte para definir a fonte de tradução no modo somente tradução.
- Adicionado acesso rápido para ativar legendas de vídeo em Netflix, Ted, Bloomberg, Udemy e Coursera.
- Corrigido: alguns estilos traduzidos (como sublinhados) não eram eficazes no Safari.
- Corrigido: durante a tradução da página, o problema em que passar o mouse não acionava a retradução.

## 1.1.8

- Adicionada uma opção para o serviço de tradução filho seguir o serviço de tradução principal.
- Suporte para legendas bilíngues em [Amazon Prime Video](https://www.primevideo.com).
- Otimização adicional da função de tradução de PDF incorporado no Sci-Hub.
- Corrigido um problema com PDFs online que não abriam corretamente.
- Corrigido o problema com a reprodução contínua de legendas bilíngues na Netflix.

## 1.1.7

- Agora você pode especificar uma fonte para a tradução na página de configurações -> [Configurações Básicas] -> [Estilo de Tradução].
- Adicionado uma configuração de atalho para [Traduzir Parágrafo Especificado] no painel flutuante em dispositivos móveis.
- Otimizada a sensibilidade da detecção de foco do mouse sobre Ctrl para evitar confundir `Ctrl+C` com `Ctrl`.
- Adicionado suporte para uma nova configuração de atalho que permite alternar rapidamente se as legendas de vídeo usam as legendas de tradução automática incorporadas.
- No site do Sci-Hub, ao clicar no botão flutuante, os PDFs incorporados na página da web serão traduzidos.

## 1.1.6

- **Tradução de Parágrafos Específicos no Celular:** A versão móvel agora suporta a tradução de parágrafos específicos e adicionou uma variedade de operações de atalho, incluindo deslizar para a esquerda, deslizar para a direita, tocar duas vezes, tocar três vezes e gestos de toque com vários dedos. Estes não estão ativados por padrão e exigem que o usuário selecione ativamente o gesto de disparo na página de configurações em 【Mouse Hover】.
- **Atualização da Versão Padrão do Gemini:** A versão padrão agora é `v1beta`.
- **Correção da Tradução do Chinês Clássico:** Corrigida a funcionalidade de tradução do chinês clássico da Microsoft e OpenAI.
- **Otimização da Tradução do Japonês:** Otimizada a tradução do japonês do OpenAI para melhorar a precisão e fluência.
- **Experiência de Tradução Imersiva:** Para melhor se adaptar aos hábitos do usuário, o atalho para legendas bilíngues no modo de tela cheia na plataforma YouTube foi movido para o lado esquerdo.

## 1.1.5

- Corrigido o problema em que o menu suspenso no modo escuro do Windows não tinha cor.
- Corrigido o problema de alinhamento em que a opção "Mais" não estava alinhada à esquerda no Windows.

## 1.1.4

- **Atualização da Interface do Painel Pop-up:** O novo design visa melhorar a usabilidade e a compreensão. Esta atualização inclui:

  - **Novos recursos no menu principal:**
    - **Alternância de modo bilíngue/somente tradução:** Agora você pode alternar entre o "Modo de Tradução Bilíngue" e o "Modo Somente Tradução" diretamente no menu principal, localizado à esquerda do botão de tradução.
    - **Entrada de tradução de documentos:** A entrada para traduzir "arquivos PDF/ePub/legendas" foi movida para o menu principal para acesso rápido.
    - **Configurações de tradução de vídeo:** A entrada para as configurações de "Tradução de Vídeo" também foi colocada no menu principal para ajustes rápidos.
    - **Nova entrada para documentação de uso:** Fornece guias de operação detalhados e documentos de ajuda.

- **Entrada de tradução de documentos integrada:** Agora, você pode traduzir arquivos PDF, ePub e legendas por meio de uma entrada de upload unificada. Basta clicar no botão 【PDF/ePub】 no painel pop-up, sem necessidade de selecionar 【Mais】.

- **Adicionado suporte para 5 sites de vídeo:**
  - Suporte para legendas de podcasts no Youtube Music.
  - Adicionado suporte para o site iview.abc.net.au.
  - Adicionado suporte para o site www.nma.art.
  - Adicionado suporte para o site creativecloud.adobe.com.
  - Adicionado suporte para o site [www.masterclass.com](https://www.masterclass.com).

## 1.1.3

- Corrigido problema de exibição anormal do plugin móvel ao abrir páginas PDF.
- Otimizado o efeito de tradução em conversas GPT.
- Adicionado suporte à tradução de domínio para o Baidu Translate.
- Adicionado um modo de tradução-somente na página de configurações.
- Adicionada função de lembrete ao alternar modos de tradução com atalhos.
- Corrigido o problema em que a tradução de campos de entrada contendo URLs traduzia apenas partes do conteúdo.

## 1.1.2

- Correção: o problema em que a troca de serviços de tradução não surtia efeito quando a página ainda não havia sido traduzida.
- Otimização: no processo de tradução de Epub e PDF, se algum conteúdo não for traduzido, agora é possível mudar para outro serviço de tradução no painel sem reiniciar todo o processo de tradução (a lógica anterior era usar imediatamente um novo serviço de tradução para retraduzir todo o livro). Isso significa que, no meio da tradução, você pode mudar para um serviço de tradução diferente e clicar em [Tentar Novamente Todos os Parágrafos Falhados], após o que o sistema continuará a tradução usando o novo serviço.
- Otimização: ajustado o tamanho da fonte dos prompts de erro de tradução para melhorar a legibilidade.

## 1.1.1

- Corrigido o problema do atalho de legendas bilíngues do YouTube ter um texto em inglês muito longo.

## 1.1.0

### Novos Recursos

- **Configurações de Teclas de Atalho:** Adicionado um novo menu de nível superior "Atalhos" e as seguintes funções de teclas de atalho personalizáveis:

  - Designar uma combinação de teclas para traduzir o conteúdo da caixa de entrada atual, complementando o método anterior de pressionar rapidamente a barra de espaço três vezes.
  - Designar uma combinação de teclas para ativar temporariamente a "tradução direta ao passar o mouse" na página. Pressioná-lo novamente cancelará esta função.
  - Adicionadas teclas de atalho dedicadas para 6 serviços de tradução (como DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) para facilitar a alternância temporária entre os serviços de tradução.

- **Atualização da Interface da Página de Configurações do Plugin:**

  - Em "Configurações Avançadas", uma nova opção foi adicionada para permitir que os usuários especifiquem certas palavras (por exemplo, "LLM") para serem excluídas da tradução.
  - Em "Configurações Avançadas", uma nova opção foi adicionada para configurar o número mínimo de caracteres necessários para traduzir um parágrafo. O padrão é 4 caracteres, mas pode ser definido para um valor mais alto (por exemplo, 20), para que apenas parágrafos mais longos sejam traduzidos.
  - Adicionado um tutorial para iniciantes, cobrindo as configurações do botão flutuante, configurações de legendas de vídeo e configurações de foco do mouse.

- **Legendas Bilíngues do YouTube:** Adicionado um acesso rápido na janela de reprodução de vídeo do YouTube para ativar ou ocultar legendas bilíngues (este recurso pode ser desativado).

- **Suporte a Idiomas do Deepl:** Adicionado suporte para português (Brasil).

- **Novo Guia do Usuário:** Quando novos usuários abrem uma página em um idioma não alvo pela primeira vez, um balão de guia de ajuda do botão flutuante é exibido.

### Otimização e Correções

- **Otimização da Interface do Usuário:** Redesenhada a interface do usuário para prompts de erro de tradução de página para torná-los mais fáceis de entender. Quando houver muitos erros, um pop-up alertará ativamente o usuário.

- **Correções de Bugs:**

  - Corrigido o problema em que a tradução por mouseover falhava quando a página perdia o foco.
  - Corrigido o problema em que menos de 3 caracteres no recurso de aprimoramento da caixa de entrada não eram traduzidos.
  - Corrigido o problema em que alguns diretórios não eram traduzidos durante a produção de Epubs bilíngues.

- **Remoção de Recurso:** Removido o recurso de aprimoramento de informações bilíngues (exibindo resultados de pesquisa em inglês nas páginas de pesquisa do Google simultaneamente).

### Outras Atualizações

- **Atualização da Configuração do OpenAI:** Agora suporta a configuração do número de configurações por segundo em decimais, como 0,5, significando 1 solicitação a cada 2 segundos.

## 0.12.14

- Correção: O problema de reconhecimento do idioma de destino padrão em algumas máquinas após a primeira instalação.
- Otimização: A ordem padrão dos títulos das páginas da web foi alterada para [Chinês - Inglês].

## 0.12.13

- Corrigido: Problema com a junção de parágrafos longos da OpenAI em alguns casos. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Otimizado: Ao usar o mouse, o problema em que a perda de foco na página e a reativação se tornam ineficazes.
- Corrigido: O problema em que o cache ainda existe após modificar o prompt/modelo na OpenAI.

## 0.12.12

- Atualizado: Otimizado o painel pop-up, removendo algumas opções para o site atual.
- Otimizado: Melhorado o processo de mesclagem de legendas manuais.
- Otimizado: Definir automaticamente o idioma de destino com base no idioma do navegador.
- Adicionado: Suporte a legendas bilíngues para a plataforma de aprendizado [ArtStation](https://www.artstation.com/learning) e [ZDF](https://www.zdf.de/).
- Corrigido: Resolvido o problema em que os títulos na página de lista do jstor não eram traduzidos [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Corrigido: Corrigido o problema em que apenas parte do conteúdo desaparecia no Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Adicionado suporte a legendas bilíngues para as plataformas [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/) e [Domestika](https://www.domestika.org).

## 0.12.10

- Corrigido o problema de autorização do domínio Gemini no script Tampermonkey.
- Suporte à tradução de legendas em tempo real para o Twitter Space.
- Para versões mais antigas do script Tampermonkey, um prompt de atualização foi adicionado à página de configurações.

## 0.12.9

- Adicionado suporte para tradução Gemini.
- Corrigido o problema em que as traduções não respondiam a tempo quando a página era rolada para a posição do meio em alguns casos.
- Corrigido o bug em que a alternância de legendas em alguns sites de vídeo fazia com que a tradução fosse exibida repetidamente.
- Corrigido o problema em que o mouse pairava para continuar traduzindo sem manter pressionada a tecla de atalho em alguns casos.
- No macOS, o nome de exibição do atalho do painel foi otimizado.

## 0.12.8

- Reparado: as legendas originais do vídeo não eram exibidas quando "O site atual está configurado para nunca traduzir".
- Reparado: o conflito com alguns plug-ins que causavam o retorno infinito da página.
- Reparado: a não tradução de alguns parágrafos após ativar as quebras de linha de parágrafos longos.
- Corrigido: [Ao ativar temporariamente a tradução da página da web por um longo tempo, clicar no painel [Sempre traduzir este site] não cancela a tradução sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Legendas bilíngues adicionadas para suportar as plataformas [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://learn.codewithchris.com/enrollments), e [Skillshare](https://www.skillshare.com/).
- O botão flutuante agora está oculta por padrão quando o vídeo está em tela cheia.
- Corrigido o problema de clique instável do painel de ação do botão flutuante na página do Firefox.
- Suporte para colaboração no site pubmed.ncbi.nlm.nih.gov e no plug-in scholarscope.
- Corrigido o problema de tremulação da página de tradução da caixa de entrada do Reddit.

## 0.12.6

- Corrigido o problema de a tradução do YouTube/Web of Science etc. não ser sensível ao alternar as guias.
- O botão flutuante no celular agora suporta operação de pressionar longamente, pressionar rapidamente para traduzir e pressionar longamente para abrir o painel.
- A tradução de e-books bilíngues agora também traduzirá o índice.
- O recurso de Aprimoramento de Pesquisa (algumas páginas da Pesquisa Google exibem resultados de pesquisa bilíngues) agora não está ativado por padrão e será removido na próxima versão.

## 0.12.5

- Corrigido problema em que a criação de eBooks a partir de cliques em traduções no painel não funcionava no Epub.

## 0.12.4

- Ao ativar as legendas bilíngues no painel, a página será atualizada automaticamente (para exibir as legendas bilíngues com mais precisão), e alguns sites ainda exigem que os usuários cliquem manualmente no botão "CC" no site para ativar as legendas.
- Otimizada a detecção de idioma no Grease Monkey e Safari.
- Fornece acesso rápido a versões bilíngues de todos os artigos no site de artigos [Arxiv](https://arxiv.org/abs/1910.06709).
- Corrigido problema de fixação do botão flutuante à esquerda [#1168](https://github.com/immersive-translate/immersive-translate/issues/1168).
- Corrigido problema de exibição do Modo de Aprendizagem [#1180](https://github.com/immersive-translate/immersive-translate/issues/1180).
- Corrigido problema em que a ativação temporária da tradução da web por um longo período não cancelava a opção "Sempre Traduzir" [#1172](https://github.com/immersive-translate/immersive-translate/issues/1172).
- Otimizados problemas de inicialização de arquivos PDF.

## 0.12.3

- Corrigido o problema em que o recurso [desativar permanentemente legendas de vídeo] não estava funcionando [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175).

## 0.12.2

- Suporte a legendas bilíngues fornecido para mais plataformas de vídeo, agora suportadas: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Observação: devido a limitações técnicas, alguns sites precisam ser atualizados após a primeira ativação das legendas bilíngues ou é necessário aguardar a conclusão da tradução para que as legendas sejam exibidas).
- Tamanho do arquivo zip do plugin significativamente otimizado, reduzido pela metade em comparação com o original, download e atualização mais rápidos.
- Corrigido problema de download de PDF estendido.
- Adicionado um portal de tradução rápida de PDF no lado direito do site de artigos do [Arxiv](https://arxiv.org/abs/1910.06709), que leva a uma página HTML limpa (suportado apenas por alguns artigos, pois requer que os autores originais enviem o código-fonte, portanto, cerca de 50% dos artigos mostrarão este portal).
- Páginas PDF online sem extensão .pdf agora podem ir diretamente para a página de tradução de PDF clicando no botão flutuante na página.
- Corrigidos alguns problemas de aprimoramento da caixa de entrada no Safari.
- Otimizada a detecção de idioma no Grease Monkey e no Safari.

## 0.11.6

- Adicionados 11 novos idiomas de interface para o plugin e o site oficial, agora os idiomas de interface suportados chegam a 14, incluindo Chinês Simplificado, Chinês Tradicional, Inglês, Japonês, Coreano, Russo, Espanhol, Português, Hindi, Italiano, Alemão, Francês, Árabe e Persa.
- Modificado o compartilhamento bilíngue (modo de atualização) adicionado na última versão para compartilhamento de instantâneos de página bilíngue, para que o conteúdo compartilhado seja mais original, bem como tenha maior adaptabilidade.
- Corrigido emoji no final da caixa de entrada do Twitter que não podia ser traduzido.
- Corrigida a situação em que o conteúdo de plug-ins de terceiros era traduzido em alguns cenários.
- Reparado o botão flutuante em PDF online com clique que não respondia.

## 0.11.5

- Agora você pode gerar um link público para a página bilíngue traduzida para o Immersive Translate.
- [Clique](/docs/share/) no ícone de compartilhamento do Immersive Translate para gerá-lo em um clique!
- Resolvido o problema de algumas plataformas não reconhecerem se o mouse era suportado ou não.
- Existem alguns navegadores de desktop que suportam tanto touchscreen quanto mouse, e o Immersive Translate tecnicamente não consegue detectar se tais plataformas suportam mouse, então adicionamos a opção [Forçar Suporte a Mouse] na configuração de [Passar o Mouse].

## 0.11.2-0.11.4

- Otimização da experiência, correção de alguns bugs.

## 0.11.1

- O modelo padrão para traduções OpenAI é: GPT3.5-turbo-1106.
- Otimizado o Prompt Chinês para OpenAI, agora menos propenso a alucinações!
- Reduzido o comprimento dos prompts da OpenAI de 90 para 40, economizando ainda mais tráfego.

## 0.11.0

- Corrigidos cliques instáveis no botão flutuante da página.
- Corrigidos problemas de tradução do Azure.

## 0.10.9

- Corrigidos alguns problemas menores.

## 0.10.8

- Suporte para configuração de botões de tradução rápida no botão flutuante (suporte para PC/celular).
- Otimização do julgamento de idioma do Grease Monkey.
- Correção da tradução de arquivos txt.

## 0.10.7

- Suporte para pressionar Ctrl novamente ao passar o mouse para mostrar o texto original.
- Ignorar idioma "Nunca traduzir" ao passar o mouse.
- Otimização de legendas bilíngues do Youtube.

## 0.10.6

- Suporte a tradução apenas de legendas do Youtube.
- Adicionado alerta de atualização de versão baixa do Grease Monkey.
- Corrigido o problema de arquivos txt locais não poderem ser traduzidos.

## 0.10.5

- Corrigido problema ocasional de retorno à página inicial do Youtube.

## 0.10.4

- Corrigido conflito de legendas do Youtube com o plugin de legendas duplas (a tradução de legendas do Youtube pelo Immersive Translate não é ativada quando o plugin de legendas duplas do Youtube é detectado para evitar conflitos).
- Adicionada a opção [Desativar Permanentemente a Função de Legendas de Vídeo], caso haja outros problemas de conflito e você não queira ativar a função de legendas bilíngues com o Immersive Translate.
- Otimizadas quebras de legendas.

## 0.10.3

- Corrigido problema de tradução com chave de autenticação DeppL personalizada.

## 0.10.3

- Suporte perfeito para vídeos do Youtube com legendas bilíngues 🎉.
- Para páginas de artigos, o corpo do texto agora será traduzido primeiro, antes do restante do conteúdo da barra lateral.
- Otimizada a contextualização da tradução do DeepL.
- Otimizada a tradução de arquivos de legendas do OpenAI para contextualização.

## 0.10.1

- Aumentada a prioridade da tradução do corpo para otimizar a experiência de tradução.
- Corrigido problema de texto não traduzido ao clicar em "mais" no Instagram.

## 0.9.8

- Otimização da experiência, correção de alguns bugs.

## 0.9.7

- Corrigida a tradução automática quando o Readwise está realçado.

## 0.9.6

- Corrigida a limpeza do cache ao desconectar o usuário.

## 0.9.5

- Correções de bugs em eBooks online.

## 0.9.4

- Otimização da detecção de aprimoramento de entrada para reduzir toques falsos.
- Tradução de eBooks e legendas online.

## 0.9.3

- Tradução da caixa de entrada: exibe um lembrete pop-up quando usada pela primeira vez, e o usuário pode optar por desativá-la desta vez ou permanentemente para evitar toques acidentais.
- Otimização da velocidade de exportação da tradução do PDF: se você optar por exportar apenas a tradução, poderá chamar diretamente a visualização do PDF do sistema para exportar, mais rápido.
- Deeplx suporta vários URLs, basta separá-los com ponto.

## 0.9.2

- A ferramenta de tradução de PDF foi migrada para a versão online: [https://app.immersivetranslate.com/pdf/](https://app.immersivetranslate.com/pdf/), para que o Grease Monkey e o Safari possam usar a tradução de PDF, e os problemas possam ser melhor iterados sem a necessidade de lançar uma versão para resolver o problema.
- Otimização da interface do usuário do POPUP, o painel está mais bonito!

## 0.9.1

- Corrigidos problemas de nome de arquivo na criação de eBooks Epub.

## 0.8.8

- Suporte a ajuste de espaçamento entre linhas e palavras em PDF para re-reconhecer parágrafos.
- Corrigido problema de rolagem automática em dispositivos móveis na leitura online de epub.

## 0.8.7

- Suporte para download apenas da tradução em PDF.
- Corrigido problema de login do Google no Safari.

## 0.8.2 - 0.8.6

- Permite definir o intervalo entre os acionamentos do combo de aprimoramento de entrada.
- Corrigidos alguns bugs.

## 0.8.1

- Otimização da detecção de idioma.
- Recursos Beta: API personalizada (Beta ativado nas configurações do desenvolvedor).
- Suporte para tradução do AliCloud.
- Corrigidos alguns bugs.

## 0.8.0

- Sistemas de usuário suportados.
- Suporte a [Ativar Associação Pro](/pricing), que permite aos usuários desfrutar de traduções Deepl e OpenAI e sincronização de configurações em nuvem.
- O serviço de tradução por mouse hover pode ser configurado individualmente.
- O serviço de tradução da caixa de entrada pode ser configurado separadamente.
- Otimização da tradução de PDF.
- Corrigidos alguns bugs.

## 0.7.16

- Tradução de PDF com novas opções para controle rápido do estilo de tradução (arquivos PDF são muito estranhos e ativar essas opções pode ser útil para alguns arquivos PDF com formatação confusa).
- Versões para iOS e macOS estão de volta à Apple Store Country Store.

## 0.7.15

- Fomos notificados pela Apple que as Traduções OpenAI foram temporariamente removidas do iOS e macOS, e estamos tentando relançá-las na China.

## 0.7.11- 0.7.14

- Correção: problema de tradução de todas as regiões do Gmail.
- Desativada temporariamente a função de exportação de PDF do Safari devido à restrição do Safari em downloads de plug-ins (bug).
- Corrigidos alguns outros problemas.

## 0.7.10

- Atualização da interface do usuário do painel de ícones do navegador pop-up, um pouco mais de design.
- Corrige o problema de algumas passagens em japonês não serem traduzidas.

## 0.7.9

- O PDF finalmente suporta a exportação de versões bilíngues! Você pode clicar no botão [Salvar] para exportar o arquivo PDF bilíngue traduzido.
- Regras personalizadas agora suportam a mesclagem com as regras internas padrão, por exemplo: `{"id": "youtube", "selectors.add":["#test"]}` significa adicionar um `#test` aos seletores existentes, `selectors` significa substituir o padrão, `selectors.remove` significa excluir um dos seletores padrão.
- Ícone do Safari atualizado, um pouco maior.
- Outras correções de bugs.

## 0.7.8

- Correções de bugs.

## 0.7.7

- Adaptado ao estilo de sistema do Safari, o ícone da extensão do Safari foi alterado para contorno transparente.
- Adicionada alteração de status do ícone do navegador: quando uma página da web for traduzida, um ✅ será adicionado automaticamente no canto inferior direito do ícone do navegador.
- Ativada automaticamente a tradução de sites em inglês usados com frequência para novos usuários.
- Corrigidos problemas de tradução com [https://claude.ai/](https://claude.ai/).

## 0.7.6

- O aprimoramento da caixa de entrada suporta desfazer os resultados da tradução com ctrl+z.
- Suporte à tradução no modo de leitura de documentos do Flying Book.
- Adaptação [https://pi.ai/talk](https://pi.ai/talk).

## 0.7.5

- Corrigido o ícone do Grease Monkey que não era exibido.
- Corrigidos vários problemas.

## 0.7.4

- Corrigidos vários problemas.
- A página de configuração suporta a exclusão em lote de URLs selecionados.
- Suporta ativar/desativar a tradução de legendas do Youtube para evitar conflitos com outros plugins relacionados.
- O Arigato Translator suporta a configuração de campos e ID de terminologia.

## 0.7.2

- Aprimoramento da caixa de entrada: permite omitir o prefixo // e acionar a tradução de toda a caixa de entrada com 3 espaços, ou você pode desativar essa opção na página de configurações.

## 0.7.1

- Suporte ao aprimoramento da pesquisa: quando ativado, ao pesquisar no Google/Google Notícias em chinês, a coluna da direita mostrará automaticamente os resultados da pesquisa de palavras-chave em inglês correspondentes, ativado por padrão.
- Motivo: Descobrimos que na pesquisa do Google, os resultados da pesquisa para palavras-chave em chinês e inglês podem ser muito diferentes. Com o Aprimoramento da Pesquisa do Immersive Translate ativado, pesquisamos automaticamente as mesmas palavras-chave em inglês para você e as exibimos no lado direito. Você pode optar por desativá-lo se não precisar do recurso.
- Não suportado pelo Safari devido a limitações de API.

## 0.6.20

- Modificação das configurações padrão: Devido a um grande número de comentários de usuários que não usam a ferramenta de tradução após a instalação, a expectativa deles é que a ferramenta traduza automaticamente páginas da web em inglês após a instalação. Portanto, a partir desta versão, para usuários chineses, a opção de traduzir páginas em inglês por padrão foi ativada (se o usuário tiver uma configuração anterior do idioma que sempre será traduzido, ela será respeitada, e a alteração apenas modifica as configurações iniciais da extensão), e precisa ser cancelada, o que pode ser feito facilmente no [Painel pop-up ou página de configurações](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91).

## 0.6.19

- Correção de bugs em PDF.
- Correção de bug no Web of Science.
- Adaptação para feeder.com.
- Correção de epub que não traduzia alguns livros.

## 0.6.18

- Correção do problema de estouro de largura do pop-up no Safari.
- Otimização do processo de compilação.

## 0.6.17

- Otimização de alertas de erro.
- Otimização da seleção do idioma de destino, agora ele mostrará apenas os idiomas suportados pelo serviço de tradução correspondente.
- Otimização da tradução de PDF.
- Adaptado para o site Good Reads, Amazon e South China Morning Post.

## 0.6.16

- Adicionada exibição de página sem permissão em PDF.
- Reparada a exibição de parágrafos da lista de texto em PDF.
- Aumentada a escala de fontes pequenas em PDF no Chrome e Safari.

## 0.6.15

- Reparado o problema de, ao abrir arquivos PDF, o painel de extensão indicar que não há permissões.
- Corrigido o problema de o aprimoramento da caixa de entrada não ser ativado quando o site está configurado para nunca traduzir.

## 0.6.14

- Otimização da tradução de PDF, a área de tradução agora pode ser editada/arrastada/excluída.
- Arraste no canto superior esquerdo, exclua no canto superior direito, redimensione no canto inferior direito.
- Alinhamento à esquerda da caixa suspensa do Windows.
- Suporte a chinês tradicional e chinês simplificado.

## 0.6.13

- Corrigido o problema de tradução repetida ao passar o mouse.
- A tradução de PDF suporta arrastar para alterar o tamanho e editar o conteúdo da tradução.

## 0.6.12

- Corrigido o problema de imagens de tradução Epub ficarem menores em alguns navegadores.
- Otimizada a tradução da caixa de entrada, agora funciona sem problemas no Bard!

## 0.6.10

- Modelo padrão do OpenAI alterado para a versão 0613.
- Corrigidos alguns estilos de caixa de entrada.
- Mais inteligente para determinar se é uma área de navegação e, se for, nenhuma tradução é realizada.
- Corrigidos possíveis ataques de injeção XSS.

## 0.6.8

- O painel de extensão agora pode indicar páginas não suportadas (por exemplo, páginas sem permissões e páginas não HTML).
- Aprimoramento da caixa de entrada para mostrar o status de carregamento na tradução.
- Atualizadas as cores de carregamento padrão nas traduções.
- Quando a caixa de entrada está configurada sem prefixo, ela suporta a tradução `ja Hello` para japonês e `English Hello` para inglês.

## 0.6.6

- Correção: algumas áreas não traduziam (Quora).

## 0.6.5

- Otimização do Google Bard.
- A tradução da caixa de entrada suporta a tradução direta de toda a caixa de texto sem prefixos.
- Otimizado o problema de traduções do OpenAI adicionarem pontos sem pensar (se nenhum ponto for detectado no texto original, se o OpenAI retornar um ponto, remova-o).
- Problemas com arquivos de legendas do Safari não sendo reconhecidos.

## 0.6.3

O idioma padrão para tradução da caixa de entrada agora pode omitir o espaço, ou seja, //Hello World também pode ser traduzido.

## 0.6.2

O aprimoramento mais emocionante da caixa de entrada está aqui:

- Digite: // Hello World na caixa de entrada em qualquer página da web e clique três vezes na barra de espaço para traduzir o parágrafo para o inglês.
- Você também pode especificar a tradução para um determinado idioma: /ja Hello World, em seguida, clique três vezes na barra de espaço para traduzir o parágrafo para o japonês.

[Clique aqui para uma rápida introdução de 30 segundos](/docs/input/)

## 0.6.0

- Primeiro lançamento em junho, migrado do subdomínio pessoal anterior [https://immersive-translate.owenyoung.com](https://immersive-translate.owenyoung.com) para o novo domínio [https://immersivetranslate.com/](https://immersivetranslate.com/).
- A funcionalidade permanece praticamente inalterada (novos recursos estarão disponíveis na próxima versão!).

## 0.5.17

- Corrigido o problema de eBooks bilíngues não terem imagens após a exportação.

## 0.5.16

- Corrigido problema de tradução do OpenAI em chinês tradicional.

## 0.5.15

- Otimização: o número mínimo de caracteres em um parágrafo que aciona a tradução foi modificado para um mínimo de 4 caracteres para reduzir a confusão, enquanto usa outros recursos para evitar traduzir as áreas de navegação e final do site.
- Correção: detalhes do Github não traduzidos após a expansão.

## 0.5.14

- Corrigido o problema de imagens em algumas páginas da web ficarem maiores após a cópia.
- Correção: seção de comentários do Medium não traduzida.
- Corrigido o problema de imagens em algumas páginas serem copiadas incorretamente.

## 0.5.12

- Recurso: O estilo de tradução de linha dividida adiciona uma linha vertical para traduções de linha única.
- Correção: Casos muito raros de divisão de parágrafo.
- Uma ótima página de orientação de configuração inicial para novos usuários do iOS.

## 0.5.11

- Suporte à tradução de legendas para exportar apenas traduções.
- Correção: Alguns elementos não eram reconhecidos ao passar o mouse.
- Correção: Quebras de linha parciais de tweets não eram reconhecidas.
- Correção: O estilo de criação de eBooks não estava funcionando.

## 0.5.10

- Correção: Quebras de linha de tweets não eram reconhecidas.
- Correção: A página de detalhes do Reddit retornava alguns parágrafos que não podiam ser traduzidos.
- Corrigido um problema em que algumas tags de código não eram reconhecidas corretamente.

## 0.5.9

- Corrige quebras de parágrafo em alguns casos.
- Correção: A alternância do Tampermonkey mostra apenas traduções.
- Correção: Problema de estilo de leitura online de eBook não funcionando.

## 0.5.8

- Corrige o problema de a configuração temporária da duração da tradução do site não ter efeito.

## 0.5.7

- Super atualização!

- A funcionalidade "Mostrar apenas tradução" está aqui! Clique em [Mais] -> [Alternar para mostrar apenas tradução].

  - Suporte a atalhos personalizados, definidos em "Configurações de interface" -> "Configurações de atalho"

- Otimizada a questão de limitação de frequência de requisições da OpenAI

- O ChatGPT agora usa o modelo mobile por padrão, que é mais rápido!

- Refatoração da análise do núcleo da web, o que significa:

  - Tradução em larga escala de páginas da web em segundos
    - Por exemplo: [https://pve.proxmox.com/pve-docs/pve-admin-guide.html](https://pve.proxmox.com/pve-docs/pve-admin-guide.html), que antes levava 30 segundos, agora é traduzida em segundos.
  - Uso de memória ultrabaixo para páginas complexas
    - Por exemplo: [https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1](https://www.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1)
  - Adaptação a mais sites

- Todas as traduções de sites usando ShadowRoot são suportadas.

  - Por exemplo: [https://bugs.chromium.org/p/chromium/issues/detail?id=418987](https://bugs.chromium.org/p/chromium/issues/detail?id=418987)
  - Por exemplo, a seção de comentários de: [https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html](https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html)

- Corrigido o problema de tela branca após a tradução de sites com hidratação, como o Next.js.

  - Por exemplo: [https://webpack.js.org/](https://webpack.js.org/)

- Corrigido o problema em que a modificação do atalho de foco do mouse precisava de uma atualização da página para ter efeito.

- Corrigido um problema com o reconhecimento de quebra de linha em arquivos TXT.

- Muitas novidades!

- A funcionalidade "Mostrar apenas tradução" chegou! Clique em "Mais" -> "Alternar para mostrar apenas tradução".

  - Permite atalhos personalizados, configuráveis em "Configurações de interface" -> "Configurações de atalho"

- Otimizado para o problema de limite de taxa de requisições da OpenAI

- A análise do núcleo da web foi reconstruída, o que significa:

  - Tradução instantânea para sites grandes
  - Uso mínimo de memória para páginas complexas
  - Melhor compatibilidade com mais sites

- Suporte a tradução para todos os sites com ShadowRoot.

- Corrigido o problema de tela branca após a tradução de sites com hidratação, como Next.js

- Corrigido o problema em que a alteração do atalho de passagem do mouse exigia uma atualização da página

- Corrigido o problema de reconhecimento de quebra de linha em arquivos TXT.

## 0.5.6

- Correção: problema de pop-up em nova guia no macOS.
- Novo: nova página de guia para novos usuários.

## 0.5.5

- Correção: problema de área de foco do mouse.

## 0.5.4

- Correção: duplicação de página Spa.

## 0.5.3

- Correção: atalhos do mouse hover no userscript.
- Correção: tradução de documentos PDF.
- Novo: adicionada nova página de guia para o cliente.

## 0.5.2

- Correção: configurações de atalhos do mouse hover no userscript.

## 0.5.1

- Correção: API OpenAI não funciona.

## 0.5.0

- Novo: traduzir o parágrafo atual ao passar o mouse.
- Novo: refatoração da tradução de PDF, agora você pode traduzir a maioria dos PDFs com o Immersive Translate.
- Correção: desabilitar o menu de contexto não estava funcionando [#428](https://github.com/immersive-translate/immersive-translate/issues/428).
- Correção: evitar política de segurança de conteúdo para [Mastodon](https://mastodon.social/).

## 0.4.11

- Correção: permissão do userscript (apenas para userscript).

## 0.4.8

- Novo: Bing Translate para Microsoft Translate para uma qualidade mais estável.
- Correção: página da web TXT pura como [esta](https://edoras.sdsu.edu/~vinge/misc/singularity.html).
- Desempenho: exclusão de algumas páginas de publicidade secundárias no site, com pequena melhora no desempenho.

## 0.4.7

- Correção: pop-up do Userscript no Firefox ausente.

## 0.4.6

- Novo: permitir que terceiros enviem eventos de documento para chamar `toggleTranslatePage`.
- Novo: aplicativo iOS adiciona botão para ativar a extensão e links para comunidades.
- UI: o campo de modelo de configurações do OpenAI usa seleção em vez de caixa de entrada de texto.

## 0.4.5

- Correção: problema de extensão do Safari no iOS 15.0.
- Correção: atalhos de extensão do Safari no macOS.
- Correção: pop-up de política de segurança de conteúdo para extensão e parcialmente para userscript.

## 0.4.4

- Correção: remoção de console.log.

## 0.4.3

- Correção: detecção de espaço em branco em tags sup e sub.
- Novo: suporte ao site ChatGPT Plus como serviço de tradução. Este é um recurso beta, portanto, você pode acessá-lo ativando o recurso Beta nas configurações do desenvolvedor. Isso é muito lento, pois o ChatGPT só pode enviar uma solicitação por vez. Certifique-se de ter uma conta ChatGPT Plus, pois há mais limites na conta gratuita e não tenho certeza se isso traz riscos para sua conta, tenha cuidado ao usá-la.

## 0.4.1

- Correção: menu de contexto do Firefox desaparecia após reiniciar.
- Suporte ao Azure OpenAI.

## 0.4.0

- Novo: suporte para tradução de arquivos de legenda locais (.srt, .ass, etc.).

## 0.3.17

- Novo: suporte para tradução de arquivos .txt locais.
- Correção: o menu de contexto pode não estar disponível às vezes. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Correção: manter &nbsp; como espaço em branco.
- Remoção: Papago removido, pois [o serviço está fora do ar](https://github.com/immersive-translate/immersive-translate/issues/310).

## 0.3.15

- UI: permite nenhuma chave de API para OpenAI.
- UI: permite que o OpenAI seja redefinido para as configurações padrão.

## 0.3.14

- Dependência: atualização do pdf.js para a versão mais recente.
- Correção: cor de fundo da seleção de PDF.
- Correção: detecção de espaço em branco.

## 0.3.13

- Correção: problema de caractere específico do criador de e-book, como algum caminho de capítulo ser `xxx' xxxx`.
- UI: opções personalizadas do OpenAI dobradas por padrão.
- UI: adicionado status de exportação para exportação epub.
- Correção: prompt padrão do GPT4.

## 0.3.12

- Recurso: agora podemos personalizar a cor de fundo do tema de tradução do marcador.
- Correção: postMessage ao iniciar a página quebrava alguns sites, agora faremos isso apenas quando realmente traduzirmos as páginas.
- Correção: problema de progresso do ebook.
- Correção: melhor para dividir parágrafos longos, 1,5 bilhão, 25,5%, Mr. não será considerado como um limite.

## 0.3.11

- Correção: cor do texto do leitor de ebook no modo escuro.
- Correção: prompt do OpenAI.

## 0.3.10

- Melhor: detectar contêiner japonês/coreano.
- Correção: progresso do Ebook Builder parou em 99%.

## 0.3.9

- Correção: a troca de serviços de tradução da interface do usuário de opções não alterava o estado da entrada.

## 0.3.8

- UI: cor de carregamento mais transparente.
- Correção: detectar idioma do Ebook.
- Recurso: adicionar progresso de tradução para o criador de ebook e um belo confete após o sucesso.
- Recurso: adicionar nova tentativa a todos os parágrafos com falha para o botão de nova tentativa.
- Correção: tratamento de erros DeepL.

## 0.3.7

- Correção: o leitor de ebook não conseguia carregar imagens no Chrome.

## 0.3.6

- UI: melhor para fazer a página de criação de ebook UI.

## 0.3.5

- Correção: exportação de ebook do userscript.
- Recurso: adicionar endpoint de API personalizado para OpenAI.
- Recurso: adicionar opções de tempo temporário do site de tradução em "Configurações avançadas".

## 0.3.4

- CI: Falha na compilação.

## 0.3.3

- Correção: criador de ebook para Kindle.
- Alteração: cor do ícone de carregamento, de preto para azul, para adaptar à página da web no modo escuro.
- Recurso: suporte à tradução local de arquivos HTML para extensão.

## 0.3.2

- Correção: movimentação do cursor de entrada do formulário de opções.
- Recurso: OpenAI suporta apiUrl personalizado para configurações de desenvolvimento.

## 0.3.1

- Recurso: atualizar o ícone escuro para transparência.
- Correção: ordem errada para parágrafos longos.

## 0.3.0

- Versão: A partir de agora, mudaremos o número da versão menor uma vez por mês, por exemplo, agora em março, a versão começará em 0.3.0, em abril, o número da versão começará em 0.4.0, no próximo abril, o número da versão será 1.4.0 e assim por diante. Isso ocorre porque não faz sentido para as extensões seguir a semântica, mas padronizar os números de versão de acordo com as leis do tempo é uma motivação para o desenvolvimento continuar atualizando e para os usuários encontrarem problemas mais facilmente.
- Recurso: suporte a ícone escuro para Firefox.

## 0.2.86

- Adicionada opção de comprimento máximo de texto por solicitação com Open AI.
- Correção: identificador de ebook duplicado.
- Recurso: suporte à tradução de páginas da web TXT.

## 0.2.85

- Correção: alguns arquivos epub não podem ser encontrados.

## 0.2.84

- Recurso: suporte para Ebook Reader e Maker.

## 0.2.83

- Recurso: permite que a senha de entrada do formulário mostre a senha.

## 0.2.82

- Correção: alguns sites usam `span` para estilos, então usamos `font` em vez de span para o wrapper de destino da tradução.
- Correção: limite máximo de tokens do OpenAI, alterando o máximo de caracteres de 1500 para 1300.

## 0.2.81

- Correção: m.youtube.com
- Correção: interface do usuário do formulário de opções
- Correção: prompt do OpenAI
- Recurso: suporte a várias chaves do OpenAI, use ',' para separá-las.

## 0.2.80

- Recurso: adicionar menu Ativar/Desativar para pop-up -> mais.
- Correção: conflito de mensagem do DingTalk.

## 0.2.79

- Correção: OpenAI para parágrafo de espaço.

## 0.2.78

- Recurso: suporte ao OpenAI CHATGPT 3.5 (suporta a interface OpenAI ChatGPT 3.5).
- Recurso: adicionar novo tema Solid Border (nova borda com linha sólida).

## 0.2.77

- Correção: erro de várias tags de código. [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Correção: erro de várias tags de código [#178](https://github.com/immersive-translate/immersive-translate/issues/178).

## 0.2.75

- Recurso: suporte à contagem de texto de tradução imediata personalizada para diferentes serviços de tradução.

## 0.2.74

- Recurso: suporte a Tencent (alfa).
- Correção: tradução do OpenAI.
- Correção: verificação em linha de tags desconhecidas.

## 0.2.73

- Recurso: suporte ao tema de tradução cinza.
- Correção: página de tendências do Github.

## 0.2.72

- Correção: problema de rede de serviço de tradução do Firefox mobile.

## 0.2.71

- Correção: permissão do userscript do OpenAI.

## 0.2.70

- Correção: espaço reservado do OpenAI.

## 0.2.69

- Recurso: suporte ao OpenAI como serviço de tradução.
- Recurso: suporte à verificação do serviço de tradução em options.html.
- Recurso: suporte ao quadro principal personalizado, pois alguns sites não usam o corpo como quadro principal.

## 0.2.68

- Suporte a Caiyun (Alfa).
- Correção de tags de bloco desconhecidas.

## 0.2.67

- Recurso: adicionado `<all>` para sempre traduzir idiomas, então agora você pode usá-lo para traduzir todos os idiomas, exceto o idioma de destino e nunca traduzir idiomas.
- Correção: permitir configuração de API personalizada do Google.
- Melhor: suporte gratuito ao DeepL.
- Correção: alto uso de memória para userscripts e extensão (removendo opencc zh-CN para zh-TW, em vez de Google Tradutor).
- Correção: Relingo [#159](https://github.com/immersive-translate/immersive-translate/issues/159).
- Correção: configuração de tradução do Azure, mas ainda mostrando (precisa de configuração).

## 0.2.66

- Correção: falha na tradução de arquivos PDF, bug da versão 0.2.60 para suportar DeepL de zh-CN para zh-TW.

## 0.2.65

- Suporte a solicitações de aceleração para vários quadros.
- Não traduzir o título da página quando estiver em iframe.

## 0.2.64

- Correção: seleção de serviços de tradução do OpenAI.
- Recurso: suporte à opção de traduzir título.

## 0.2.63

- Recurso: suporte ao serviço de tradução do Azure.
- Recurso: suporte ao serviço de tradução do Papago.
- Correção: sincronização nativa do Google Drive no Firefox para Android.
- Correção: alteração da transparência de 0.4 para 0.618 [#147](https://github.com/immersive-translate/immersive-translate/pull/147).
- Correção: dicas de atalhos no pop-up.
- Desempenho: solicitações seriais para simultâneas.
- Melhor para detectar a contagem de japonês.

## 0.2.62

- Recurso: adicionar regra waitForSelectors, para corrigir alguns sites como o Reddit.

## 0.2.61

- Correção: userscript muito grande para Greasy Fork.
- Melhor: reduzir o tamanho do arquivo.

## 0.2.60

- Recurso: suporte a zh-CN para zh-TW para DeepL.
- Recurso: Immersive Translate DeepL Feature.
- Recurso: suporte a zoom de tamanho de fonte personalizado.
- Correção: estilo do fórum Steam.
- Correção: estilo global não alterado após a geração de elementos dinâmicos.
- Correção: priorizar exclusão de promoção.
- UI: alteração da página sobre.
- Correção: alguns elementos matemáticos permanecem originais.

## 0.2.59

- Correção: elemento de bloco Unkowntags.
- Correção: sobrescrever elemento translate=no.
- Correção: correspondência de URL com vários \*.

## 0.2.58

- Recurso: suporte a cor de texto de tradução personalizada, cor da borda.

## 0.2.57

- Sem alterações, reconstrução.

## 0.2.56

- Correção de tradução duplicada para elementos inline com elemento de código.
- Correção de verificação inline/block de tags desconhecidas.
- Recurso: suporte a CSS injetado no painel do desenvolvedor.
- Recurso: aparar authKey, appid appSecret.
- Melhor: abrir página de configurações em uma nova guia (mas não para Stay).

## 0.2.55

- Tentar corrigir o conjunto de caracteres da API DeepL.

## 0.2.54

- Remoção da permissão de guias para rejeição da Chrome Store.
- Correção: ao traduzir a página inteira, o rodapé era ignorado.
- Adicionadas notas à página sobre.
- Suporte a URL personalizado da configuração interna.

## 0.2.53

- Correção de erro de sincronização do Google Drive no userscript.

## 0.2.52

### Código

- Usar o esbuild mais recente.
- Usar a versão mais recente do Deno.
- CI: enviar código-fonte para o Firefox.

## 0.2.51

- Correção: autenticação do Google precisa de login no Chrome/Firefox.
- Substituição de links de serviço de tradução.
- Melhora nas permissões.
- Remoção de minificação.

## 0.2.50

- Correção do problema de upload do Google Drive (realmente) [#81](https://github.com/immersive-translate/immersive-translate/issues/81).

## 0.2.49

- Remoção dos atalhos alt+d, alt+s, pois podem entrar em conflito com atalhos nativos.
- Correção do problema de upload do Google Drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81).

## 0.2.48

- Melhora na velocidade, adicionando minLength para 50 para detecção de idioma.
- Correção da validação do token do Google Drive.

## 0.2.47

- Correção da API DeepL.

## 0.2.46

- Correção de marca de bloco.

## 0.2.45

- Correção de elemento innerText indefinido.
- Correção de idioma de origem indefinido na tradução de Caiyun.

## 0.2.44

- Correção de alternância de máscara do userscript.
- Correção da lógica de alternância de máscara.

## 0.2.43

- Corrigido problema de alternância da máscara do userscript com evento de toque.
- Corrigido a velocidade (removendo sleep(300))

## 0.2.42

- Corrigido foco na máscara ao alternar a máscara novamente.
- Adicionados atalhos de máscara para dispositivos móveis
- Corrigido problema de sincronização em nuvem do userscript
- Movida a página de opções avançadas para o menu esquerdo.
- Adicionada lógica de nova tentativa ao serviço de tradução

## 0.2.41

- Correção da tradução Niu no userscript.
- Correção da tradução XHTML.

## 0.2.40

- Correção da exibição do recurso beta.
- Correção da página de configurações pop-up na nova página da guia.
- Correção da substituição do espaço reservado da tradução.

## 0.2.39

- Suporte a atalhos para mostrar a tradução da máscara.
- Suporte para habilitar o recurso beta no painel do desenvolvedor.
- Correção de atalhos na extensão móvel.

## 0.2.38

- Suporte para carregar tema.
- Correção de getpocket.com.
- Correção de rodapé lateral para área do corpo.
- Correção do ícone de importação/exportação.

## 0.2.37

- Correção da marca de exclusão de quadro.

## 0.2.36

- Suporte à sincronização com o Google Drive.

## 0.2.35

- Correção de tag rb, rt japonesa ignorada.
- Melhorias na interface do usuário pop-up.
- Melhorias nas dicas de userscript incorreto.
- Adição de contribuição à página sobre.
- Correção da tradução automática do Volc.

## 0.2.34

- Correção de velocidade de tradução de vários idiomas.

## 0.2.33

- Suporte ao modo de escrita vertical, como japonês.
- Adição de 3 temas.
- Adição do serviço de tradução Niu.

## 0.2.32

- Correção da tradução básica de PDF.
- Correção de pop-up ao selecionar um serviço não configurado, indo para a página de opções.
- Correção das configurações de permanência aberta.
- Correção da velocidade de detecção de vários idiomas.

## 0.2.31

- Correção de injeção de CSS dinâmica em iframe.

## 0.2.30

- Suporte à tradução de iframe em linha no userscript.
- Suporte à tradução shadowroot. Por exemplo:
  - [https://www.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation](https://www.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation)
    - Área de conversa.
- Também verifica a regra de sincronização no pop-up.

## 0.2.29

- Correção da tradução do Facebook.
- Suporte para mostrar a opção do menu de contexto.

## 0.2.28

- Remoção de correspondência não padrão para userscript.

## 0.2.27

- Suporte à tradução de iframe em linha. (Apenas para extensão, não disponível para userscript).
- Correção de tradução de vários idiomas.

## 0.2.26

- Correção do complemento do Firefox para Android.
- Adição de configurações avançadas para nova linha de tradução.

## 0.2.25

- Suporte à tradução de iframe, como QQ mail, tweet incorporado.

## 0.2.24

- Adicionada tradução temporária do site por um tempo.
- Correção da API do navegador Stay.app userscript.
- Correção da página de opções do Stay.app.

## 0.2.23

- Correção da tradução de páginas com vários idiomas.

## 0.2.22

- Correção da compilação do userscript.

## 0.2.21

- Corrigida tradução online de PDF no Firefox

## 0.2.20

- Corrigido problema de requisição do macaque
- Corrigida a altura da linha de destaque da marcação

## 0.2.19

- Correção: japonês inteligente da Tencent.
- Correção: navegador Haikuo World.

## 0.2.18

- Correção: alteração de URL do cliente, manter automaticamente o estado da tradução.
- Remoção do contêiner lateral como contêiner de tradução.
- Refatoração da posição do pop-up.

## 0.2.17

- Alteração de destaque para marca.
- Adição de tema de tradução de destaque.

## 0.2.16

- Compatibilidade com Macaque.

## 0.2.15

- Correção de problema de salto de toque.

## 0.2.14

- Correção de globalThis.GM não funcionando no Safari.

## 0.2.13

- Suporte para arrastar o pop-up do Userscript.
- Suporte a três dedos em dispositivos touch para ativar a alternância de páginas de tradução.
- Suporte para ocultar o ícone pop-up do userscript.

## 0.2.12

- Melhorias no Inoreader.

## 0.2.11

- Correção:
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  O conteúdo principal da página do Annas archive não pôde ser traduzido.

## 0.2.10

- Correção da distância da altura da linha do PDF.

## 0.2.9

- Correção da marca de exclusão de elementos.
- Correção da verificação de tipo Deno.
- Remoção do mapa de importação.
- Correção da tradução dos menus de contexto.
- Restauração da página quando a opção "nunca traduzir este site" estiver ativada.
- Adição de descrição para adicionar URL.

## 0.2.8

- Detecta o idioma do usuário para o idioma da interface.
- Corrige erro de quebra de linha.

## 0.2.7

- Corrige requisição do Grease Monkey.

## 0.2.6

- Correção: Problema de correspondência de URL de arquivo
  ([#30](https://github.com/immersive-translate/immersive-translate/issues/30)).

## 0.2.5

- Atualiza versão para teste de integração contínua (CI).

## 0.2.4

- Captura erro de conexão de mensagem para o pop-up.

## 0.2.3

- Corrige criação múltipla de contexto
  ([#26](https://github.com/immersive-translate/immersive-translate/issues/26)).

## 0.2.2

- Corrige arquivo de exemplo de PDF.
- Corrige arquivo PDF local no Firefox.
- Corrige atalhos de PDF.

## 0.2.1

- Suporte ao gerenciador de atalhos do Grease Monkey.
- Corrige expressão regular de correspondência.
- Corrige comentários do YouTube.
- Corrige versão compacta móvel do Reddit.
- Corrige problema de tradução de texto completo.

## 0.2.0

- Corrige PDF de duas colunas.
- Corrige bug na versão da Chrome/Edge Store.
- Corrige problema
  ([#21](https://github.com/immersive-translate/immersive-translate/issues/21)).

## 0.1.2

- Publica no complemento do Firefox.
- Publica na Edge.
- Corrige margem do PDF.
- Altera arquivo de exemplo de PDF.

## 0.0.62

- Corrige formatação e recuo de PDF.
- Corrige prevenção de alteração de elemento em telegra.ph.

## 0.0.61

- Corrige fechamento de elemento span.
- Corrige permissão para navegadores antigos.

## 0.0.60

- Corrige PDF do Chrome.

## 0.0.59

- Suporte inicial para PDF.

## 0.0.58

- Edita descrição do tema de tradução.

## 0.0.57

- Altera interface do usuário do pop-up para facilitar o uso.

## 0.0.56

- Corrige tempo limite do Chrome.
- Corrige erro de divisão de frase.

## 0.0.55

- Corrige exibição de elemento oculto.
- Refatora marcação de elemento.

## 0.0.54

- Suporta quebra de linha para X caracteres.

## 0.0.53

- Usa sendMessage em vez de connect, pois o Chrome desconecta a porta após 5 minutos.
- Melhora detecção de contêineres de texto.

## 0.0.52

- Não traduz parágrafos que possuem apenas elementos de espaço reservado,
  por exemplo, a primeira linha em ([https://github.com/nank1ro/solidart](https://github.com/nank1ro/solidart)).
- Melhora detecção de elementos filho.

## 0.0.51

- Corrige problema de cache
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive- translate/next-immersive-translate/issues/7)
- Corrige tamanho da fonte da interface de opções.

## 0.0.50

- Corrige tradução de imagens em bloco.

## 0.0.49

- Corrige extensão do Firefox.

## 0.0.48

- Corrige extensão do Chrome.

## 0.0.47

- Reescreve mensagem em segundo plano, usa connect em vez de sendMessage.
- Adiciona suporte para Reddit mobile.
- Corrige espaço em branco em pré-formatação para alguns artigos.

## 0.0.46

- Formata meta informações do userscript.

## 0.0.45

- Userscript usa um arquivo.
- Adiciona tempo limite para requisição de cache.

## 0.0.44

- Corrige erro de divisão do Tencent.
- Corrige erro de elemento sup em linha.
- Melhora para o Twitter.

## 0.0.43

- Corrige quebra de linha em tweets.
- Corrige tradução global.

## 0.0.42

- Corrige tag BR.
- Trata tags de bloco como regras.

## 0.0.41

- Corrige verificação de elemento em linha.
- Adiciona opção de log de depuração para desenvolvedores.

## 0.0.39

- Corrige serviço de tradução contendo mock2.

## 0.0.38

- Suporte a resultado em cache para userscript.
- Adiciona interface de opções.
- Suporte a detecção de mais contêineres de conteúdo.

## 0.0.37

- Corrige problema de não funcionamento da alteração do serviço de tradução no pop-up.
- Corrige tradução de conteúdo de postagem no Reddit mobile.

## 0.0.36

- Corrige caracteres especiais da Wikipédia
  ([#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)).
- Corrige tamanho do ícone do userscript.
- Habilita detecção de idioma de parágrafo em todos os sites.

## 0.0.35

- Corrige ir para a próxima página no YouTube.
- Suporte à página de pesquisa do YouTube.
- Corrige alternância avançada de opções.
- Corrige tags img e hidden
  ([#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)).
- Corrige atualização forçada da Pesquisa Google
  ([#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)).
- Suporte a resultados em tabela do Google
  ([#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)).
- Corrige problema de página em branco na Wikipédia
  ([#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)).

## 0.0.34

### Mudanças Importantes

- A tecla de atalho padrão para alternar a tradução foi alterada para `alt+A`, pois
  é a tecla mais conveniente para digitar.

### Outros

- Suporte para definir modo de tradução imediata, permitindo que a página seja traduzida o mais
  rápido possível.
- Suporte para definir a área da página a ser traduzida, permitindo traduzir mais áreas.
- Suporte para definir a quantidade inicial de texto a ser traduzida imediatamente.
- Corrige tradução duplicada ao alterar o serviço de tradução.
- Interface do usuário do pop-up aprimorada.

## 0.0.33

- Suporte a mais idiomas: zh-TW, en.

## 0.0.32

- Corrige tradução de arquivo local após salvar. Corrigido
  ([#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)).
- Adiciona arquivo js dist ao repositório público.

## 0.0.31

- Suporte à tradução da página inteira.
- Suporte à tradução imediata da página.
- Mais opções de configuração na interface do usuário.
- Reflete o tema.
- Adiciona novo ícone.
- Adiciona novo tema de tradução dashedBorder.

## 0.0.30

- Melhora para o tema dashed.

## 0.0.29

- Corrige validação de parágrafo.
- Adiciona temas dotted e thinDashed.
- Melhora para os temas dashed e highlight.

## 0.0.28

- Corrige sublinhado.
- Adiciona temas dashed e paper.
- Corrige detecção de cabeçalho.

## 0.0.27

- Suporte a translationTheme.

## 0.0.26

- Corrige permissão de conexão do userscript volc alpha.
- Corrige a possibilidade de clicar na versão.

## 0.0.25

- Suporte a selectorMatches, permitindo correspondência com todos os Mastodon agora.
- Corrige erro de userscript no Firefox.

## 0.0.23

- Melhora na detecção de chinês.
- Corrige problema de innerText no Reddit.

## 0.0.22

- Suporte a DeepL.
- Corrige múltiplas traduções ao alternar o serviço.

## 0.0.21

- Corrige algumas tags span como elemento de bloco.

## 0.0.20

- Suporte a não traduzir hashtags como #hashtag, tags de arroba como @xxx, $tag, como $APPL.
- Suporte a elementos de bloco.

## 0.0.18

- Suporte a DeepL, Bing, Baidu, Youdao, volc, OpenAI e Caiyun.

## 0.0.13

- Suporte a userscript.

## 0.0.4.8

- Corrige ordem do código.
- Suporte a interface básica do pop-up.

## 0.0.4.6

- Suporte a verificação de nova versão.

## 0.0.3

- Suporte a arquivos locais.

## 0.0.2

- Suporte a elementos dinâmicos.
- Suporte a tradução visível.
