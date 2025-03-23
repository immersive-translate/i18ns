---
sidebar_position: 6
---

# Registo de Alterações

Este registo de alterações é atualizado de acordo com o progresso do desenvolvimento. A data após a versão é a data de fusão do código, não a data de Release nas lojas de aplicativos (o tempo de revisão varia após a submissão a cada loja de aplicativos, podendo algumas demorar até uma semana para revisão). Atualmente, estamos a avançar com duas versões.

A **versão Release** é a versão estável oficial, disponível nas principais lojas de aplicativos como [Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh), [Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg), [Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/), [Apple](https://apps.apple.com/app/id6447957425), etc.

A **versão Preview** é publicada com mais frequência e inclui algumas funcionalidades experimentais. Comparada com a versão Release, pode conter mais bugs. É lançada principalmente em

- [userscript do site oficial](https://download.immersivetranslate.com/immersive-translate.user.js)
- [versão beta na loja Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.15.9 Release (2025-03-23)

- Corrigido: Um problema onde a tradução não funcionava no Safari 16.4.

## 1.15.8 Release (2025-03-20)

- Corrigido: Um problema onde a tecla de atalho de tradução por hover não funcionava em dispositivos que suportam tanto rato como toque.
- Adicionado: Suporte para tradução de modelo grande Youdao Ziyue.

## 1.15.7 Release (2025-03-19)

- Adicionado: Pré-tradução dinâmica de conteúdo a ser traduzido ao navegar em páginas.
- Corrigido: Um problema onde o serviço de tradução AI outputava incorretamente Chinês Simplificado ao traduzir Chinês Tradicional.
- Corrigido: Um problema com a tradução por hover não funcionando no modo "Tradução primeiro, texto original segue".
- Corrigido: Problemas de compatibilidade com o modo "Apenas Tradução" quando usado com plugins de leitura como Reader View.
- Otimizado: Melhorada a qualidade do serviço de tradução AI para conteúdo principal.
- Otimizado: Melhorado o suporte para tradução de imagens em certos sites.
- Otimizado: Otimizado o formato de texto misto em Chinês e Inglês.
- Otimizado: O serviço de tradução Gemini suporta prompt de sistema personalizado (System Prompt).
- Otimizado: Melhorada a velocidade do userscript.

## 1.15.2 Release (2025-03-02)

- Adicionado: Gemini suporta Português (Brasil).
- Adicionado: Serviços de tradução Grok, Ollama, Groq, Azure-OpenAI.
- Corrigido: Problema de tradução de legendas no Google Meet e Microsoft Teams.
- Corrigido: Problema de tradução do Google com caracteres de escape.
- Otimizado: Melhorada a precisão na identificação automática do idioma do conteúdo traduzido.
- Otimizado: [Tradução de imagem gratuita] suporta formatação para idiomas da direita para a esquerda.
- Otimizado: Compatível com modelos como o1, o3 que não suportam função de sistema (o parâmetro de função de sistema não será passado quando a configuração do System Prompt estiver vazia).

## 1.14.16 Release (2025-02-21)

- Adicionado: Deepseek, Gemini, Claude suportam troca de contexto.
- Corrigido: Atualizar termos não envia nova solicitação de tradução.
- Melhorado: Idioma da interface adiciona Húngaro.
- Melhorado: Qualidade da tradução do Google.
- Melhorado: Formatação de imagem gratuita.

## 1.14.12 Release (2025-02-19)

- Melhorado: Pausar tradução limpa imediatamente a fila de solicitações.
- Melhorado: Filtra texto sujo no serviço de tradução deepl.
- Corrigido: Tradução inválida da barra lateral nas configurações avançadas.
- Corrigido: Problema de exibição de tradução personalizada deepseek.

## 1.14.11 Release (2025-02-18)

- Corrigido: Erro `401: Authentication Fails` na API Key personalizada do DeepSeek.

## 1.14.10 Release (2025-02-17)

- Novo: Membros Pro suportam o serviço de tradução DeepSeek (v3).
- Corrigido: Resolvido problema de arquivo de configuração do usuário excedendo o limite de tamanho.
- Melhorado: Item de menu de clique direito pode ser fechado (operado nas configurações avançadas).
- Melhorado: Melhoradas as capacidades de reconhecimento de idioma para Greasemonkey e Safari em páginas com idiomas menores.
- Melhorado: Acesso à interface de teste da página de configurações online.
- Melhorado: Experiência do usuário aprimorada da funcionalidade de pré-visualização de comparação de contexto.
- Melhorado: Lógica de julgamento de modo de toque e rato.

## 1.14.8 Release (2025-02-10)

- Corrigido: Problema onde arquivos longos do PDF-Pro não eram traduzidos automaticamente.
- Melhorado: Microsoft, Google e Tencent agora suportam Cantonês.
- Melhorado: BBC agora suporta legendas.

## 1.14.6 Preview (2025-02-08)

- Corrigido: Problema onde a **Tradução por Hover do Rato** não conseguia traduzir texto rico.
- Melhorado: Versão Tampermonkey agora suporta tradução de legendas do YouTube.

## 1.14.4 Release (2025-02-07)

- Corrigido: Problema com detecção incorreta de idioma na **Caixa de Entrada Aprimorada**.
- Corrigido: Problema de correspondência inteligente de especialistas em AI em serviços de tradução personalizados.
- Corrigido: Problema de falha de sincronização do Google Drive em alguns navegadores.
- Corrigido: Problema de tradução de comentários ao vivo do YouTube.
- Corrigido: Problema de sobreposição de legendas em alguns vídeos do YouTube.
- Melhorado: Falha na tradução de mangás em sites como shonenjumpplus no navegador Safari.

## 1.13.8 Release (2025-01-24)

- Novo: Tradução de imagem gratuita agora está disponível (atualmente suportada apenas nas versões para PC dos navegadores Chrome e Edge), acessível via menu de clique direito.
- Corrigido: Resolvido um problema onde algum conteúdo era perdido durante a tradução de múltiplos segmentos no Gemini.
- Otimizado: Melhorado o carregamento de legendas do YouTube.
- Novo: Serviço de tradução AI agora suporta Norueguês.

## 1.13.6 Preview (2025-01-17)

- Melhorado: **AI Expert** pode ser usado com **AI Context-Aware Translation**.
- Melhorado: **Tradução de Imagem** agora é compatível com weibo.com (suportado apenas no Chrome e Edge).
- Melhorado: Quando o idioma da interface está definido para Inglês, o idioma alvo padrão para a **Caixa de Entrada Aprimorada** é alterado para Chinês.
- Melhorado: Adicionada uma entrada de revisão da loja nas opções **Mais** no painel.

## 1.13.5 Release (2025-01-14)

- Melhorado: Compatível com o modelo de pensamento Gemini 2.0.
- Melhorado: Suporta estilo negrito no modo apenas tradução.

## 1.13.4 Preview (2025-01-13)

- Adicionado: Membros Pro agora podem usar diretamente o modelo **Zhipu 4 Plus**.
- Melhorado: Tradução Gemini.

## 1.13.1 (2025-01-10)

- Adicionado: Quando o texto traduzido e o texto original pertencem ao mesmo sistema de escrita, exibir a tradução usando um estilo especializado.
- Corrigido: O problema onde a **Tradução por Hover do Rato** não funciona em alguns sites.
- Melhorado: DeepLx agora suporta Árabe.
- Melhorado: Melhorado o reconhecimento do idioma original. Anteriormente, páginas contendo múltiplos idiomas poderiam não ser traduzidas, mas agora são traduzidas corretamente.
- Melhorado: Para o Twitter, traduções de conteúdo multilinha são configuradas para não quebrar por padrão. A quebra ocorrerá apenas quando o conteúdo exceder 10 linhas ou 1000 caracteres. A quebra pode ser ativada através das configurações **Configurações Avançadas** -> **Ativar quebra automática de linha para parágrafos longos**.

## 1.12.8 (2025-01-03)

- Corrigido: o problema onde a página de configurações do iOS 18.3 não pode ser exibida corretamente.
- Corrigido: a falta de linhas vazias ao traduzir tweets.
- Corrigido: o problema de números decimais sendo forçadamente quebrados em linha ao traduzir textos longos.

## 1.12.7 Release (2024-12-30)

- Melhorado: Bing/Google agora suportam Português (Brasil).
- Melhorado: Melhoradas as descrições para o idioma da interface em Chinês Tradicional.
- Melhorado: Ajuste de layout para idiomas da direita para a esquerda em painéis e páginas de configurações.

## 1.12.6 (2024-12-26)

- Corrigido: Problema onde a função de hover do rato carrega o serviço de tradução errado sob certas condições.
- Corrigido: Problema onde ativar temporariamente legendas bilíngues no YouTube não funciona.
- Corrigido: Após mudar serviços de tradução, o serviço de tradução na "**Caixa de Entrada Aprimorada**" não atualiza.
- Corrigido: O interruptor "**YouTube Enable Bilingual**" na página de configurações não está funcionando.
- Melhorado: Removido o modelo gemini-1.0-pro obsoleto.

## 1.12.4 (2024-12-13)

- Adicionado: **AI Context-Aware Translation** pode melhorar a precisão da tradução de conteúdo profissional. (Disponível apenas para membros Pro, suportado exclusivamente por modelos OpenAI) **Opções** -> **Geral** -> **Ativar AI Context-Aware Translation**
- Corrigido: Alguns bugs no efeito de tradução multilinha no Twitter.
- Corrigido: Problemas com a tradução de certas fórmulas devido a texto rico.
- Melhorado: Ao traduzir no **x.com**, vídeos com legendas terão automaticamente legendas bilíngues traduzidas.
- Melhorado: Vídeos sem legendas exibirão um ícone de tradução e fornecerão uma razão pela qual a tradução não é possível.

## 1.11.7 (2024-11-25)

- Adicionado: Bing/Google agora suportam Khmer (Cambojano).
- Adicionado: Permitir que arquivos ePub incompletos continuem a tradução de onde pararam após reimportação.
- Corrigido: Problema com tradução de imagens do Twitter no navegador Safari.
- Corrigido: Teclas de atalho tornando-se ineficazes ao alternar a funcionalidade "**Hover Translation**".
- Melhorado: Exibição aprimorada de tradução bilíngue multilinha no Twitter e Youtube.
- Melhorado: Tradução de texto rico é desativada por padrão no modo bilíngue para melhorar a qualidade da tradução.
- ~~Melhorado: Adicionada a opção de personalizar a "**Ativar Tradução de Barra Lateral & Navbar**" em "**Configurações Avançadas**".~~
- Melhorado: Imagens não são mais traduzidas no modo "**Hover - traduzir imediatamente este parágrafo**".

## 1.11.4 (2024-11-16)

- Corrigido: Problema com tradução de fórmulas causado pela "Melhoria de Tradução do Twitter" na versão 1.11.2.

## 1.11.2 (2024-11-13)

- Corrigido: Problema onde o conteúdo desaparece após clicar em "ver mais" no modo apenas tradução do Facebook.
- ~~Melhorado: Exibição aprimorada de traduções bilíngues multilinha no Twitter.~~
- Melhorado: Atualizada a interface do utilizador da lista suspensa de serviços de tradução no painel.

## 1.11.1 (2024-11-05)

- Adicionado: A ativação da **Tradução de Legendas** em tempo real agora é suportada via "float ball", disponível no Zoom, Google Meet e Microsoft Teams.
- Corrigido: Problemas de sincronização de tempo das legendas no YouTube após assistir a anúncios.
- Corrigido: Problemas de exibição com o menu de tradução do clique direito no Safari no MacOS 15.
- Corrigido: Problemas com a funcionalidade de desfazer Ctrl+Z no **Enhanced input** em certos websites.

## 1.10.6 (2024-10-25)

- Corrigido: Problema com as teclas de atalho do **Enhanced input** não sendo acionadas
- Melhorado: Redução do tamanho do pacote de instalação
- Melhorado: Solução de exibição de legendas na Netflix

## 1.10.5 (2024-10-23)

- Adicionado: Exibir um aviso quando a língua de origem e a língua de destino são as mesmas
- Corrigido: Problema de tradução de caracteres de espaço em branco em texto rico [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Melhorado: Aprimoramento de entrada e funcionalidade de passar o mouse dentro de iframes incorporados em páginas web

## 1.10.2 (2024-10-11)

- Adicionado: Tradução de imagens (versão Beta)
- Adicionado: Modo Forçar Ativação do Suporte ao Mouse (Ative este recurso apenas se a função de passar o mouse não estiver disponível em dispositivos tablet) **Configurações** -> **Configurações Avançadas** -> **Forçar Ativação do Suporte ao Mouse**
- Adicionado: Exibir mensagem de erro quando a tradução de legendas de vídeo falha
- Corrigido: Problema de tradução de texto rico [#2163](https://github.com/immersive-translate/immersive-translate/issues/2163)
- Melhorado: Abordados problemas onde o botão de tradução pode não funcionar durante a tradução de PDF
- Melhorado: Aprimorada a renderização de fórmulas traduzidas
- Melhorado: Lista de seleção de idiomas

## 1.9.8 (2024-09-28)

- Adicionado: Serviço de tradução "Zhipu BigModel"
- Removido: Modelo "SiliconCloud" qwen1.5-7B-chat (devido à descontinuação oficial)
- Corrigido: Resolvido problema de compatibilidade de login com o plugin Safari no macOS 15

## 1.9.7 (2024-09-20)

- Suporte aprimorado de entrada para Baidu, Gmail e outros campos de entrada
- Suporte para cabeçalho de solicitação anthropic-dangerous-direct-browser-access para Claude Anthropic API
- Suporte para download de legendas de vídeos do Hulu, Bloomberg e Domestika
- DeepX suporta tradução de texto rico
- Corrigido o problema com especialistas em IA personalizados não sincronizando

## 1.9.6 (2024-09-13)

- [PDF Pro](https://app.immersivetranslate.com/pdf-pro/) suporta cópia de fórmulas (clique com o botão direito na fórmula para ver o menu de cópia)
- Corrigido o problema de exibição de legendas bilíngues para múltiplos vídeos na mesma página do Twitter
- Corrigidos alguns bugs

## 1.9.3 (2024-09-05)

- A opção para comparação bilíngue/exibição apenas de tradução foi movida para as configurações gerais.
- Por padrão, o sistema lembrará o modo alternado ao clicar no ícone no painel para comparação bilíngue ou exibição apenas de tradução. Para alternar temporariamente, clique em "Mais" -> "Alternar para exibição apenas de tradução" no painel.
- Por padrão, traduzir Chinês Simplificado para Chinês Tradicional e vice-versa usará o modo apenas de tradução, em vez do modo de comparação bilíngue.
- Corrigidos alguns bugs.

## 1.9.1 (2024-09-03)

- Suporte para configurar exceções para idiomas e websites no modo de contraste bilíngue ou apenas tradução (configure na página de Configurações -> Configurações Avançadas). Por exemplo: Se o seu modo de tradução padrão é contraste bilíngue, mas você não deseja que o Chinês Tradicional também use contraste bilíngue, então você pode adicionar o Chinês Tradicional aos idiomas de exceção para contraste bilíngue, assim o Chinês Tradicional usará o modo apenas de tradução para tradução. Da mesma forma, se o seu modo de tradução padrão é apenas tradução, mas você deseja que um certo idioma ou website use o modo de contraste bilíngue, você também pode adicionar esse idioma ou website aos idiomas de exceção.
- Corrigido um problema onde a caixa de entrada na interface de mensagem privada do Tiktok era traduzida incorretamente
- Corrigido um problema onde quadrinhos no Read Comic Online não podiam ser traduzidos
- Corrigido um problema onde o [Configurações Avançadas -> Número mínimo de caracteres necessários para traduzir um parágrafo] não surtia efeito em alguns casos

## 1.8.4 (2024-08-30)

- O serviço de tradução DeepL agora suporta oficialmente o Chinês Tradicional como idioma de destino (anteriormente, traduzir para Chinês Tradicional com DeepL envolvia um processo adicional de conversão de Chinês Simplificado para Tradicional de terceiros).
- Otimizado o desempenho da tradução de texto rico.

## 1.8.3

- Google Meet agora suporta legendas bilíngues para reuniões ao vivo: Agora, você pode desfrutar do recurso de legendas bilíngues em reuniões do Google Meet. Basta abrir o link da reunião, ativar as legendas bilíngues no painel de tradução imersiva e, em seguida, atualizar a página para experimentá-lo.
- Adicionada a opção de "Relatar problemas de tradução da página atual" e a opção de "Ligar/desligar rapidamente o float ball" nas mais opções do painel.
- Após ajustar a posição das legendas bilíngues do YouTube, o sistema lembrará automaticamente a nova posição.
- Otimizada a lógica de cache do plugin, agora limpando automaticamente dados de cache com mais de 30 dias.
- Otimizados blocos de código dentro de parágrafos para uma restauração mais precisa do texto original.
- Melhorado o tratamento de "palavras não traduzíveis" nas configurações avançadas.

## 1.8.2

- Agora você pode traduzir texto em caixas de entrada com o clique direito: Selecione qualquer texto em uma caixa de entrada em uma página web, clique com o botão direito para escolher traduzir, e a tradução imersiva traduzirá automaticamente o texto selecionado para o idioma de destino da caixa de entrada, tornando conveniente traduzir rapidamente texto em idioma nativo em caixas de entrada para outros idiomas.
- Agora você pode relatar rapidamente problemas de tradução de páginas web no float ball de tradução imersiva. Após traduzir uma página web, se houver algum problema, você pode clicar no botão [Feedback] no lado direito do float ball, preencher a descrição do problema, e nós lidaremos com isso o mais rápido possível.
- Arquivos Epub agora suportam tradução de texto rico (ou seja, preservando o formato do texto original de cada parágrafo, como links, negrito, etc.)
- Suporte para legendas bilíngues em tempo real em reuniões de vídeo na versão web do Microsoft Teams (Abra o link da reunião do Teams, ative as legendas bilíngues no painel de tradução imersiva e, em seguida, atualize)
- Otimizadas legendas bilíngues para a versão em inglês do iQIYI (iq.com)
- Fornecido mais artigos do arXiv com layout de tradução bilíngue otimizado
- Devido a restrições do site do Youtube, o script do Chrome Tampermonkey não suporta mais legendas bilíngues do Youtube. Por favor, use a [versão do plugin](https://immersivetranslate.com/).

## 1.8.1

- Corrigidos problemas de tradução com o script Tampermonkey SiliconCloud
- A tradução Claude agora suporta Tibetano e permite configuração do parâmetro Temperature
- A página de detalhes do especialista em IA exibe os prompts usados pelo especialista
- As configurações de atalho agora permitem atribuir teclas de atalho exclusivas para qualquer serviço de tradução
- Otimizada a detecção para traduções de artigos do arXiv

## 1.7.9

- Corrigidos problemas com tradução de texto rico para serviços de tradução como Google, DeepL (por exemplo, páginas exibindo diretamente `<button>` etc.)
- Corrigido o problema onde o atalho bilíngue para vídeos do YouTube não podia ser desligado.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini e outros serviços de tradução suportam tradução para manter o formato original do texto (por exemplo, links, negrito, etc.)
- Após selecionar o texto, o menu de clique direito mudará para [Traduzir o texto], clicando no qual você pode pular automaticamente para a página de Tradução de Texto Imersiva
- Novo serviço de tradução gratuito para grandes modelos: SiliconCloud, disponível para todos os usuários.
- Adicionada tradução de grande modelo Zero-One-Thing, que pode ser usada preenchendo a API Key após registrar-se na plataforma Zero-One-Thing.
- Novo botão de feedback do usuário para tradução de mangá (após traduzir um mangá, clique no botão [Feedback] no lado direito do float ball para dar feedback sobre a qualidade da tradução).

## 1.7.7

- Adotado algoritmo de divisão de frases inteligente por IA para legendas em inglês geradas automaticamente no YouTube [Pro Disponível]
- Otimizar a tradução do clique direito para "Traduzir para xx idioma de destino"
- Suporte para integração imersiva [JS SDK](https://immersivetranslate.com/docs/js-sdk/) para websites de terceiros
- Otimizar exibição de legendas do Hulu
- Suporte para tradução de legendas de reunião na versão web do ZOOM

## 1.7.6

- Suporte para personalizar especialistas em IA, a entrada está na parte inferior da página [Configurações]->[Especialista em IA].
- Otimizar carregamento de legendas no site TED
- Português (Brasil) é suportado como idioma do plugin.
- Sites suportados para tradução de quadrinhos
  - [Antbyw](https://www.antbyw.com)
  - [Zerobywzz](https://www.zerobywzz.com)
  - [动漫之家](https://www.idmzj.com)
  - [Jmanga](https://jmanga.org)

## 1.7.5

- Habilitada a cópia de legendas do YouTube
- Otimizada a exibição de legendas em alguns sites de vídeo
- Melhorada a velocidade de tradução de mangás

## 1.7.2

- Corrigida falha de tradução de quadrinhos no navegador Firefox.

## 1.7.1

- Melhorada a velocidade de tradução para traduções de quadrinhos
- Adicionado suporte para novos sites em traduções de quadrinhos:
  - [ShonenJumpPlus](https://shonenjumpplus.com)
  - [Heros Web](https://viewer.heros-web.com/)
  - [Comic Days](https://comic-days.com/)
  - [ComicWalker](https://comic-walker.com/)
  - [Web Ace](https://web-ace.jp/)

## 1.6.6

- Adicionado suporte para novos sites para tradução de quadrinhos:
  - [Mangabuddy](https://mangabuddy.com/)
  - [Hitomi](https://hitomi.la)
  - [Yamibo](https://www.yamibo.com)
  - [Copymanga](https://www.copymanga.site/)
- As legendas bilíngues do YouTube agora suportam divisão inteligente de frases (Beta) (Apenas quando ativar manualmente a tradução imersiva de legendas do YouTube em [Configurações] - [Legendas de Vídeo], e as legendas originais do vídeo são legendas em inglês geradas automaticamente)
- Adicionado serviço de tradução Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Corrigir problemas de layout de texto das traduções de quadrinhos para idiomas no script latino.
- Novos sites suportados para tradução de quadrinhos:
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Corrigido um problema onde serviços de IA personalizados não podiam selecionar especialistas em IA.

## 1.6.4

- Quando especialistas em IA são usados para "Seleção Inteligente", diferentes especialistas em IA podem ser personalizados para diferentes sites. Isso pode ser configurado em [Configurações] -> [Especialistas em IA] -> [Insira qualquer especialista].
- Corrigido o problema em que as legendas não eram exibidas no YouTube no modo "Apenas Tradução".
- Corrigido o problema das legendas bilíngues não funcionarem no Mubi.
- Compatível com PDFs abertos com o plugin Adobe Acrobat.
- Todos os utilizadores podem [contribuir online](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) para a tradução multilíngue da interface de tradução imersiva.

## 1.6.3

- Nova funcionalidade: tradução de Manga (Beta), em sites de manga suportados, um botão de tradução de manga aparecerá abaixo da bola flutuante de tradução rápida da página web. Clicar nele ativará a tradução de manga. Esta funcionalidade está disponível para membros Pro (500 páginas por mês, pacotes adicionais podem ser adquiridos), atualmente suportando os seguintes sites:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nova funcionalidade: tradução de Manga (Beta), em sites de manga suportados, um botão de tradução de manga aparecerá abaixo da bola flutuante de tradução rápida da página web. Clicar nele ativará a tradução de manga. Esta funcionalidade está disponível para membros Pro (500 páginas por mês, pacotes adicionais podem ser adquiridos), atualmente suportando os seguintes sites:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nova funcionalidade: tradução por IA suporta [modelo grande Doubao](https://www.volcengine.com/product/doubao)
- Nova funcionalidade: suporte para modo de comparação bilíngue com tradução primeiro e texto original a seguir, que pode ser ativado na página de configurações -> configurações avançadas.
- A lista de modelos de IA personalizados suporta a sintaxe `-all`, que pode excluir todos os modelos predefinidos.
- Em legendas bilíngues de vídeo, quando o idioma de destino é Chinês Simplificado e o texto original é Chinês Tradicional, o texto original será automaticamente convertido para Chinês Simplificado, e vice-versa.
- Corrigido o problema em que o atalho da bola flutuante não conseguia traduzir no iOS 18.
- Corrigido o problema em que Prompts personalizados eram ineficazes quando muitos eram usados.

## 1.6.1

- Suporta a plataforma de modelo grande Baidu Qianfan, a plataforma de modelo grande Alibaba Bailian, a plataforma de modelo grande DeepSeek.
- Corrigido o problema em que modificar o idioma de destino e outras configurações no painel popup seria redefinido ao clicar na bola flutuante de tradução.

## 1.5.8

- Especialistas em IA suportam o modo "Seleção Inteligente", onde o sistema selecionará automaticamente o especialista em IA mais adequado com base no site atual (por exemplo, especialistas em IA relacionados à tecnologia serão automaticamente selecionados para The Verge e Hacker News, enquanto a melhoria de tradução do Twitter será automaticamente selecionada para o Twitter).

## 1.5.7

- Suporte para adicionar serviços de tradução por IA personalizados compatíveis com OpenAI, acessível na parte inferior da página [Configurações]->[Serviços de Tradução].
- Corrigido um problema em que legendas bilíngues não funcionavam na plataforma de vídeo Domestika no Safari.

## 1.5.6

- Otimização significativa do desempenho de tradução de grandes páginas web, criação de ePub e arquivos de legendas.
- Corrigido o bug de sincronização multi-dispositivo no Pro.

## 1.5.4

- Membros Pro suportam serviços de tradução Claude e Gemini prontos para uso (Beta)
- Legendas bilíngues do YouTube suportam configurações de fonte e peso da fonte
- Corrigido problemas de limite de palavras ao quebrar longos parágrafos [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Corrigido reconhecimento de idiomas japonês e coreano
- Corrigido problema em que páginas do Reddit em dispositivos móveis não eram traduzidas ao rolar
- Corrigido algumas páginas faltando traduções com DeepL
- Corrigido tempo de sincronização multi-dispositivo de usuários Pro não sincronizando
- Otimizado problemas de cobertura de configuração de sincronização em nuvem
- Otimizado palavras de prompt para serviços de tradução por IA

## 1.5.2

- Corrigido o problema em que alterações no prompt geral do especialista sobrepunham o prompt do especialista em IA especificado [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- Nome de modelo personalizado de IA suporta sintaxe avançada, use + para adicionar um modelo, use - para ocultar um modelo, e use model_name=display_name para personalizar o nome de exibição do modelo, por exemplo: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Corrigir o erro retornado por Gemini
- Ocultar a bola flutuante ao imprimir a página
- Corrigir o tamanho da fonte não escalando proporcionalmente quando o YouTube está em tela cheia [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Suporte para serviços de tradução por IA para definir [Especialista em IA] para especificar a estratégia de tradução, atualmente um recurso Beta, que pode ser ativado em [Configurações de Desenvolvedor](https://dash.immersivetranslate.com/#developer) após ativar o Beta, e o menu [Especialista em IA] pode ser visto após atualizar.
- Serviços de tradução por IA agora podem personalizar a lista de modelos, como [OpenAI], o sistema só tem alguns dos modelos mais comumente usados embutidos. Clicando na lista suspensa de modelos, o último item que você vê é [Definir Mais Modelos], após a configuração, será automaticamente lembrado para a conveniência dos usuários testarem diferentes modelos personalizados.
- Otimizada a inconsistência no layout das traduções em alguns casos.
- Adicionado um botão de reset para o estilo de legendas do Youtube, que pode rapidamente restaurar para o estilo padrão.
- Corrigido o problema em que legendas em chinês não podiam ser baixadas no Youtube.
- Otimizada a cópia da interface em Chinês Tradicional.

## 1.4.12

- Corrigido o problema de caixa de diálogo de mensagem não traduzida ao abrir página do reddit
- Adicionada uma funcionalidade temporária para habilitar a edição de tradução na entrada "Mais" do painel
- Corrigido o problema em que YouTube Shorts sem legendas sempre exibe legendas do vídeo anterior [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Corrigido o problema em que legendas bilíngues do YouTube não podiam ser ajustadas para cima e para baixo em tela cheia [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Suporte para [VK Video](https://vk.com/video) legendas bilíngues
- Suporte para configurações de ativação independente para legendas bilíngues de vídeo do YouTube (ativado por padrão para novos usuários)
- Otimizados prompts de erro para tradução de legendas bilíngues locais

## 1.4.11

- Compatível com tradução de caixa de entrada de página Bing Copilot
- Controle de estilo de legendas do YouTube suporta estilização de borda
- Suporte para selecionar o serviço de tradução padrão na página Configurações -> Serviço de Tradução
- Corrigido substituição de placeholder do OpenAI SystemPrompt
- Corrigido problema de mesclagem de regra de usuário personalizada
- Corrigido exibição anormal de legendas para alguns vídeos da Netflix [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Corrigido o problema em que mudanças frequentes na cor da tradução através da paleta de cores eram ineficazes [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Os serviços de tradução agora estão organizados de forma distinta sob uma aba separada, permitindo uma visão abrangente de todos os serviços de tradução disponíveis. Além disso, os usuários têm a flexibilidade de personalizar quais serviços de tradução são exibidos. Por padrão, apenas uma seleção limitada de serviços de tradução é mostrada, mas os usuários podem personalizar suas preferências de exibição na seção [Mais Serviços](https://dash.immersivetranslate.com/#services).
- A página de configurações agora acomoda ajustes para [estilos de legendas do YouTube](https://dash.immersivetranslate.com/#subtitle).
- Melhorias foram feitas para resolver o problema em que legendas bilíngues imersivas não eram exibidas quando os usuários definiam o idioma das legendas para Chinês no site do YouTube.
- Um novo atalho foi introduzido para tradução temporária chamada Claude, que pode ser configurada na [página de Configurações de Atalho](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Otimizar o desempenho de tradução para arquivos grandes em PDF-Pro
- Melhorar o desempenho de tradução para páginas de conteúdo longo
- Implementar suporte à internacionalização (i18n) para navegação de documentos de página
- YouTube introduz uma funcionalidade para habilitar temporariamente legendas bilíngues
- YouTube suporta o download de legendas bilíngues (apenas para membros)
- Móvel adiciona controle de gestos, melhorando a entrada via [configurações de atalho](https://dash.immersivetranslate.com/#shortcuts)
- Suporte para tradução bilíngue para Google Docs

## 1.4.7

- Corrigido o problema em que a tradução falhava ao alternar palavras de prompt personalizadas do OpenAI sob o botão de teste
- Corrigido o problema do ícone de atalho de legendas do YouTube não exibindo
- Otimizada a detecção de idioma da extensão

## 1.4.6

- Corrigido o problema em que palavras de prompt definidas pelo usuário eram ineficazes
- Adicionadas opções de 50%, 150% para o tamanho da fonte das legendas do Youtube

## 1.4.5

- Corrigido o problema em que alterações nos estilos de legendas do Youtube não eram salvas
- Corrigido o desaparecimento de legendas em tela cheia no iOS Safari
- Otimizada ainda mais a velocidade de tradução das legendas do Youtube
- As mais opções do painel agora suportam [entrada de tradução de texto](https://app.immersivetranslate.com/text/)

## 1.4.2

- Suporte para serviço de tradução Claude
- Otimizado multi-prompt words do OpenAI, suportando formato YAML, o que melhora a flexibilidade e facilidade de uso da configuração
- Otimizada significativamente a velocidade de tradução das legendas do Youtube, e adicionou suporte para alternar entre ordem Chinês e Inglês, personalizar cor e tamanho da fonte, etc.
- Plataforma de legendas de vídeo suporta [Universidade de Southampton](https://southampton.cloud.panopto.eu)
- Legendas bilíngues do Udemy compatíveis com exibição móvel
- Serviço de tradução Gemini é oculto por padrão, pode ser ativado nas configurações de desenvolvedor para mostrar beta deste serviço de tradução

## 1.3.4

- Suporte para serviço de tradução gratuito Yandex
- Otimizadas palavras de prompt do Gemini
- Legendas de vídeo suportam configuração para exibição bilíngue/original e tradução
- Suporte para espaço entre Chinês e Inglês nos resultados de tradução do OpenAI
- Alternância do painel para exibir apenas o botão de tradução modificado para ter efeito apenas na página atual

## 1.3.3

- Otimizado o problema de exibição de legendas de vídeo CC do Twitter.
- O serviço DeepL adicionou suporte para Árabe.
- O serviço de tradução Colorful Clouds agora suporta Coreano, Espanhol, Francês e Russo.
- O serviço OpenAI adicionou suporte para o dialeto do Nordeste da China.
- A detecção automática do painel agora exibe o idioma original.
- Ajustada a descrição do atalho para o painel móvel.

## 1.3.2

- Corrigido o problema em que o painel de controle não podia ser fechado em dispositivos móveis

## 1.3.1

- Suporte para plataforma de legendas de vídeo [DeepLearning.ai](https://learn.deeplearning.ai)
- Suporte para tradução de páginas web e legendas de vídeo em idiomas como Árabe, Hebraico, etc., abordando problemas de exibição RTL (Right-To-Left)
- Corrigida a tradução de Gemini para Hebraico
- Corrigido um problema em que algumas legendas em Chinês Tradicional no YouTube não podiam ser exibidas corretamente
- Corrigido o problema de exibição de legendas do Twitter no Safari
- Corrigido o atalho para tradução imediata para o final da página

## 1.2.4

- Corrigido o problema em que os espaços reservados na criação de ePub não eram substituídos corretamente
- Suporte para tradução de legendas de vídeo [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Otimizado o controle de frequência das solicitações de serviço de tradução
- Recentemente, as solicitações de serviço de tradução da Microsoft a partir da China têm sido instáveis; quando ocorrem erros, o sistema detecta automaticamente o serviço de tradução atualmente disponível, permitindo que os usuários mudem rapidamente.
- Otimizada a mensagem de erro para erros de rede
- Corrigido o problema em que configurar a cor do texto não suportava a pré-visualização RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Corrigido o problema em que a atualização da versão do plugin Safari sempre exibia a página de sucesso de instalação
- A Microsoft adicionou suporte para Vietnamita
- Corrigido o problema em que legendas traduzidas no site edx não eram exibidas

## 1.2.2

- Suporte para tradução de legendas de vídeo para [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Também suporta a tradução de alguns vídeos legendados em CC no Twitter.
- Otimizados os pop-ups de erro, os pop-ups de erro de problema de rede detectam automaticamente serviços de tradução gratuitos válidos.
- Corrigido o suporte do aplicativo iOS imersivo para reprodução em tela cheia do YouTube.
- Corrigido o problema de tradução de parágrafos com Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Suporte para tradução de legendas de vídeo para [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Corrigido um problema em que alguns usuários Pro não podiam modificar configurações no navegador Chrome.
- Suporte para exibição de legendas bilíngues no modo de tela cheia do YouTube no iOS.

## 1.2.0

- Suporte para tradução de legendas de vídeo nas plataformas [LinkedIn](https://www.linkedin.com/) e [Viu](https://www.viu.com/).
- Adicionado mais acesso rápido a legendas de vídeo para plataformas adicionais.
- Suporte para definir sites/idiomas específicos para exibir apenas o texto traduzido.
- Corrigido um problema em que a página de configurações continuava mostrando carregamento em alguns casos no Safari.
- Suporte para traduzir nós de tag de entrada.
- Otimizada a interface do usuário do pop-up de erro.

## 1.1.9

- Suporte para tradução de legendas para YouTube Live e a plataforma [Mubi](https://mubi.com/).
- Otimização: Página de configurações, interação da interface do usuário da lista de URLs (para evitar ambiguidades, as caixas de seleção não são exibidas por padrão).
- Suporte para definir a fonte de tradução no modo de tradução apenas.
- Adicionado acesso rápido para habilitar legendas de vídeo na Netflix, Ted, Bloomberg, Udemy, Coursera.
- Corrigido: Alguns estilos traduzidos (como sublinhados) não eram eficazes no Safari.
- Corrigido: Durante a tradução de página, o problema em que passar o mouse não acionava a retradução.

## 1.1.8

- Adicionada uma opção para o serviço de tradução secundário seguir o serviço de tradução principal
- Suporte para legendas bilíngues para [Amazon Prime Video](https://www.primevideo.com)
- Otimização adicional da função de tradução de PDF incorporado no Sci-Hub
- Corrigido um problema com PDFs online não abrindo corretamente
- Corrigido o problema com a reprodução contínua de legendas bilíngues na Netflix

## 1.1.7

- Agora você pode especificar uma fonte para a tradução na página de configurações -> [Configurações Básicas] -> [Estilo de Tradução]
- Adicionada uma configuração de atalho para [Traduzir Parágrafo Especificado] no painel de bola flutuante em dispositivos móveis
- Otimizada a sensibilidade de detectar o mouse pairando sobre Ctrl para evitar confundir `Ctrl+C` como `Ctrl`
- Adicionado suporte para uma nova configuração de atalho que permite alternar rapidamente se as legendas de vídeo usam as legendas de tradução automática incorporadas
- No site Sci-Hub, clicar na bola flutuante traduzirá PDFs incorporados na página web

## 1.1.6

- **Suporte Móvel para Tradução de Parágrafos Específicos:** A versão móvel agora suporta a tradução de parágrafos especificados e adicionou uma variedade de operações de atalho, incluindo deslizar para a esquerda, deslizar para a direita, toque duplo, toque triplo e gestos de toque com vários dedos. Estes não estão ativados por padrão e exigem que o usuário selecione ativamente o gesto de ativação na página de configurações em [Mouse Hover].
- **Atualização da Versão Padrão do Gemini:** A versão padrão agora é `v1beta`.
- **Correção de Tradução de Chinês Clássico:** Corrigida a funcionalidade de tradução de Chinês Clássico da Microsoft e OpenAI.
- **Otimização da Tradução Japonesa:** Otimizada ainda mais a tradução japonesa do OpenAI para melhorar a precisão e fluência.
- **Experiência de Tradução Imersiva:** Para melhor se adaptar aos hábitos dos usuários, movemos o atalho para legendas bilíngues no modo de tela cheia na plataforma YouTube para o lado esquerdo.

## 1.1.5

- Corrigido o problema em que o menu suspenso no modo escuro no Windows não tinha cor.
- Corrigido o problema de alinhamento com a opção "Mais" não sendo alinhada à esquerda no Windows.

## 1.1.4

- **Atualização da Interface do Usuário do Painel de Pop-up:** O novo design visa melhorar a usabilidade e a compreensão. Esta atualização inclui:

  - **Novos recursos no menu principal:**
    - **Alternância de modo bilíngue/somente tradução:** Agora você pode alternar entre "Modo de Tradução Bilíngue" e "Modo Somente Tradução" diretamente no menu principal, localizado à esquerda do botão de tradução.
    - **Entrada de tradução de documentos:** A entrada para traduzir "arquivos PDF/ePub/legendas" foi movida para o menu principal para acesso rápido.
    - **Configurações de tradução de vídeo:** A entrada para configurações de "Tradução de Vídeo" também foi colocada no menu principal para ajustes rápidos.
    - **Nova entrada para documentação de uso:** Fornece guias de operação detalhados e documentos de ajuda.

- **Entrada de tradução de documentos integrada:** Agora, você pode traduzir arquivos PDF, ePub e legendas através de uma entrada de upload unificada. Basta clicar no botão [PDF/ePub] no painel de pop-up, não é mais necessário selecionar [Mais].

- **Adicionado suporte para 5 sites de vídeo:**
  - Suporte para legendas de podcasts no Youtube Music.
  - Adicionado suporte para o site iview.abc.net.au.
  - Adicionado suporte para o site www.nma.art.
  - Adicionado suporte para o site creativecloud.adobe.com.
  - Adicionado suporte para o site www.masterclass.com.

## 1.1.3

- Corrigido o problema de anomalia de exibição do plugin móvel ao abrir páginas PDF.
- Otimizado o efeito de tradução de conversas GPT.
- Suporte para tradução de domínio para Baidu Translate.
- Adicionado um modo somente tradução na página de configurações.
- Adicionada uma função de lembrete ao alternar modos de tradução com atalhos.
- Corrigido o problema em que traduzir campos de entrada contendo URLs apenas traduzia partes do conteúdo.

## 1.1.2

- Correção: O problema em que alternar serviços de tradução não surtia efeito quando a página ainda não havia sido traduzida.
- Otimização: No processo de tradução de Epub e PDF, se algum conteúdo falhar na tradução, agora é possível alternar para outro serviço de tradução no painel sem reiniciar todo o processo de tradução (a lógica anterior era usar imediatamente um novo serviço de tradução para retraduzir todo o livro). Isso significa que, no meio da tradução, você pode mudar para um serviço de tradução diferente e clicar em [Tentar Novamente Todos os Parágrafos Falhados], após o qual o sistema continuará a tradução usando o novo serviço.
- Otimização: Ajustado o tamanho da fonte dos avisos de erro de tradução para melhorar a legibilidade.

## 1.1.1

- Corrigido o problema do atalho de legendas bilíngues para YouTube ter texto em inglês excessivamente longo.

## 1.1.0

### Novos Recursos

- **Configurações de Teclas de Atalho**: Adicionado um novo menu de nível superior "Atalhos" e as seguintes funções de teclas de atalho personalizáveis:

  - Designar uma combinação de teclas para traduzir o conteúdo da caixa de entrada atual, complementando o método anterior de pressionar rapidamente a barra de espaço três vezes.
  - Designar uma combinação de teclas para habilitar temporariamente "tradução direta ao passar o mouse" na página. Pressioná-la novamente cancelará esta função.
  - Adicionadas teclas de atalho dedicadas para 6 serviços de tradução (como DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) para facilitar a troca temporária entre serviços de tradução.

- **Atualização da Página de Configurações do Plugin**:

  - Em "Configurações Avançadas", uma nova opção foi adicionada para permitir que os usuários especifiquem certas palavras (por exemplo, "LLM") a serem excluídas da tradução.
  - Em "Configurações Avançadas", uma nova opção foi adicionada para configurar o número mínimo de caracteres necessários para traduzir um parágrafo. O padrão é 4 caracteres, mas pode ser configurado para um valor maior (por exemplo, 20), para que apenas parágrafos mais longos sejam traduzidos.
  - Adicionado um tutorial para iniciantes, cobrindo configurações de bola flutuante, configurações de legendas de vídeo e configurações de passar o mouse.

- **Legendas Bilíngues do YouTube**: Adicionado um acesso rápido na janela de reprodução de vídeo do YouTube para habilitar ou ocultar legendas bilíngues (este recurso pode ser desativado).

- **Suporte de Idioma do Deepl**: Adicionado suporte para Português (Brasil).

- **Novo Guia do Usuário**: Quando novos usuários abrem uma página em um idioma não-alvo pela primeira vez, uma bolha de ajuda da bola flutuante é exibida.

### Otimização e Correções

- **Otimização da Interface do Usuário**: Redesenhada a interface do usuário para avisos de erro de tradução de página para torná-los mais fáceis de entender. Quando há muitos erros, um pop-up irá ativamente avisar o usuário.

- **Correções de Bugs**:

- Corrigido o problema em que a tradução ao passar o mouse falhava quando a página perdia o foco.
- Corrigido o problema em que menos de 3 caracteres na funcionalidade de aprimoramento da caixa de entrada não eram traduzidos.
- Corrigido o problema em que alguns diretórios não eram traduzidos durante a produção de Epubs bilíngues.

- **Remoção de Funcionalidade**: Removida a funcionalidade de aprimoramento de informações bilíngues (exibindo resultados de pesquisa em inglês nas páginas de pesquisa do Google simultaneamente).

### Outras Atualizações

- **Atualização de Configuração do openAI**: Agora suporta a definição do número de configurações por segundo em decimais, como 0.5, significando 1 solicitação a cada 2 segundos.

## 0.12.14

- Correção: O problema de reconhecimento do idioma alvo padrão em algumas máquinas após a primeira instalação.
- Otimização: A ordem padrão dos títulos das páginas web foi alterada para [Chinês - Inglês].

## 0.12.13

- Corrigido: Problema com a costura de tradução de parágrafos longos do OpenAI em alguns casos. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Otimizado: Ao usar o mouse hover, o problema em que perder o foco na página e depois reativar se torna ineficaz.
- Corrigido: O problema em que o cache ainda existe após modificar o prompt/modelo no OpenAI.

## 0.12.12

- Atualizado: Otimizado o painel pop-up, removendo algumas opções para o site atual.
- Otimizado: Melhorado o processo de fusão de legendas manuais.
- Otimizado: Definido automaticamente o idioma alvo com base no idioma do navegador.
- Adicionado: Suporte a legendas bilíngues para a plataforma de aprendizagem [ArtStation](https://www.artstation.com/learning) e [ZDF](https://www.zdf.de/).
- Corrigido: Resolvido o problema em que os títulos na página de lista do jstor não eram traduzidos [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Corrigido: Corrigido o problema em que apenas parte do conteúdo desaparecia no Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Adicionado suporte a legendas bilíngues para as plataformas [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/) e [Domestika](https://www.domestika.org).

## 0.12.10

- Corrigido o problema de autorização do domínio Gemini sob o script Tampermonkey.
- Suporte à tradução de legendas em tempo real para o Twitter Space.
- Para versões mais antigas do script Tampermonkey, agora foi adicionado um aviso de atualização na página de configurações.

## 0.12.9

- Adicionado suporte para tradução Gemini.
- Corrigido o problema em que as traduções não respondiam a tempo quando a página web era rolada para a posição do meio em alguns casos.
- Corrigido o bug em que a troca de legendas em alguns sites de vídeo fazia com que a tradução fosse exibida repetidamente.
- Corrigido o problema em que o mouse pairava para continuar traduzindo sem pressionar a tecla de atalho em alguns casos.
- No macOS, otimizado o nome de exibição do atalho do painel.

## 0.12.8

- Reparar as legendas originais do vídeo não são exibidas quando "O site atual está definido para nunca traduzir".
- Reparar o conflito com alguns plug-ins que causam retorno infinito da página.
- Reparar a não tradução de alguns parágrafos após ativar quebras de linha de parágrafos longos.
- Corrigido [Quando temporariamente ativando a tradução da página web por um longo tempo, clicar no painel [Sempre traduzir este site] não cancela a tradução sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Legendas bilíngues adicionadas para suportar as plataformas [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/).
- O hoverball agora está oculto por padrão quando o vídeo está em tela cheia.
- Corrigir o problema de clique trêmulo do painel de ação do hoverball da página do Firefox.
- Suporte para colaboração sob o site pubmed.ncbi.nlm.nih.gov e o plugin scholarscope.
- Corrigir o problema de tremor da página de tradução da caixa de entrada do Reddit.

## 0.12.6

- Corrigir o problema de que a tradução do YouTube/Web of Science etc. não é sensível ao alternar abas.
- Hoverball no celular agora suporta operação de longa pressão, pressão curta para traduzir, longa pressão para abrir o painel.
- Traduzir e-books bilíngues agora traduzirá o índice também.
- A funcionalidade de Aprimoramento de Pesquisa (algumas páginas de Pesquisa do Google exibem resultados de pesquisa bilíngues) agora não está ativada por padrão e será removida no próximo Release.

## 0.12.5

- Corrigir a criação de Epubs a partir do painel clicando em traduções que não funcionam.

## 0.12.4

- Quando você ativa legendas bilíngues no painel, ele primeiro atualizará a página automaticamente (para exibir legendas bilíngues com mais precisão), e alguns sites ainda exigem que os usuários cliquem manualmente no botão "CC" no site para ativar as legendas.
- Otimizar Grease Monkey, detecção de idioma do Safari.
- Fornece acesso rápido a versões bilíngues de todos os artigos no site de artigos [Arxiv](https://arxiv.org/abs/1910.06709).
- [Suporte ao hoverball configurado para ser fixado à esquerda #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Corrigir problema de exibição do Modo de Aprendizagem #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Ativar temporariamente a tradução da web por um tempo não cancela Sempre Traduzir #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Otimizar problemas de inicialização de arquivos PDF.

## 0.12.3

- Correção para a funcionalidade [desativar permanentemente legendas de vídeo] não funcionando [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175).

## 0.12.2

- Suporte a legendas bilíngues é fornecido para mais plataformas de vídeo, que agora são suportadas: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Note que devido a limitações técnicas, alguns sites precisam atualizar a página após ativar as legendas bilíngues pela primeira vez ou esperar a tradução ser concluída para exibir as legendas bilíngues).
- Otimizado significativamente o tamanho do arquivo zip do plugin, reduzido pela metade em comparação com o original, download e atualização mais rápidos.
- Corrigir problemas de download de PDF estendido.
- Adicionado um portal de tradução rápida de PDF ao lado direito do site de artigos [Arxiv](https://arxiv.org/abs/1910.06709), que leva a uma página HTML limpa (apenas suportada por alguns artigos, pois requer que os autores originais enviem o código-fonte, então aproximadamente 50% dos artigos mostrarão este portal).
- Páginas PDF online sem extensão .pdf agora podem pular diretamente para a página de tradução de PDF clicando no hoverball na página.
- Corrigir alguns problemas de aprimoramento da caixa de entrada no Safari.
- Otimizar a detecção de idioma no Grease Monkey e Safari.

## 0.11.6

- Adicionado 11 novos idiomas de interface para o plugin e o site oficial, agora os idiomas de interface suportados chegam a 14, incluindo Chinês Simplificado, Chinês Tradicional, Inglês, Japonês, Coreano, Russo, Espanhol, Português, Hindi, Italiano, Alemão, Francês, Árabe e Persa.
- Modificar o compartilhamento bilíngue (modo de atualização) adicionado na última versão para compartilhamento de instantâneos de página bilíngue, para que o conteúdo compartilhado seja mais original, bem como uma adaptabilidade mais ampla.
- Corrigir emoji no final da caixa de entrada do Twitter que não pode ser traduzido.
- Corrigir a situação em que o conteúdo de plug-ins de terceiros é traduzido em alguns cenários.
- Reparar clique no hoverball de pdf online sem resposta.

## 0.11.5

- Agora você pode gerar um link público para a página bilíngue traduzida para o Immersive Translate.
  - [Clique](/docs/share/) no ícone de compartilhamento do Immersive Translate para gerá-lo com um clique!
- Resolvido o problema de que algumas plataformas não conseguiam reconhecer se o mouse era suportado ou não.
  - Existem alguns navegadores de desktop que suportam tanto touchscreen quanto mouse, e o Immersive Translate tecnicamente não consegue detectar se tais plataformas suportam mouse, então adicionamos a opção [Forçar Ativar Suporte ao Mouse] na configuração [Mouse Hover].

## 0.11.2-0.11.4

- Otimizar experiência, corrigir alguns bugs.

## 0.11.1

- O modelo padrão para traduções OpenAI é: GPT3.5-turbo-1106.
- Otimizado o Prompt Chinês para OpenAI, agora menos propenso a alucinações!
- Reduzido o comprimento dos prompts do OpenAI de 90 para 40, economizando ainda mais tráfego.

## 0.11.0

- Corrigir cliques trêmulos do hoverball da página.
- Corrigir problemas de tradução do Azure.

## 0.10.9

- Corrigir alguns problemas menores.

## 0.10.8

- Suporte para configurar botões de tradução rápida do hoverball (suporte para PC/celular).
- Otimizar julgamento de idioma do Grease Monkey.
- Corrigir tradução de arquivo txt.

## 0.10.7

- Suporte ao mouse hover pressione Ctrl novamente para mostrar o texto original.
- Mouse Hover Ignorar Nunca Traduzir Idioma.
- Otimização de Legendas Bilíngues do Youtube.

## 0.10.6

- Suporte a legendas do Youtube apenas para traduções.
- Adicionar Alerta de Atualização de Versão Baixa do Grease Monkey.
- Corrigir o problema de que arquivos txt locais não podem ser traduzidos.

## 0.10.5

- Corrigir o Youtube ocasionalmente retornando à página inicial.

## 0.10.4

- Corrigir conflito de legendas do Youtube com o plugin de legendas duplas (tradução de legendas do Youtube do Immersive Translate não é ativada quando o plugin de legendas duplas do Youtube é detectado para evitar conflito).
- Adicionado [Função Desativar Permanentemente Legendas de Vídeo], se houver outros problemas de conflito e você não quiser ativar a função de legendas bilíngues com o Immersive Translate.
- Otimizar quebras de legendas.

## 0.10.3

- Corrigir problema de tradução da Chave de Autenticação Custom DeppL

## 0.10.3

- Suporte perfeito para vídeos do Youtube com legendas bilíngues 🎉.
- Para páginas de artigos, o texto principal será agora traduzido primeiro antes do resto do conteúdo da barra lateral
- Otimizar a Contextualização da Tradução DeepL
- Otimizar a tradução de arquivos de legendas do OpenAI para contextualização

## 0.10.1

- Aumentar a prioridade da tradução do corpo para otimizar a experiência de tradução
- Corrigir problema de texto não traduzido ao clicar em "mais" no ins

## 0.9.8

- Otimizar experiência, corrigir alguns bugs

## 0.9.7

- Corrigir tradução automática quando readwise está destacado

## 0.9.6

- Corrigido o problema de limpar o cache ao fazer logout do usuário.

## 0.9.5

- Correções de bugs em eBooks online

## 0.9.4

- Otimizar a detecção de aprimoramento de entrada para reduzir toques falsos
- Tradução de e-book e legendas online

## 0.9.3

- Tradução da Caixa de Entrada: exibe um lembrete pop-up quando usado pela primeira vez, e o usuário pode optar por desativá-lo desta vez ou permanentemente para evitar toques acidentais.
- Otimização da velocidade de exportação de tradução apenas para PDF, se você escolher exportar apenas a tradução, pode chamar diretamente a pré-visualização do sistema PDF para exportar, mais rápido.
- Deeplx suporta múltiplos URLs, basta separá-los com .

## 0.9.2

- A ferramenta de tradução de PDF foi migrada para a versão online: https://app.immersivetranslate.com/pdf/ , para que Grease Monkey e Safari possam usar a tradução de PDF, e os problemas podem ser melhor iterados sem a necessidade de emitir uma versão para resolver o problema.
- Otimização da UI POPUP, o painel está mais bonito!

## 0.9.1

- Corrigir problemas de nome de arquivo com criação de eBook Epub

## 0.8.8

- suporte a pdf para ajustes de espaçamento de linha e espaçamento de palavras para re-reconhecer parágrafos
- correção do problema de rolagem automática em leitura online de epub em dispositivos móveis

## 0.8.7

- suporte a pdf para downloads de tradução apenas
- Corrigir problema de login do Google no safari

## 0.8.2 - 0.8.6

- Permite definir o intervalo entre os gatilhos de combinação de aprimoramento de entrada
- Corrigir alguns bugs

## 0.8.1

- Otimização de Detecção de Idioma
- Funcionalidades Beta: API Customizada (Beta ativado nas configurações do desenvolvedor)
- Suporte para Tradução AliCloud
- Corrigido alguns bugs

## 0.8.0

- Sistemas de Usuário Suportados
- Suporta [Ativar Membro Pro](/pricing), que permite aos usuários desfrutar de traduções Deepl e OpenAI e configurações de sincronização em nuvem.
- Serviço de tradução ao passar o mouse pode ser configurado individualmente
- Serviço de tradução da caixa de entrada pode ser configurado separadamente
- Otimização de Tradução de PDF
- Corrigido alguns bugs

## 0.7.16

- Tradução de PDF com novas opções para controle rápido do estilo de tradução (arquivos PDF são muito estranhos e ativar essas opções pode ser útil para alguns arquivos PDF com formatação confusa)
- Versões iOS e macOS estão de volta na Apple Store Country Store

## 0.7.15

- Fomos notificados pela Apple que as Traduções OpenAI foram temporariamente removidas do iOS e macOS, e estamos tentando relançá-las na China.

## 0.7.11- 0.7.14

- Corrigir: problema de Tradução de Todas as Regiões do Gmail
- Desativar temporariamente a função de exportação de PDF do Safari devido à restrição do Safari sobre downloads de plug-ins (bug).
- Corrigir alguns outros problemas

## 0.7.10

- Atualização da UI do Painel de Ícones do Navegador Popup, um pouco mais de design ～
- Corrige o problema de que algumas passagens em japonês não são traduzidas.

## 0.7.9

- PDF finalmente suporta a exportação de versões bilíngues! Você pode clicar no botão [Salvar] para exportar o arquivo PDF bilíngue traduzido.
- Regras personalizadas agora suportam a fusão com as regras padrão embutidas, por exemplo: `{"id": "youtube", "selectors.add":["#test"]}` significa adicionar um `#test` aos seletores existentes, `selectors` significa substituir o padrão, `selectors.remove` significa excluir um dos seletores padrão, e `selectors.remove` significa excluir um dos seletores padrão.
- Ícone do Safari atualizado, um pouco maior.
- Outras Correções de Bugs

## 0.7.8

- Correções de Bugs

## 0.7.7

- Adaptado ao estilo do sistema do Safari, ícone de extensão do Safari alterado para contorno transparente.
- Adicionar mudança de status do ícone do navegador, quando uma página da web foi traduzida, um ✅ será adicionado automaticamente ao canto inferior direito do ícone do navegador.
- Ativar automaticamente a tradução de sites em inglês frequentemente usados para novos usuários
- Corrigir problemas de tradução com https://claude.ai/

## 0.7.6

- Suporte a Resultados de Tradução de Suporte Aprimorado de Entrada ctrl+z Desfazer
- Suporte a tradução no modo de leitura de documentos do Flying Book
- Adaptação https://pi.ai/talk

## 0.7.5

- Corrigir ícone do Grease Monkey não exibindo
- Corrigir vários problemas

## 0.7.4

- Corrigir vários problemas
- Página de configuração suporta exclusão em massa de URLs selecionados.
- Suporta ativar/desativar tradução de legendas do Youtube para evitar conflitos com outros plugins relacionados.
- Arigato Translator suporta configuração de campos e id de terminologia

## 0.7.2

- Aprimoramento da Caixa de Entrada: permite omitir o prefixo // e acionar a tradução de toda a caixa de entrada com 3 espaços, ou você pode desativar essa opção na página de configurações.

## 0.7.1

- Suporte a Aprimoramento de Pesquisa, quando ativado, ao pesquisar no Google/Google News em chinês, a coluna da direita mostrará automaticamente os resultados de pesquisa das palavras-chave correspondentes em inglês, que está ativado por padrão.
  - Razão: Descobrimos que na pesquisa do Google, os resultados de pesquisa para palavras-chave em chinês e palavras-chave em inglês podem ser muito diferentes, com o Aprimoramento de Pesquisa Traduzida Imersiva ativado, pesquisamos automaticamente as mesmas palavras-chave em inglês para você e as exibimos no lado direito. Você pode optar por desativá-lo se não precisar do recurso.
  - Safari não é suportado devido a limitações de API.

## 0.6.20

- Modificar as configurações padrão: Devido ao feedback de um grande número de usuários de que não usarão a ferramenta de tradução após a instalação, sua expectativa da ferramenta de tradução é que ela traduza automaticamente páginas da web em inglês após a instalação, então a partir desta versão, para usuários chineses, a opção de traduzir páginas em inglês por padrão foi ativada (se o usuário tiver uma configuração anterior do idioma que sempre será traduzido, então será respeitada, e a alteração apenas modifica as configurações iniciais da extensão), e precisa ser cancelada, pode ser facilmente cancelada no [Painel Popup ou página de configurações](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Corrigir Bugs de PDF
- Corrigir Bug da web of science
- Adaptação feeder.com
- Corrigir epub não traduzindo alguns livros

## 0.6.18

- Corrigir problema de estouro de largura do Popup do Safari.
- Otimização do Processo de Construção

## 0.6.17

- Otimizar alertas de erro
- Otimizar a seleção do idioma alvo, agora mostrará apenas os idiomas suportados pelo serviço de tradução correspondente
- Otimização de Tradução de PDF
- Adaptado para o site Good Reads, Amazon e South China Morning Post

## 0.6.16

- Adicionar exibição de página sem permissão de PDF
- Reparar a exibição de parágrafos da lista de texto de PDF
- Ampliar a escala de fonte pequena de PDF no chrome e safari

## 0.6.15

- Reparar o problema de que ao abrir arquivos PDF, o painel de extensão avisa que não há permissões.
- Corrigir o problema de que o aprimoramento da caixa de entrada não é ativado quando o site está configurado para nunca traduzir.

## 0.6.14

- Otimização de tradução de PDF, a área de tradução agora pode ser editada/arrastada/excluída
  - Arrastar no canto superior esquerdo, excluir no canto superior direito, mudar tamanho no canto inferior direito
- Alinhamento à esquerda da Caixa de Suspensão do Windows
- Suporte a Chinês Tradicional e Chinês Simplificado

## 0.6.13

- Corrigir o problema de tradução repetida ao passar o mouse
- Suporte a tradução de PDF para arrastar para mudar o tamanho e editar o conteúdo da tradução

## 0.6.12

- Corrige imagens de tradução de Epub ficando menores em alguns navegadores
- Tradução da caixa de entrada otimizada, agora funciona suavemente no Bard!

## 0.6.10

- Modelo padrão do OpenAI alterado para a versão 0613
- Corrigir alguns estilos de caixa de entrada
- Mais inteligente para determinar se é uma área de navegação, e se for, nenhuma tradução é realizada
- Corrigir possíveis ataques de injeção XSS

## 0.6.8

- O painel de extensão agora pode indicar páginas não suportadas (por exemplo, páginas sem permissões e páginas não-HTML)
- Aprimoramento da caixa de entrada para mostrar status de Carregamento na tradução
- Atualizar cores de carregamento padrão nas traduções
- Quando a caixa de entrada é configurada sem prefixo, suporta tradução `ja Hello` para japonês e `English Hello` para inglês.

## 0.6.6

- Correção para: algumas áreas não traduzindo (quora)

## 0.6.5

- Otimização do Google Bard
- Tradução da Caixa de Entrada suporta tradução direta de toda a caixa de texto sem prefixos.
- Otimizar o problema de traduções do OpenAI adicionando pontos sem sentido, (se nenhum ponto for detectado no texto original, se o openai retornar um ponto, então removê-lo)
- Problemas com arquivos de legendas do safari não sendo reconhecidos

## 0.6.3

O idioma padrão para tradução da caixa de entrada agora pode omitir o espaço, ou seja, //Hello World pode ser traduzido também.

## 0.6.2

O aprimoramento mais emocionante da caixa de entrada está aqui:

- Digite: // Hello World na caixa de entrada em qualquer página da web, depois clique três vezes na barra de espaço para traduzir o parágrafo para o inglês
- Você também pode especificar a tradução para um determinado idioma: /ja Hello World, depois clique três vezes na barra de espaço para traduzir o parágrafo para o japonês

[Clique aqui para uma introdução rápida de 30 segundos](/docs/input/)

## 0.6.0

- Primeiro lançamento em junho, migrado do subdomínio pessoal anterior https://immersive-translate.owenyoung.com para o novo domínio https://immersivetranslate.com/
- Funcionalidade é em grande parte inalterada (novos recursos estarão disponíveis no próximo lançamento!)

## 0.5.17

- Corrigir o problema de que: eBooks bilíngues não têm imagens após a exportação

## 0.5.16

- Corrigir: problema de tradução openai em Chinês Tradicional

## 0.5.15

- Otimizar: O número mínimo de caracteres em um parágrafo que aciona a tradução foi modificado para um mínimo de 4 caracteres para reduzir a confusão, enquanto usa outros recursos para evitar traduzir as áreas de navegação e fim do site.
- Corrigir: Detalhes do Github não traduzindo após a expansão.

## 0.5.14

- Corrigir o problema de que as imagens em algumas páginas web de: ficam maiores após a cópia
- Corrigir: seção de comentários do medium não traduzindo
- Corrigido o problema de que as imagens em algumas páginas de: foram copiadas incorretamente

## 0.5.12

- Funcionalidade: Estilo de Tradução de Linha Dividida adiciona uma linha de divisão vertical para traduções de linha única
- Corrigir: Casos muito raros de divisão de parágrafos.
- Uma excelente página de orientação para configuração inicial para novos utilizadores de iOS.

## 0.5.11

- Suporte à tradução de legendas apenas para exportar traduções
- Corrigir: Alguns elementos não são reconhecidos ao passar o mouse
- Corrigir: quebras de linha parciais em tweets não reconhecidas
- Corrigir: estilo de autoria de eBook não funcionando

## 0.5.10

- Corrigir: quebras de linha em tweets não reconhecidas
- Corrigir: página de detalhes do Reddit retorna alguns parágrafos que não podem ser traduzidos
- Corrigido um problema com: onde algumas das tags de Código não foram reconhecidas corretamente.

## 0.5.9

- Corrigir quebras de parágrafo em alguns casos em:
- Corrigir: Tampermonkey Toggle Only Shows Translations
- Corrigir: problema de estilo de leitura online de eBook não funcionando

## 0.5.8

- Corrigir o problema de que: a configuração temporária da duração da tradução do site não tem efeito.

## 0.5.7

- Super atualização!

- A funcionalidade Mostrar Apenas Traduções chegou! Clique em [Mais] -> [Alternar para mostrar apenas traduções].

  - Suporte a atalhos personalizados, configurados em configurações de interface -> Configurações de Atalho

- Otimizar a limitação de frequência de solicitações do OpenAI

- ChatGPT por padrão no modelo móvel, que é mais rápido!

- Reestruturação da análise do núcleo da web, o que significa:

  - Tradução de páginas web em grande escala em segundos
    - Por exemplo,: https://pve.proxmox.com/pve-docs/pve-admin-guide.html, que antes levava 30 segundos, agora é traduzido em segundos.
  - Uso de memória ultra-baixo para páginas web complexas
    - Por exemplo: https://www\.wsj.com/articles/global-stocks-markets-dow-news-05-05-2023-cb142c76?mod=hp_lead_pos1
  - Adaptação a mais sites

- Todas as traduções do site ShadowRoot são suportadas.

  - Por exemplo: https://bugs.chromium.org/p/chromium/issues/detail?id=418987
  - Por exemplo, a seção de comentários de: https://news.yahoo.com/gma/virginia-mom-facing-charges-6-190600893.html

- Corrigir o problema de tela branca após a tradução de sites com hidratação, como Next.js.

  - Por exemplo: https://webpack.js.org/

- Corrigido o problema de que modificar o atalho de passar o mouse precisava atualizar a página para ter efeito

- Corrigido um problema com o reconhecimento de quebras de linha em arquivos TXT.

- Muitas atualizações!

- A funcionalidade 'Mostrar Apenas Tradução' chegou! Clique em 'Mais' -> 'Alternar para Mostrar Apenas Traduções'.

  - Suporta atalhos personalizados, que podem ser configurados em 'Configurações de Interface' -> 'Configurações de Atalho'

- Otimizado para o problema de limite de taxa de solicitação do OpenAI

- A análise do núcleo da web foi reconstruída, o que significa.

  - Tradução instantânea para grandes sites
  - Uso mínimo de memória para páginas web complexas
  - Melhor compatibilidade com mais sites

- Agora suporta traduções para todos os sites com ShadowRoot.

- Corrigido o problema de tela branca após traduzir sites com hidratação, como Next.js

- Corrigido o problema em que mudar o atalho de passar o mouse exigia uma atualização da página para ter efeito

- Corrigido o problema com o reconhecimento de quebras de linha em arquivos TXT.

## 0.5.6

- Corrigir: problema de pop-up de nova aba no macOS.
- Funcionalidade: Nova página de guia para novos utilizadores.

## 0.5.5

- Corrigir: problema de área de passar o mouse.

## 0.5.4

- Corrigir: Página Spa duplicada

## 0.5.3

- Corrigir: ouvinte de tecla de atalho de passar o mouse.
- Corrigir: tradução de documento PDF
- Funcionalidade: Adicionar nova página de guia do cliente

## 0.5.2

- Corrigir: configurações de atalhos de passar o mouse do userscript

## 0.5.1

- Corrigir: OpenAI API não funciona.

## 0.5.0

- Funcionalidade: Traduzir o parágrafo atual ao passar o mouse.
- Funcionalidade: Refatorar tradução de PDF, agora você pode traduzir a maioria dos PDFs com Immersive Translate
- Corrigir: Desativar Menu de Contexto não funcionando [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Corrigir: Evitar Content Security Policy para [Mastondon](https://mastodon.social/)

## 0.4.11

- Corrigir: permissão de userscript (apenas para userscript).

## 0.4.8

- Funcionalidade: Bing Translate para Microsoft Translate para uma qualidade mais estável.
- Corrigir: Página web TXT pura como [esta](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Desempenho: Excluir algumas páginas de publicidade infantil no site, e o desempenho melhorou um pouco

## 0.4.7

- Corrigir: pop-up de Userscript do Firefox ausente.

## 0.4.6

- Funcionalidade: Permitir que terceiros enviem evento de documento para chamar `toggleTranslatePage`
- Funcionalidade: aplicativo iOS adiciona botão de ativar extensão e link de comunidades
- UI: modelo de campo de configurações do OpenAI usa seleção em vez de caixa de entrada de texto.

## 0.4.5

- Corrigir: problema de extensão do safari no iOS 15.0.
- Corrigir: atalhos de extensão do safari no macOS
- Corrigir: pop-up de política de segurança de conteúdo para extensão, e parcialmente para userscript.

## 0.4.4

- Tarefa: Remover console.log

## 0.4.3

- Corrigir: detecção de espaço em branco de tag sup, sub.
- Funcionalidade: suporte ao ChatGPT Plus Website como Serviço de Tradução, Esta é uma funcionalidade beta, então você pode acessá-la ativando a Funcionalidade Beta nas configurações de desenvolvedor. Isso é muito lento, pois o chatgpt só pode enviar uma solicitação de cada vez. Certifique-se de ter uma Conta ChatGPT Plus, pois há mais limites na Conta Gratuita, e não tenho certeza se isso traz risco para sua conta, tenha cuidado para Certifique-se de ter uma Conta ChatGPT Plus, pois há mais limites na Conta Gratuita, e não tenho certeza se isso traz risco para sua conta, tenha cuidado ao usá-la.

## 0.4.1

- Corrigir: menu de contexto do firefox desapareceu após reiniciar.
- Suporte ao Azure openai

## 0.4.0

- Funcionalidade: Suporte a Tradução de Arquivo de Legenda Local (.srt,.ass,etc.)

## 0.3.17

- Funcionalidade: Suporte a tradução de arquivo .txt local.
- Corrigir: Menu de Contexto pode não estar disponível às vezes. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Corrigir: manter &nbsp; como espaço em branco.
- Remover: Remover Papago, pois [o serviço está fora do ar](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: permitir sem chave de API para openai
- UI: permitir que o Open AI redefina para as configurações padrão

## 0.3.14

- Dependência: Atualizar pdf.js para a versão mais recente
- Corrigir: cor de fundo da seleção de pdf
- Corrigir: detecção de espaço em branco

## 0.3.13

- Corrigir: problema de caractere específico do construtor de ebook, como alguns caminhos de capítulo são `xxx' xxxx`.
- UI: dobrar opções personalizadas do openai por padrão.
- UI: Adicionar status de exportação para exportação de epub.
- Corrigir: prompt padrão do Gpt4

## 0.3.12

- Funcionalidade: Agora podemos personalizar a cor de fundo do tema de tradução do Marcador.
- Corrigir: postMessage quando a página inicial quebrou alguns sites, agora faremos isso apenas quando realmente traduzirmos páginas
- Corrigir: problema de progresso do ebook.
- Corrigir: melhor para dividir parágrafo longo, 1.5 bilhões, 25.5%, Sr. não será considerado como um limite

## 0.3.11

- Corrigir: cor do texto no modo escuro do leitor de ebook
- Corrigir: prompt do openAI

## 0.3.10

- Melhor: detectar contêiner japonês/coreano.
- Corrigir: Progresso do Construtor de Ebook 99% parado.

## 0.3.9

- Corrigir: estado de entrada de serviços de tradução de switch UI de Opções não alterado.

## 0.3.8

- UI: cor de carregamento mais transparente
- Corrigir: Detectar Idioma do Ebook.
- Funcionalidade: Adicionar progresso de tradução para o construtor de ebook, e um belo confete após o sucesso.
- Funcionalidade: Adicionar botão de tentar novamente todos os parágrafos falhados.
- Corrigir: Manipulação de Erro do Deepl

## 0.3.7

- Corrigir: leitor de ebook não pode carregar imagens no Chrome.

## 0.3.6

- UI: melhor para fazer UI de página de ebook

## 0.3.5

- Corrigir: exportação de ebook de userscript
- Funcionalidade: adicionar endpoint de API personalizado para OpenAI
- Funcionalidade: adicionar opções de tempo de tradução temporária do site em `Configurações Avançadas`

## 0.3.4

- CI: Build falhou

## 0.3.3

- Corrigir: criador de ebook para Kindle
- Alterar: Cor do ícone de carregamento, de preto para azul, para adaptar a página web em modo escuro.
- Funcionalidade: Suporte a tradução de html local para extensão

## 0.3.2

- Corrigir: Movimento do cursor de entrada do Formulário de Opções.
- Funcionalidade: OpenAI suporta apiUrl personalizado para configurações de desenvolvimento.

## 0.3.1

- Funcionalidade: atualizar ícone escuro para transparência.
- Corrigir: Ordem errada para parágrafo longo

## 0.3.0

- Versão: A partir de agora, mudaremos o número da versão menor uma vez por mês, por exemplo, agora em março, a versão começará a partir de 0.3.0, em abril, o número da versão começará a partir de 0.3.0, em abril, o número da versão começará a partir de 0.4.0, no próximo abril, o número da versão será 1.4.0, e assim por diante. Isso ocorre porque não faz sentido para extensões seguir Isso ocorre porque não faz sentido para extensões seguir semântica, mas padronizar números de versão de acordo com as leis do tempo é motivação para o desenvolvimento continuar atualizando, e para os utilizadores encontrarem problemas mais facilmente.
- Funcionalidade: Suporte a ícone escuro para firefox

## 0.2.86

- Adicionar opção de comprimento máximo de texto por solicitação com Open AI
- Corrigir: identificador de ebook duplicado
- Funcionalidade: Suporte a tradução de página web txt

## 0.2.85

- Corrigir: alguns arquivos epub não podem ser encontrados.

## 0.2.84

- Funcionalidade: Suporte a Leitor e Criador de Ebook

## 0.2.83

- Funcionalidade: Permitir que o Formulário de entrada de senha mostre a senha.

## 0.2.82

## 0.2.81

- Corrigir: m.youtube.com
- Corrigir: interface do formulário de opções
- Corrigir: prompt do Open AI
- Funcionalidade: Suporte a múltiplas chaves OpenAI, use `,` para separá-las.

## 0.2.80

- Funcionalidade: Adicionar Menu Ativar/Desativar para popup -> mais
- Corrigir: Conflito de Mensagem do DingTalk

## 0.2.79

- Corrigir: Open AI para parágrafo com espaço

## 0.2.78

- Funcionalidade: suporte ao OpenAI CHATGPT 3.5 (suporta a interface OpenAI ChatGPT 3.5)
- Funcionalidade: Adicionar novo tema Solid Border (新增新主题，实线边框)

## 0.2.77

- Corrigir: erro de múltiplas tags de código.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Corrigir: erro de múltiplas tags de código [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Funcionalidade: Suporte a contagem de texto de tradução imediata personalizada para diferentes serviços de tradução.

## 0.2.74

- Funcionalidade: Suporte a Tencent (alpha)
- Corrigir: tradução openai
- Corrigir: verificação de tags desconhecidas inline

## 0.2.73

- Funcionalidade: Suporte ao Tema de Tradução Cinza
- Corrigir: Página de Tendências do Github

## 0.2.72

- Corrigir: problema de rede do serviço de tradução de verificação no firefox mobile.

## 0.2.71

- Corrigir: permissão do userscript Open AI

## 0.2.70

- Corrigir: placeholder do Open AI

## 0.2.69

- Funcionalidade: Suporte ao Open AI como serviço de tradução.
- Funcionalidade: Suporte à verificação do serviço de tradução em options.html
- Funcionalidade: Suporte a frame principal personalizado, pois alguns sites não usam o corpo como frame principal

## 0.2.68

- Suporte a Caiyun (Alpha)
- Corrigir tags de bloco desconhecidas

## 0.2.67

- Funcionalidade: Adicionar `<all>` para sempre traduzir idiomas, então agora você pode usá-lo para traduzir todos os idiomas, exceto o idioma alvo, e nunca traduzir idiomas
- Corrigir: Permitir configuração de API do Google personalizada
- Melhor: Suporte Deepl Free
- Corrigir: alto uso de memória para userscripts e extensão (removendo opencc zh-CN para zh-TW, em vez disso com Google translate)
- Corrigir: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Corrigir: configuração de tradução Azure, mas ainda mostra (necessário configurar)

## 0.2.66

- Corrigir: tradução de arquivo PDF falhou, Bug da versão 0.2.60 para suportar deepl de zh-CN para zh-TW

## 0.2.65

- Suporte a requisições limitadas para múltiplos frames
- Não traduzir título da página quando em iframe

## 0.2.64

- Corrigir: escolha de serviços de tradução openl
- Funcionalidade: Suporte à opção de traduzir título

## 0.2.63

- Funcionalidade: Suporte ao Serviço de Tradução Azure
- Funcionalidade: Suporte ao Serviço de Tradução Papago
- Corrigir: sincronização do google drive no firefox android nativo.
- Corrigir: mudar transparência de 0.4 para 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Corrigir: dicas de atalhos do popup
- Desempenho: requisições de serial para concorrência
- Melhor para detectar contagem de japonês

## 0.2.62

- Funcionalidade: Adicionar regra waitForSelectors, para corrigir alguns sites como reddit

## 0.2.61

- Corrigir: userscript é muito grande para greasy fork
- Melhor: reduzir tamanho do arquivo

## 0.2.60

- Funcionalidade: Suporte a zh-CN para zh-TW para Deepl
- Funcionalidade: Recurso Deepl de Tradução Imersiva
- Funcionalidade: Suporte a zoom de tamanho de fonte personalizado
- Corrigir: estilo do fórum Steam
- Corrigir: estilo global não alterado após elementos dinâmicos gerados
- Corrigir: promover prioridade de exclusão
- UI: mudança na página sobre
- Corrigir: alguns elementos matemáticos permanecem originais

## 0.2.59

- Corrigir: Elemento de Bloco de Tags Desconhecidas
- Corrigir: elemento translate=no sobreposto
- Corrigir: correspondência de URL com múltiplos \*

## 0.2.58

- Funcionalidade: Suporte a cor de texto de tradução personalizada, cor da borda.

## 0.2.57

- Sem alterações, reconstruir

## 0.2.56

- Corrigir tradução duplicada para elementos inline com elemento de código.
- Corrigir verificação de tags desconhecidas inline/bloco
- Funcionalidade: suporte a css injetado no painel de desenvolvedor
- Funcionalidade: aparar authKey, appid appSecret
- Melhor: abrir página de configurações em nova aba (mas não para Stay)

## 0.2.55

- Tentar corrigir charset da API deepl

## 0.2.54

- Remover permissão de abas para rejeição da loja do chrome
- Corrigir tradução da página inteira, rodapé é ignorado
- Adicionar notas à página sobre
- Suporte a URL personalizada da Configuração embutida

## 0.2.53

- Corrigir erro de sincronização do google drive no userscript.

## 0.2.52

### Código

- Usar a última versão do esbuild
- Usar a última versão do deno
- CI: enviar código-fonte para firefox

## 0.2.51

- Corrigir necessidade de login do Google Auth no Chrome/Firefox
- Substituir links de serviço de tradução
- Melhor para permissão.
- remover minify.

## 0.2.50

- Corrigir problema de upload do google drive (realmente) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Remover atalhos alt+d, alt+s pois podem conflitar com atalhos nativos.
- Corrigir problema de upload do google drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Melhor para velocidade, adicionando minLength para 50 para detecção de idioma.
- Corrigir validação de token do Google Drive.

## 0.2.47

- Corrigir API deepl

## 0.2.46

- corrigir marca de bloco

## 0.2.45

- Corrigir innerText do elemento é indefinido
- Corrigir tradução caiyun idioma de origem indefinido

## 0.2.44

- Corrigir alternância de máscara do userscript
- Corrigir lógica de alternância de máscara

## 0.2.43

- Corrigir alternância de máscara do userscript com evento de toque.
- Corrigir velocidade (removendo sleep(300))

## 0.2.42

- Corrigir hover de máscara ao alternar máscara novamente.
- Adicionar atalhos de máscara para mobile
- Corrigir problema de sincronização em nuvem do userscript
- Mover página de opções avançadas para o menu à esquerda.
- Adicionar lógica de tentativa ao serviço de tradução

## 0.2.41

- Corrigir tradução niu do userscript
- Corrigir tradução xhtml

## 0.2.40

- Corrigir exibição de recurso beta
- Corrigir página de configuração do popup em nova aba
- Corrigir substituição de placeholder de tradução

## 0.2.39

- Suporte a atalhos para mostrar tradução de máscara
- Suporte a ativar recurso beta no painel de desenvolvedor
- Corrigir atalhos na extensão mobile

## 0.2.38

- Suporte a tema de carregamento
- Corrigir getpocket.com
- Corrigir rodapé lateral para área do corpo
- Corrigir ícone de importação/exportação

## 0.2.37

- Corrigir marca de exclusão de frame

## 0.2.36

- Suporte a sincronização com o Google Drive

## 0.2.35

- Corrigir ignorar tag japonesa rb, rt.
- Melhor para interface do popup mais
- Melhor para dicas de userscript ruins
- Adicionar contribuição à página sobre
- Corrigir tradução volc para detecção automática de idioma

## 0.2.34

- Corrigir velocidade de múltiplos idiomas

## 0.2.33

- Suporte a modo de escrita vertical, como japonês.
- Adicionar 3 temas
- Adicionar serviço de tradução Niu

## 0.2.32

- Corrigir tradução básica de PDF
- Corrigir seleção de popup de um serviço não configurado, ir para a página de opções.
- Corrigir permanecer aberto configurações.
- Corrigir velocidade de detecção de múltiplos idiomas

## 0.2.31

- Corrigir injeção de css em iframe dinâmico

## 0.2.30

- Suporte a tradução de iframe inline do userscript.
- Suporte a tradução shadowroot. Por exemplo:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Área de conversa.
- também verificar regra de sincronização no popup

## 0.2.29

- Corrigir tradução do Facebook
- Suporte a mostrar opção de menu de contexto.

## 0.2.28

- Remover correspondência não padrão para userscript

## 0.2.27

- Suporte a tradução de iframe inline. (Apenas para extensão, não disponível para
  userscript)
- Corrigir tradução de múltiplos idiomas

## 0.2.26

- Corrigir addon do firefox android
- Adicionar configurações avançadas para nova linha de tradução

## 0.2.25

- Suporte a tradução de iframe, como email QQ, tweet incorporado.

## 0.2.24

- Adicionar site de tradução temporária por um tempo
- Corrigir API do navegador do userscript stay.app
- Corrigir página de opções do stay.app

## 0.2.23

- Corrigir tradução de página de múltiplos idiomas

## 0.2.22

- Corrigir build do userscript

## 0.2.21

- Corrigir tradução de pdf online no firefox

## 0.2.20

- Corrigir problema de requisição macaque
- Corrigir marca de linha de destaque

## 0.2.19

- Corrigir japonês inteligente tencent
- Corrigir navegador haikuo world

## 0.2.18

- Corrigir mudança de URL do cliente, permanecer automaticamente no estado de tradução.
- Remover contêiner lateral como contêiner de tradução.
- Refatorar posição do popup.

## 0.2.17

- Mudar destaque para marca
- Adicionar tema de tradução de destaque

## 0.2.16

- Compatibilidade com Macaque

## 0.2.15

- Corrigir problema de bounce de toque

## 0.2.14

- Corrigir globalThis.GM do safari não funcionando

## 0.2.13

- Suporte a Arrastar Popup do Userscript
- Suporte a Três Dedos em dispositivo de toque para acionar alternância de páginas de tradução
- Suporte a Ocultar o ícone do popup do userscript.

## 0.2.12

- Melhor para inoreader

## 0.2.11

- Corrigir
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  O conteúdo principal da página de Annas archive não pôde ser traduzido

## 0.2.10

- Corrigir distância de altura de linha em PDF

## 0.2.9

- Corrigir marcação de elementos excluídos
- Corrigir verificação de tipo deno
- remover importmap
- Corrigir tradução de menus de contexto
- restaurar página quando "nunca traduzir este site" estiver ativado
- Adicionar descrição para adicionar URL

## 0.2.8

- Detectar a língua do agente do utilizador para a língua da interface
- Corrigir bug de quebra de linha.

## 0.2.7

- Corrigir pedido de grease monkey

## 0.2.6

- Corrigir
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema de correspondência de URL de ficheiro

## 0.2.5

- aumentar versão para teste de CI

## 0.2.4

- capturar erro de conexão de mensagem para popup.

## 0.2.3

- Corrigir
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  criar contexto múltiplas vezes

## 0.2.2

- Corrigir ficheiro de exemplo PDF
- Corrigir ficheiro local PDF no Firefox
- Corrigir atalhos PDF

## 0.2.1

- Suporte para Gerenciador de Atalhos do Grease Monkey.
- Corrigir correspondência de regex
- Corrigir comentários do YouTube.
- Corrigir versão compacta móvel do Reddit
- Corrigir problema de tradução de texto completo

## 0.2.0

- Corrigir PDF de duas colunas.
- Corrigir bug da versão da Chrome/Edge Store.
- Corrigir
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publicar no addon do Firefox
- Publicar no Edge
- corrigir margem de PDF.
- Alterar ficheiro de exemplo PDF

## 0.0.62

- Corrigir formato PDF, indentação.
- Corrigir mudança de elemento em telegra.ph

## 0.0.61

- Corrigir fechamento de elemento span.
- Corrigir permissão para navegador inicial

## 0.0.60

- Corrigir PDF no Chrome

## 0.0.59

- Suporte inicial para PDF

## 0.0.58

- Editar descrição do tema de tradução

## 0.0.57

- Alterar UI do popup, para facilitar o uso

## 0.0.56

- Corrigir tempo limite do Chrome
- Corrigir erro de divisão de sentença.

## 0.0.55

- Corrigir exibição de elemento "none".
- refatorar marcação de elemento

## 0.0.54

- Suporte para quebra de linha para X caracteres.

## 0.0.53

- usar sendMessage em vez de connect, pois o Chrome desconectará a porta após
  5 minutos
- melhor para detectar contêineres de texto

## 0.0.52

- Não traduzir o parágrafo que só tem elementos de espaço reservado, por
  [exemplo](https://github.com/nank1ro/solidart), a primeira linha.
- Melhor para detectar elementos filhos.

## 0.0.51

- Corrigir problema de cache
  [#12](https://github.com/immersive-translate/next-immersive-translate/issues/12),
  [#7](https://github.com/immersive-translate/next-immersive-translate/issues/7)
- Corrigir tamanho da fonte da UI de opções

## 0.0.50

- Corrigir tradução de imagem bloqueada.

## 0.0.49

- Corrigir extensão do Firefox

## 0.0.48

- Corrigir extensão do Chrome

## 0.0.47

- reescrever mensagem com fundo, usar connect em vez de sendMessage
- adicionar suporte móvel para Reddit
- corrigir espaço em branco pré para alguns artigos

## 0.0.46

- Formatar informações meta do userscript

## 0.0.45

- userscript usa um arquivo.
- adicionar tempo limite para pedido de cache

## 0.0.44

- Corrigir erro de divisão do Tencent.
- Corrigir erro de elemento sup inline.
- Melhor para Twitter

## 0.0.43

- Corrigir tweet br
- Corrigir tradução global.

## 0.0.42

- Corrigir tag BR
- tratar tags de bloco para regras

## 0.0.41

- Corrigir verificação de elemento inline
- Adicionar opção de log de depuração para desenvolvedores

## 0.0.39

- Corrigir serviço de tradução que contém mock2

## 0.0.38

- Suporte para resultado de cache para userscript
- Adicionar UI de opções
- Suporte para detectar mais contêineres de conteúdo

## 0.0.37

- Corrigir mudança de serviço de tradução no popup que não funciona
- Corrigir tradução de conteúdo de post móvel do Reddit.

## 0.0.36

- Corrigir caractere especial da Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Corrigir tamanho do ícone do userscript.
- habilitar todos os sites para detectar a língua do parágrafo.

## 0.0.35

- Corrigir YouTube ir para a próxima página
- Suporte para página de pesquisa do YouTube.
- Corrigir alternância avançada de opções.
- Corrigir tag img, tag oculta
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Corrigir atualização forçada de pesquisa do Google
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Suporte para resultado de tabela do Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Corrigir espaço em branco na Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Alterações de Ruptura

- A tecla de atalho padrão para alternar tradução foi alterada para `alt+A`, pois
  é a tecla mais conveniente para digitar.

### Outros

- Suporte para definir modo de tradução imediata, para que possa traduzir a página web
  o mais rápido possível.
- Suporte para definir a área da página que precisa ser traduzida, para que possa traduzir mais área.
- Suporte para definir a contagem de texto dos primeiros x a serem traduzidos imediatamente.
- Corrigir tradução duplicada ao mudar tradução
- Melhor UI do popup

## 0.0.33

- Suporte para mais línguas, zh-TW, en

## 0.0.32

- Corrigir tradução de ficheiro local após salvo. Corrigido
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Adicionar ficheiro dist js ao repositório público

## 0.0.31

- Suporte para traduzir a página inteira
- Suporte para traduzir página imediatamente
- Mais UI de configuração
- Refletir o tema
- Adicionar novo ícone
- Adicionar novo tema de tradução dashedBorder

## 0.0.30

- Melhor para tema dashed

## 0.0.29

- Corrigir parágrafo válido.
- Adicionar tema dotted, thinDashed
- Melhor para tema dashed, highlight

## 0.0.28

- Corrigir sublinhado
- Adicionar tema dashed, paper
- Corrigir detecção de cabeçalho

## 0.0.27

- Suporte para translationTheme

## 0.0.26

- Corrigir permissão de conexão do userscript volc alpha.
- Corrigir versão clicável.

## 0.0.25

- Suporte para selectorMatches, para que possamos corresponder todos os manstondon agora.
- Corrigir erro de userscript do Firefox.

## 0.0.23

- Melhor para detecção de chinês
- Corrigir problema de innerText do Reddit

## 0.0.22

- Suporte para deeplx
- Corrigir múltiplas traduções ao mudar serviço

## 0.0.21

- Corrigir alguns elementos span que são elementos de bloco

## 0.0.20

- Suporte para não traduzir hashtags como #hash, at tags como @xxx, $tag, como $APPL
- Suporte para elemento de bloco

## 0.0.18

- Suporte para deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Suporte para userscript

## 0.0.4.8

- Corrigir ordem de código.
- Suporte para UI básica de popup

## 0.0.4.6

- Suporte para verificar nova versão

## 0.0.3

- Suporte para ficheiros locais

## 0.0.2

- Suporte para Elementos Dinâmicos
- Suporte para tradução visível