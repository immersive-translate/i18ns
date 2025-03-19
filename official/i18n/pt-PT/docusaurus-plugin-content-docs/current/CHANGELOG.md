---
sidebar_position: 6
---

# Registo de Alterações

Este registo de alterações é atualizado de acordo com o progresso do desenvolvimento. A data após a versão é a data de fusão do código, não a data de lançamento nas lojas de aplicativos (o tempo de revisão varia após a submissão a cada loja de aplicativos, podendo algumas demorar até uma semana para revisão). Atualmente, estamos a avançar com duas versões.

A **versão Release** é a versão estável oficial, disponível nas principais lojas de aplicativos, como [Chrome](https://chromewebstore.google.com/detail/bpoadfkcbjbfhfodiogcnhhhpibjhbnh), [Edge](https://microsoftedge.microsoft.com/addons/detail/amkbmndfnliijdhojkpoglbnaaahippg), [Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate/), [Apple](https://apps.apple.com/app/id6447957425), etc.

A **versão Preview** é publicada com mais frequência e inclui algumas funcionalidades experimentais. Em comparação com a versão Release, pode conter mais bugs. É lançada principalmente em

- [userscript do site oficial](https://download.immersivetranslate.com/immersive-translate.user.js)
- [versão beta na loja Firefox](https://addons.mozilla.org/firefox/addon/immersive-translate-beta/)
- [Github Release Assets](https://github.com/immersive-translate/immersive-translate/releases)

## 1.15.7 Release (2025-03-19)

- Adicionado: Pré-tradução dinâmica de conteúdo a ser traduzido ao navegar em páginas.
- Corrigido: Um problema onde o serviço de tradução AI outputava incorretamente Chinês Simplificado ao traduzir Chinês Tradicional.
- Corrigido: Um problema com a tradução ao passar o mouse não funcionando no modo "Tradução primeiro, texto original segue".
- Corrigido: Problemas de compatibilidade com o modo "Apenas Tradução" quando usado com plugins de leitura como o Reader View.
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
- Otimizado: Compatível com modelos como o1, o3 que não suportam papel de sistema (o parâmetro de papel de sistema não será passado quando a configuração do System Prompt estiver vazia).

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

- Corrigido: Erro `401: Authentication Fails` na chave API personalizada do DeepSeek.

## 1.14.10 Release (2025-02-17)

- Novo: Membros Pro suportam o serviço de tradução DeepSeek (v3).
- Corrigido: Resolvido problema de arquivo de configuração do usuário excedendo o limite de tamanho.
- Melhorado: Item do menu de clique direito pode ser fechado (operado nas configurações avançadas).
- Melhorado: Melhoradas as capacidades de reconhecimento de idioma para Greasemonkey e Safari em páginas com idiomas menores.
- Melhorado: Acesso à interface de teste da página de configurações online.
- Melhorado: Experiência do usuário aprimorada da funcionalidade de pré-visualização de comparação de contexto.
- Melhorado: Lógica de julgamento de modo de toque e mouse.

## 1.14.8 Release (2025-02-10)

- Corrigido: Problema onde arquivos longos do PDF-Pro não eram traduzidos automaticamente.
- Melhorado: Microsoft, Google e Tencent agora suportam Cantonês.
- Melhorado: BBC agora suporta legendas.

## 1.14.6 Preview (2025-02-08)

- Corrigido: Problema onde a **Tradução ao Passar o Mouse** não conseguia traduzir texto rico.
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
- Melhorado: Suporta estilo em negrito no modo apenas tradução.

## 1.13.4 Preview (2025-01-13)

- Adicionado: Membros Pro agora podem usar diretamente o modelo **Zhipu 4 Plus**.
- Melhorado: Tradução Gemini.

## 1.13.1 (2025-01-10)

- Adicionado: Quando o texto traduzido e o texto original pertencem ao mesmo sistema de escrita, exibir a tradução usando um estilo especializado.
- Corrigido: O problema onde a **Tradução ao Passar o Mouse** não funciona em alguns sites.
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

- Corrigido: Problema onde a função de passar o mouse carrega o serviço de tradução errado sob certas condições.
- Corrigido: Problema onde ativar temporariamente legendas bilíngues no YouTube não funciona.
- Corrigido: Após mudar serviços de tradução, o serviço de tradução na "**Caixa de Entrada Aprimorada**" não atualiza.
- Corrigido: O interruptor "**YouTube Enable Bilingual**" na página de configurações não está funcionando.
- Melhorado: Removido o modelo gemini-1.0-pro obsoleto.

## 1.12.4 (2024-12-13)

- Adicionado: **AI Context-Aware Translation** pode melhorar a precisão da tradução de conteúdo profissional. (Disponível apenas para membros Pro, suportado exclusivamente por modelos OpenAI) **Opções** -> **Geral** -> **Ativar AI Context-Aware Translation**
- Corrigido: Alguns bugs no efeito de tradução multilinha no Twitter.
- Corrigido: Problemas com a tradução de certas fórmulas devido a texto rico.
- Melhorado: Ao traduzir em **x.com**, vídeos com legendas terão automaticamente legendas bilíngues traduzidas.
- Melhorado: Vídeos sem legendas exibirão um ícone de tradução e fornecerão uma razão pela qual a tradução não é possível.

## 1.11.7 (2024-11-25)

- Adicionado: Bing/Google agora suportam Khmer (Cambojano).
- Adicionado: Permitir que arquivos ePub incompletos continuem a tradução de onde pararam após reimportação.
- Corrigido: Problema com a tradução de imagens do Twitter no navegador Safari.
- Corrigido: Teclas de atalho tornando-se ineficazes ao alternar a funcionalidade "**Hover Translation**" ativada ou desativada.
- Melhorado: Exibição aprimorada de tradução bilíngue multilinha no Twitter e YouTube.
- Melhorado: Tradução de texto rico é desativada por padrão no modo bilíngue para melhorar a qualidade da tradução.
- ~~Melhorado: Adicionada a opção de personalizar a "**Ativar Tradução de Barra Lateral & Navbar**" em "**Configurações Avançadas**".~~
- Melhorado: Imagens não são mais traduzidas no modo "**Hover - traduzir imediatamente este parágrafo**".

## 1.11.4 (2024-11-16)

- Corrigido: Problema com tradução de fórmulas causado pela "Melhoria de Tradução do Twitter" na versão 1.11.2.

## 1.11.2 (2024-11-13)

- Corrigido: Problema onde o conteúdo desaparece após clicar em "ver mais" no modo apenas tradução do Facebook.
- ~~Melhorado: Exibição aprimorada de traduções bilíngues multilinha no Twitter.~~
- Melhorado: Atualizada a interface do usuário da lista suspensa de serviços de tradução no painel.

## 1.11.1 (2024-11-05)

- Adicionado: Tradução de **Legendas em Tempo Real** agora suporta ativação via "bola flutuante", disponível no Zoom, Google Meet e Microsoft Teams.
- Corrigido: Problemas de sincronização de tempo de legendas no YouTube após assistir anúncios.
- Corrigido: Problemas de exibição com o menu de tradução de clique direito no Safari no MacOS 15.
- Corrigido: Problemas com a funcionalidade de desfazer Ctrl+Z na **entrada aprimorada** em certos sites.

## 1.10.6 (2024-10-25)

- Corrigido: Problema com teclas de atalho de **entrada aprimorada** não sendo acionadas.
- Melhorado: Reduzido o tamanho do pacote de instalação.
- Melhorado: Solução de exibição de legendas da Netflix.

## 1.10.5 (2024-10-23)

- Adicionado: Exibir um aviso quando a língua de origem e a língua de destino forem as mesmas
- Corrigido: Problema de tradução de caracteres de espaço em branco em texto rico [#2175](https://github.com/immersive-translate/immersive-translate/issues/2175)
- Melhorado: Aprimoramento de entrada e funcionalidade de passar o mouse sobre iframes incorporados em páginas web

## 1.10.2 (2024-10-11)

- Adicionado: Tradução de imagem (versão Beta)
- Adicionado: Modo Forçar Ativação do Suporte ao Mouse (Ative esta funcionalidade apenas se a função de passar o mouse não estiver disponível em dispositivos tablet) **Configurações** -> **Configurações Avançadas** -> **Forçar Ativação do Suporte ao Mouse**
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

- Suporte aprimorado para campos de entrada do Baidu, Gmail e outros
- Suporte para cabeçalho de solicitação anthropic-dangerous-direct-browser-access para API Claude Anthropic
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

- Suporte para configurar exceções para idiomas e sites no modo de contraste bilíngue ou apenas tradução (configure na página de Configurações -> Configurações Avançadas). Por exemplo: Se o seu modo de tradução padrão é contraste bilíngue, mas você não deseja que o Chinês Tradicional também use contraste bilíngue, então você pode adicionar o Chinês Tradicional aos idiomas de exceção para contraste bilíngue, assim o Chinês Tradicional usará o modo apenas de tradução para tradução. Da mesma forma, se o seu modo de tradução padrão é apenas tradução, mas você deseja que um determinado idioma ou site use o modo de contraste bilíngue, você também pode adicionar esse idioma ou site aos idiomas de exceção.
- Corrigido um problema onde a caixa de entrada na interface de mensagem privada do Tiktok era traduzida incorretamente
- Corrigido um problema onde quadrinhos no Read Comic Online não podiam ser traduzidos
- Corrigido um problema onde a [Configurações Avançadas -> Número mínimo de caracteres necessários para traduzir um parágrafo] não surtia efeito em alguns casos

## 1.8.4 (2024-08-30)

- O serviço de tradução DeepL agora oficialmente suporta Chinês Tradicional como idioma de destino (anteriormente, traduzir para Chinês Tradicional com DeepL envolvia um processo adicional de conversão de Chinês Simplificado para Tradicional de terceiros).
- Otimizado o desempenho da tradução de texto rico.

## 1.8.3

- O Google Meet agora suporta legendas bilíngues para reuniões ao vivo: Agora, você pode desfrutar do recurso de legendas bilíngues em reuniões do Google Meet. Basta abrir o link da reunião, ativar as legendas bilíngues no painel de tradução imersiva e, em seguida, atualizar a página para experimentá-lo.
- Adicionada a opção de "Relatar problemas de tradução da página atual" e a opção de "Ligar/desligar rapidamente a bola flutuante" nas mais opções do painel.
- Após ajustar a posição das legendas bilíngues do YouTube, o sistema lembrará automaticamente a nova posição.
- Otimizada a lógica de cache do plugin, agora limpando automaticamente dados de cache com mais de 30 dias.
- Otimizados blocos de código dentro de parágrafos para uma restauração mais precisa do texto original.
- Melhorado o tratamento de "palavras não traduzíveis" nas configurações avançadas.

## 1.8.2

- Agora você pode traduzir texto em caixas de entrada com o clique direito: Selecione qualquer texto em uma caixa de entrada em uma página web, clique com o botão direito para escolher traduzir, e a tradução imersiva traduzirá automaticamente o texto selecionado para o idioma de destino da caixa de entrada, tornando conveniente traduzir rapidamente texto em idioma nativo em caixas de entrada para outros idiomas.
- Agora você pode relatar rapidamente problemas de tradução de páginas web na bola flutuante de tradução imersiva. Após traduzir uma página web, se houver algum problema, você pode clicar no botão [Feedback] no lado direito da bola flutuante, preencher a descrição do problema, e nós lidaremos com isso o mais rápido possível.
- Arquivos Epub agora suportam tradução de texto rico (ou seja, preservando o formato do texto original de cada parágrafo, como links, negrito, etc.)
- Suporte para legendas bilíngues em tempo real em reuniões de vídeo na versão web do Microsoft Teams (Abra o link da reunião do Teams, ative as legendas bilíngues no painel de tradução imersiva e, em seguida, atualize)
- Otimizadas legendas bilíngues para a versão em inglês do iQIYI (iq.com)
- Fornecido mais artigos do arXiv com layout de tradução bilíngue otimizado
- Devido a restrições do site do Youtube, o script do Chrome Tampermonkey não suporta mais legendas bilíngues do Youtube. Por favor, use a [versão do plugin](https://immersivetranslate.com/).

## 1.8.1

- Corrigidos problemas de tradução com o script Tampermonkey SiliconCloud
- A tradução Claude agora suporta Tibetano e permite configuração do parâmetro Temperature
- A página de detalhes do especialista em IA exibe os prompts usados pelo especialista
- As configurações de atalho agora permitem atribuir teclas de atalho únicas para qualquer serviço de tradução
- Otimizada a detecção para traduções de artigos do arXiv

## 1.7.9

- Corrigidos problemas com tradução de texto rico para serviços de tradução como Google, DeepL (por exemplo, páginas exibindo diretamente `<button>` etc.)
- Corrigido o problema onde o atalho bilíngue para vídeos do YouTube não podia ser desligado.

## 1.7.8

- DeepL, Microsoft Translate, Google Translate, OpenAI, Claude, Gemini e outros serviços de tradução suportam tradução para manter o formato original do texto (por exemplo, links, negrito, etc.)
- Após selecionar o texto, o menu de clique direito mudará para [Traduzir o texto], clicando no qual você pode pular automaticamente para a página de Tradução de Texto Imersiva
- Novo serviço de tradução gratuito para grandes modelos: SiliconCloud, disponível para todos os usuários.
- Adicionado tradução de grande modelo Zero-One-Thing, que pode ser usado preenchendo a API Key após registrar-se na plataforma Zero-One-Thing.
- Novo botão de feedback do usuário para tradução de mangá (após traduzir um mangá, clique no botão [Feedback] no lado direito da bola flutuante para dar feedback sobre a qualidade da tradução).

## 1.7.7

- Adotar algoritmo de divisão de frases inteligente por IA para legendas em inglês geradas automaticamente no YouTube [Pro Disponível]
- Otimizar a tradução de clique direito para "Traduzir para xx idioma de destino"
- Suporte para integração imersiva [JS SDK](https://immersivetranslate.com/docs/js-sdk/) para sites de terceiros
- Otimizar exibição de legendas do Hulu
- Suporte para tradução de legendas de reuniões na versão web do ZOOM

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

- Habilitada cópia de legendas do YouTube
- Otimizada exibição de legendas em alguns sites de vídeo
- Melhorada a velocidade de tradução de mangá

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
- Legendas bilíngues do YouTube agora suportam divisão inteligente de frases (Beta) (Apenas quando ativar manualmente a tradução imersiva de legendas do YouTube em [Configurações] - [Legendas de Vídeo], e as legendas originais do vídeo são legendas em inglês geradas automaticamente)
- Adicionado serviço de tradução Tencent [【Hunyuan Large Model】](https://immersivetranslate.com/docs/services/tencent-hunyuan/)

## 1.6.5

- Corrigir problemas de layout de texto de traduções de quadrinhos para idiomas no script latino.
- Novos sites suportados para tradução de quadrinhos:
  - COMIC FUZCOMICFUZ(https://comic-fuz.com/)
  - MangaDexMangaDex(https://mangadex.org/)
  - KuaiKan ComicsKuaiKanComics(https://www.kuaikanmanhua.com/)
- Corrigido um problema onde serviços de IA personalizados não podiam selecionar especialistas em IA.

## 1.6.4

- Quando especialistas em IA são usados para "Seleção Inteligente", diferentes especialistas em IA podem ser personalizados para diferentes sites. Isso pode ser configurado em [Configurações] -> [Especialistas em IA] -> [Entrar em qualquer especialista].
- Corrigido o problema onde legendas não são exibidas no YouTube no modo "Apenas Tradução".
- Corrigido o problema de legendas bilíngues não funcionando no Mubi.
- Compatível com PDFs abertos com o plugin Adobe Acrobat.
- Todos os usuários podem [contribuir online](https://weblate.immersivetranslate.com/projects/immersive-translate/extension/) para a tradução multilíngue da interface de tradução imersiva.

## 1.6.3

- Nova funcionalidade: Tradução de manga (Beta), em websites de manga suportados, um botão de tradução de manga aparecerá abaixo da bola flutuante de tradução rápida da página web. Clicar nele ativará a tradução de manga. Esta funcionalidade está disponível para membros Pro (500 páginas por mês, pacotes adicionais podem ser adquiridos), atualmente suportando os seguintes sites:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)

## 1.6.2

- Nova funcionalidade: Tradução de manga (Beta), em websites de manga suportados, um botão de tradução de manga aparecerá abaixo da bola flutuante de tradução rápida da página web. Clicar nele ativará a tradução de manga. Esta funcionalidade está disponível para membros Pro (500 páginas por mês, pacotes adicionais podem ser adquiridos), atualmente suportando os seguintes sites:
  - [MANGA Plus by SHUEISHA](https://mangaplus.shueisha.co.jp)
  - [Zebrack by SHUEISHA](https://zebrack-comic.shueisha.co.jp)
  - [E-Hentai](https://e-hentai.org)
  - [Pixiv](https://www.pixiv.net/manga)
  - [seiga.nicovideo](https://seiga.nicovideo.jp/?cmnhd_ref=device=pc&site=seiga&pos=header_servicelink)
- Nova funcionalidade: Tradução AI suporta [Doubao large model](https://www.volcengine.com/product/doubao)
- Nova funcionalidade: Suporte para modo de comparação bilíngue com tradução primeiro e texto original a seguir, que pode ser ativado na página de configurações -> configurações avançadas.
- Lista de modelos AI personalizados suporta a sintaxe `-all`, que pode apagar todos os modelos predefinidos.
- Em legendas bilíngues de vídeo, quando o idioma alvo é Chinês Simplificado e o texto original é Chinês Tradicional, o texto original será automaticamente convertido para Chinês Simplificado, e vice-versa.
- Corrigido o problema onde o atalho da bola flutuante não conseguia traduzir no iOS 18.
- Corrigido o problema onde Prompts personalizados eram ineficazes quando muitos eram usados.

## 1.6.1

- Suporta a plataforma de grandes modelos Baidu Qianfan, a plataforma de grandes modelos Alibaba Bailian, a plataforma de grandes modelos DeepSeek.
- Corrigido o problema onde modificar o idioma alvo e outras configurações no painel popup resetava ao clicar na bola flutuante de tradução.

## 1.5.8

- Especialistas AI suportam o modo "Seleção Inteligente", onde o sistema selecionará automaticamente o especialista AI mais adequado com base no site atual (por exemplo, especialistas AI relacionados a tecnologia serão automaticamente selecionados para The Verge e Hacker News, enquanto o aprimoramento de tradução do Twitter será automaticamente selecionado para o Twitter).

## 1.5.7

- Suporte para adicionar serviços de tradução AI personalizados compatíveis com OpenAI, acessível na parte inferior da página [Configurações]->[Serviços de Tradução].
- Corrigido um problema onde legendas bilíngues não funcionavam na plataforma de vídeo Domestika no Safari.

## 1.5.6

- Otimização significativa do desempenho de tradução de grandes páginas web, criação de ePub e arquivos de legendas.
- Corrigido o bug de sincronização multi-dispositivo no Pro.

## 1.5.4

- Membros Pro suportam serviços de tradução Claude e Gemini prontos para uso (Beta)
- Legendas bilíngues do YouTube suportam configurações de fonte e peso da fonte
- Corrigido problemas de limite de palavras ao quebrar longos parágrafos [#86](https://github.com/immersive-translate/immersive-translate/issues/86)
- Corrigido reconhecimento de idiomas japonês e coreano
- Corrigido problema onde páginas do Reddit em dispositivos móveis não eram traduzidas ao rolar
- Corrigido algumas páginas faltando traduções com DeepL
- Corrigido tempo de sincronização multi-dispositivo de usuários Pro não sincronizando
- Otimizado problemas de cobertura de configuração de sincronização em nuvem
- Otimizado palavras de prompt para serviços de tradução AI

## 1.5.2

- Corrigido o problema onde mudanças no prompt geral de especialista sobrepunham o prompt de especialista AI especificado [#1692](https://github.com/immersive-translate/immersive-translate/issues/1692)
- Nome de modelo AI personalizado suporta sintaxe avançada, use + para adicionar um modelo, use - para ocultar um modelo, e use model_name=display_name para personalizar o nome de exibição do modelo, por exemplo: +gpt-3.5-turbo,-gpt-4,gpt-4-turbo=gpt-4-super
- Corrigir o erro retornado por Gemini
- Ocultar a bola flutuante ao imprimir a página
- Corrigir o tamanho da fonte não escalando proporcionalmente quando o YouTube está em tela cheia [#1681](https://github.com/immersive-translate/immersive-translate/issues/1681)

## 1.5.1

- Suporte para serviços de tradução AI para definir [AI Expert] para especificar a estratégia de tradução, atualmente uma funcionalidade Beta, que pode ser ativada em [Configurações de Desenvolvedor](https://dash.immersivetranslate.com/#developer) após ativar o Beta, e o menu [AI Expert] pode ser visto após atualizar.
- Serviços de tradução AI agora podem personalizar a lista de modelos, como [OpenAI], o sistema só tem alguns dos modelos mais comumente usados embutidos. Clicando na lista suspensa de modelos, o último item que você vê é [Set More Models], após a configuração, será automaticamente lembrado para a conveniência dos usuários testarem diferentes modelos personalizados.
- Otimizada a inconsistência no layout das traduções em alguns casos.
- Adicionado um botão de reset para o estilo de legendas do Youtube, que pode rapidamente restaurar para o estilo padrão.
- Corrigido o problema onde legendas em chinês não podiam ser baixadas no Youtube.
- Otimizada a cópia da interface em Chinês Tradicional.

## 1.4.12

- Corrigido o problema de caixa de diálogo de mensagem não traduzida ao abrir página do reddit
- Adicionada uma funcionalidade temporária para habilitar edição de tradução na entrada "Mais" do painel
- Corrigido o problema onde YouTube Shorts sem legendas sempre exibe legendas do vídeo anterior [#1655](https://github.com/immersive-translate/immersive-translate/issues/1655)
- Corrigido o problema onde legendas bilíngues do YouTube não podem ser ajustadas para cima e para baixo em tela cheia [#1654](https://github.com/immersive-translate/immersive-translate/issues/1654)
- Suporte para legendas bilíngues [VK Video](https://vk.com/video)
- Suporte para configurações de ativação independente para legendas bilíngues de vídeo do YouTube (ativado por padrão para novos usuários)
- Otimizados prompts de erro para tradução de legendas bilíngues locais

## 1.4.11

- Compatível com tradução da caixa de entrada da página Bing Copilot
- Controle de estilo de legendas do YouTube suporta estilização de borda
- Suporte para selecionar o serviço de tradução padrão na página Configurações -> Serviço de Tradução
- Corrigido substituição de placeholder do OpenAI SystemPrompt
- Corrigido problema de mesclagem de regra de usuário personalizada
- Corrigido exibição anormal de legendas para alguns vídeos da Netflix [#1630](https://github.com/immersive-translate/immersive-translate/issues/1630)
- Corrigido o problema onde mudanças frequentes na cor da tradução através da paleta de cores eram ineficazes [#1628](https://github.com/immersive-translate/immersive-translate/issues/1628)

## 1.4.9

- Serviços de tradução agora estão organizados distintamente sob uma aba separada, permitindo uma visão abrangente de todos os serviços de tradução disponíveis. Além disso, os usuários têm a flexibilidade de personalizar quais serviços de tradução são exibidos. Por padrão, apenas uma seleção limitada de serviços de tradução é mostrada, mas os usuários podem ajustar suas preferências de exibição na seção [More Services](https://dash.immersivetranslate.com/#services).
- A página de configurações agora acomoda ajustes para [estilos de legendas do YouTube](https://dash.immersivetranslate.com/#subtitle).
- Melhorias foram feitas para resolver o problema onde legendas bilíngues imersivas não eram exibidas quando os usuários definiam o idioma das legendas para Chinês no site do YouTube.
- Um novo atalho foi introduzido para tradução temporária chamado Claude, que pode ser configurado na [página de Configurações de Atalho](https://dash.immersivetranslate.com/#shortcuts).

## 1.4.8

- Otimizar desempenho de tradução para arquivos grandes em PDF-Pro
- Melhorar desempenho de tradução para páginas de conteúdo longo
- Implementar suporte à internacionalização (i18n) para navegação de documentos de página
- YouTube introduz uma funcionalidade para habilitar temporariamente legendas bilíngues
- YouTube suporta o download de legendas bilíngues (apenas para membros)
- Móvel adiciona controle por gestos, melhorando a entrada via [configurações de atalho](https://dash.immersivetranslate.com/#shortcuts)
- Suporte para tradução bilíngue para Google Docs

## 1.4.7

- Corrigido o problema onde a tradução falhava ao alternar palavras de prompt personalizadas do OpenAI sob o botão de teste
- Corrigido o problema do ícone de atalho de legendas do YouTube não exibindo
- Otimizada a detecção de idioma da extensão

## 1.4.6

- Corrigido o problema onde palavras de prompt definidas pelo usuário eram ineficazes
- Adicionadas opções de 50%, 150% para tamanho de fonte de legendas do Youtube

## 1.4.5

- Corrigido o problema onde mudanças nos estilos de legendas do Youtube não eram salvas
- Corrigido o desaparecimento de legendas em tela cheia no iOS Safari
- Otimizada ainda mais a velocidade de tradução de legendas do Youtube
- Mais opções do painel agora suportam [entrada de tradução de texto](https://app.immersivetranslate.com/text/)

## 1.4.2

- Suporte para serviço de tradução Claude
- Otimizado prompts multi OpenAI, suportando formato YAML, o que melhora a flexibilidade e facilidade de uso da configuração
- Otimizada significativamente a velocidade de tradução de legendas do Youtube, e adicionou suporte para alternar entre ordem Chinês e Inglês, personalizar cor e tamanho da fonte, etc.
- Plataforma de legendas de vídeo suporta [University of Southampton](https://southampton.cloud.panopto.eu)
- Legendas bilíngues do Udemy compatíveis com exibição móvel
- Serviço de tradução Gemini é oculto por padrão, pode ser ativado nas configurações de desenvolvedor para mostrar beta deste serviço de tradução

## 1.3.4

- Suporte para serviço de tradução gratuito Yandex
- Otimizados prompts Gemini
- Legendas de vídeo suportam configuração para exibição bilíngue/original e tradução
- Suporte para espaço entre Chinês e Inglês nos resultados de tradução OpenAI
- Alternância do painel para exibir apenas botão de tradução modificado para só ter efeito na página atual

## 1.3.3

- Otimizado o problema de exibição de tradução de legendas de vídeo CC do Twitter.
- Serviço DeepL adicionou suporte para Árabe.
- Serviço de tradução Colorful Clouds agora suporta Coreano, Espanhol, Francês e Russo.
- Serviço OpenAI adicionou suporte para dialeto do Nordeste da China.
- Detecção automática do painel agora exibe o idioma original.
- Ajustada a descrição do atalho para o painel móvel.

## 1.3.2

- Corrigido o problema onde o painel de controle não podia ser fechado em dispositivos móveis

## 1.3.1

- Suporte para legendas de vídeo na plataforma [DeepLearning.ai](https://learn.deeplearning.ai)
- Suporte para tradução de páginas web e legendas de vídeo em idiomas como árabe, hebraico, etc., resolvendo problemas de exibição RTL (da direita para a esquerda)
- Corrigida a tradução de Gemini para hebraico
- Corrigido um problema onde algumas legendas em chinês tradicional no YouTube não eram exibidas corretamente
- Corrigido o problema de exibição de legendas do Twitter no Safari
- Corrigido o atalho para tradução imediata para o final da página

## 1.2.4

- Corrigido o problema onde os placeholders na criação de ePub não eram substituídos corretamente
- Suporte para tradução de legendas de vídeo [Unreal Sensei](https://www.unrealsenseiacademy.com/)

## 1.2.3

- Otimizada a frequência de controle das solicitações de serviço de tradução
- Recentemente, as solicitações de serviço de tradução da Microsoft a partir da China têm sido instáveis; quando ocorrem erros, o sistema detecta automaticamente o serviço de tradução atualmente disponível, permitindo que os utilizadores mudem rapidamente.
- Otimizada a mensagem de erro para erros de rede
- Corrigido o problema onde a configuração da cor do texto não suportava a pré-visualização RGBA [#1435](https://github.com/immersive-translate/immersive-translate/issues/1435)
- Corrigido o problema onde a atualização da versão do plugin Safari sempre exibia a página de sucesso de instalação
- A Microsoft adicionou suporte para vietnamita
- Corrigido o problema onde legendas traduzidas no site edx não eram exibidas

## 1.2.2

- Suporte para tradução de legendas de vídeo para [pluto](https://pluto.tv/), [STARZ](https://www.starz.com/), [Paramount Plus](https://www.paramountplus.com/), [Rotten Tomatoes](https://www.rottentomatoes.com/), [Dailymotion](https://www.dailymotion.com/), [FMovies](https://fmoviesz.to/), [AniWatch](https://aniwatch.to/), [iQIYI](https://www.iq.com/), [Youku](https://www.youku.tv/), [movie-web](https://movie-web.app/). Também suporta a tradução de alguns vídeos com legendas CC no Twitter.
- Otimizados os pop-ups de erro, os pop-ups de erro de problemas de rede detectam automaticamente serviços de tradução gratuitos válidos.
- Corrigido o suporte do aplicativo iOS imersivo para reprodução em tela cheia no YouTube.
- Corrigido o problema de tradução de parágrafos com Perplexity.ai [#707](https://github.com/immersive-translate/immersive-translate/issues/707).

## 1.2.1

- Suporte para tradução de legendas de vídeo para [Kanopy](https://www.kanopy.com/), [RachelsEnglishAcademy](https://www.rachelsenglishacademy.com/), [Hulu](https://www.hulu.com/), [Three.js Journey](https://threejs-journey.com/).
- Corrigido um problema onde alguns utilizadores Pro não conseguiam modificar configurações no navegador Chrome.
- Suporte para exibição de legendas bilíngues no modo de tela cheia do YouTube no iOS.

## 1.2.0

- Suporte para tradução de legendas de vídeo nas plataformas [LinkedIn](https://www.linkedin.com/) e [Viu](https://www.viu.com/).
- Adicionado mais acesso rápido a legendas de vídeo para plataformas adicionais.
- Suporte para definir sites/idiomas específicos para exibir apenas o texto traduzido.
- Corrigido um problema onde a página de configurações continuava a mostrar carregamento em alguns casos no Safari.
- Suporte para tradução de nós de tags de entrada.
- Otimizada a interface do usuário do pop-up de erro.

## 1.1.9

- Suporte para tradução de legendas para YouTube Live e a plataforma [Mubi](https://mubi.com/).
- Otimização: Página de configurações, interface de interação da lista de URLs (para evitar ambiguidades, as caixas de seleção não são exibidas por padrão).
- Suporte para definir a fonte de tradução no modo apenas tradução.
- Adicionado acesso rápido para ativar legendas de vídeo na Netflix, Ted, Bloomberg, Udemy, Coursera.
- Corrigido: Alguns estilos traduzidos (como sublinhados) não eram eficazes no Safari.
- Corrigido: Durante a tradução de página, o problema onde passar o mouse não acionava a retradução.

## 1.1.8

- Adicionada uma opção para o serviço de tradução secundário seguir o serviço de tradução principal
- Suporte para legendas bilíngues para [Amazon Prime Video](https://www.primevideo.com)
- Otimização adicional da função de tradução de PDF incorporado no Sci-Hub
- Corrigido um problema com PDFs online não abrindo corretamente
- Corrigido o problema com a reprodução contínua de legendas bilíngues na Netflix

## 1.1.7

- Agora você pode especificar uma fonte para a tradução na página de configurações -> [Configurações Básicas] -> [Estilo de Tradução]
- Adicionada uma configuração de atalho para [Traduzir Parágrafo Especificado] no painel de bola flutuante em dispositivos móveis
- Otimizada a sensibilidade de detecção de passar o mouse sobre Ctrl para evitar confundir `Ctrl+C` como `Ctrl`
- Adicionado suporte para uma nova configuração de atalho que permite alternar rapidamente se as legendas de vídeo usam as legendas de tradução automática incorporadas
- No site Sci-Hub, clicar na bola flutuante traduzirá PDFs incorporados na página web

## 1.1.6

- **Suporte Móvel para Tradução de Parágrafos Específicos:** A versão móvel agora suporta a tradução de parágrafos especificados e adicionou uma variedade de operações de atalho, incluindo deslizar para a esquerda, deslizar para a direita, toque duplo, toque triplo e gestos de toque com vários dedos. Estes não estão ativados por padrão e requerem que o utilizador selecione ativamente o gesto de ativação na página de configurações em [Passar o Mouse].
- **Atualização da Versão Padrão do Gemini:** A versão padrão agora é `v1beta`.
- **Correção da Tradução de Chinês Clássico:** Corrigida a funcionalidade de tradução de Chinês Clássico da Microsoft e OpenAI.
- **Otimização da Tradução Japonesa:** Otimizada ainda mais a tradução japonesa da OpenAI para melhorar a precisão e fluência.
- **Experiência de Tradução Imersiva:** Para melhor se adaptar aos hábitos dos utilizadores, movemos o atalho para legendas bilíngues no modo de tela cheia na plataforma YouTube para o lado esquerdo.

## 1.1.5

- Corrigido o problema onde o menu suspenso no modo escuro no Windows não tinha cor.
- Corrigido o problema de alinhamento com a opção "Mais" não estando alinhada à esquerda no Windows.

## 1.1.4

- **Atualização da Interface do Painel de Pop-up:** O novo design visa melhorar a usabilidade e compreensão. Esta atualização inclui:

  - **Novas funcionalidades no menu principal:**
    - **Alternância de modo bilíngue/apenas tradução:** Agora você pode alternar entre "Modo de Tradução Bilíngue" e "Modo Apenas Tradução" diretamente no menu principal, localizado à esquerda do botão de tradução.
    - **Entrada de tradução de documentos:** A entrada para traduzir "arquivos PDF/ePub/legendas" foi movida para o menu principal para acesso rápido.
    - **Configurações de tradução de vídeo:** A entrada para configurações de "Tradução de Vídeo" também foi colocada no menu principal para ajustes rápidos.
    - **Nova entrada para documentação de uso:** Fornece guias de operação detalhados e documentos de ajuda.

- **Entrada de tradução de documentos integrada:** Agora, você pode traduzir arquivos PDF, ePub e legendas através de uma entrada de upload unificada. Basta clicar no botão [PDF/ePub] no painel de pop-up, sem necessidade de selecionar [Mais] mais.

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
- Adicionado um modo apenas tradução na página de configurações.
- Adicionada uma função de lembrete ao alternar modos de tradução com atalhos.
- Corrigido o problema onde traduzir campos de entrada contendo URLs apenas traduzia partes do conteúdo.

## 1.1.2

- Correção: O problema onde alternar serviços de tradução não surtia efeito quando a página ainda não havia sido traduzida.
- Otimização: No processo de tradução de Epub e PDF, se algum conteúdo falhar na tradução, agora é possível alternar para outro serviço de tradução no painel sem reiniciar todo o processo de tradução (a lógica anterior era usar imediatamente um novo serviço de tradução para retraduzir todo o livro). Isso significa que no meio da tradução, você pode mudar para um serviço de tradução diferente e clicar em [Tentar Novamente Todos os Parágrafos Falhados], após o qual o sistema continuará a tradução usando o novo serviço.
- Otimização: Ajustado o tamanho da fonte dos avisos de erro de tradução para melhorar a legibilidade.

## 1.1.1

- Corrigido o problema do atalho de legendas bilíngues para YouTube ter texto em inglês excessivamente longo.

## 1.1.0

### Novas Funcionalidades

- **Configurações de Teclas de Atalho**: Adicionado um novo menu de nível superior "Atalhos" e as seguintes funções de teclas de atalho personalizáveis:

  - Designar uma combinação de teclas para traduzir o conteúdo da caixa de entrada atual, complementando o método anterior de pressionar rapidamente a barra de espaço três vezes.
  - Designar uma combinação de teclas para ativar temporariamente "tradução direta ao passar o mouse" na página. Pressioná-la novamente cancelará esta função.
  - Adicionadas teclas de atalho dedicadas para 6 serviços de tradução (como DeepL, OpenAI, Google, Microsoft, Gemini, Tencent Interactive Translation) para facilitar a troca temporária entre serviços de tradução.

- **Atualização da Interface da Página de Configurações do Plugin**:

  - Em "Configurações Avançadas", uma nova opção foi adicionada para permitir que os utilizadores especifiquem certas palavras (por exemplo, "LLM") a serem excluídas da tradução.
  - Em "Configurações Avançadas", uma nova opção foi adicionada para configurar o número mínimo de caracteres necessários para traduzir um parágrafo. O padrão é 4 caracteres, mas pode ser definido mais alto (por exemplo, 20), para que apenas parágrafos mais longos sejam traduzidos.
  - Adicionado um tutorial para iniciantes, cobrindo configurações de bola flutuante, configurações de legendas de vídeo e configurações de passar o mouse.

- **Legendas Bilíngues do YouTube**: Adicionado um acesso rápido na janela de reprodução de vídeo do YouTube para ativar ou ocultar legendas bilíngues (este recurso pode ser desativado).

- **Suporte de Idioma Deepl**: Adicionado suporte para português (Brasil).

- **Novo Guia do Utilizador**: Quando novos utilizadores abrem uma página em um idioma não-alvo pela primeira vez, uma bolha de ajuda da bola flutuante é exibida.

### Otimização e Correções

- **Otimização da Interface do Usuário**: Redesenhada a interface do usuário para avisos de erro de tradução de página para torná-los mais fáceis de entender. Quando há muitos erros, um pop-up irá ativamente avisar o utilizador.

- **Correções de Bugs**:

  - Corrigido o problema onde a tradução ao passar o mouse falhava quando a página perdia o foco.
  - Corrigido o problema onde menos de 3 caracteres na funcionalidade de aprimoramento de caixa de entrada não eram traduzidos.
  - Corrigido o problema onde alguns diretórios não eram traduzidos durante a produção de Epubs bilíngues.

- **Remoção de Funcionalidade**: Removida a funcionalidade de aprimoramento de informações bilíngues (exibindo resultados de pesquisa em inglês nas páginas de pesquisa do Google simultaneamente).

### Outras Atualizações

- **openAI Configuration Update**: Agora suporta definir o número de configurações por segundo em decimais, como 0.5, significando 1 pedido a cada 2 segundos.

## 0.12.14

- Correção: O problema de reconhecimento do idioma alvo padrão em algumas máquinas após a primeira instalação.
- Otimização: A ordem padrão dos títulos das páginas web foi alterada para [Chinês - Inglês].

## 0.12.13

- Corrigido: Problema com a junção de tradução de parágrafos longos do OpenAI em alguns casos. [#1276](https://github.com/immersive-translate/immersive-translate/issues/1276)
- Otimizado: Ao usar o mouse hover, o problema de perder o foco na página e depois reativar torna-se ineficaz.
- Corrigido: O problema em que o cache ainda existe após modificar o prompt/modelo no OpenAI.

## 0.12.12

- Atualizado: Otimizado o painel pop-up, removendo algumas opções para o site atual.
- Otimizado: Melhorado o processo de fusão de legendas manuais.
- Otimizado: Definir automaticamente o idioma alvo com base no idioma do navegador.
- Adicionado: Suporte a legendas bilíngues para a plataforma de aprendizagem [ArtStation](https://www.artstation.com/learning) e [ZDF](https://www.zdf.de/).
- Corrigido: Resolvido o problema em que os títulos na página de lista do jstor não eram traduzidos [#1268](https://github.com/immersive-translate/immersive-translate/issues/1268).
- Corrigido: Corrigido o problema em que apenas parte do conteúdo desaparecia no Hacknews [#1264](https://github.com/immersive-translate/immersive-translate/issues/1264).

## 0.12.11

- Adicionado suporte a legendas bilíngues para as plataformas [HBO Max](https://play.max.com/), [BBC](https://www.bbc.com/), [Disney+](https://www.disneyplus.com), [ARD Mediathek](https://www.ardmediathek.de/), [ITV](https://www.itv.com/), e [Domestika](https://www.domestika.org).

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

- Reparar as legendas originais do vídeo não são exibidas quando "O site atual está configurado para nunca traduzir".
- Reparar o conflito com alguns plug-ins que causam retorno infinito da página.
- Reparar a não tradução de alguns parágrafos após ativar quebras de linha de parágrafos longos.
- Corrigido [Quando temporariamente ativando a tradução da página web por um longo tempo, clicar no painel [Sempre traduzir este site] não cancela a tradução sempre #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)

## 0.12.7

- Legendas bilíngues adicionadas para suportar as plataformas [TED](https://www.ted.com), [Frontend Masters](https://frontendmasters.com/), [edx](https://www.edx.org/), [CodeWithChris](https://www.edx.org/), [Skillshare](https://www.ted.com) https://learn.codewithchris.com/enrollments), [Skillshare](https://www.skillshare.com/).
- O hoverball agora está oculto por padrão quando o vídeo está em tela cheia.
- Corrigir o problema de clique trêmulo do painel de ação do hoverball da página do Firefox.
- Suporte para colaboração sob o site pubmed.ncbi.nlm.nih.gov e o plugin scholarscope.
- Corrigir problema de tremor da página de tradução da caixa de entrada do Reddit.

## 0.12.6

- Corrigir o problema de que a tradução do YouTube/Web of Science etc. não é sensível ao alternar abas.
- Hoverball no celular agora suporta operação de longa pressão, pressão curta para traduzir, longa pressão para abrir o painel.
- Traduzir e-books bilíngues agora também traduzirá o índice.
- O recurso de Melhoria de Pesquisa (algumas páginas do Google Search exibem resultados de pesquisa bilíngues) agora não está ativado por padrão e será removido na próxima release.

## 0.12.5

- Corrigir a criação de eBooks Epub a partir do painel clicando em traduções que não funcionam.

## 0.12.4

- Quando você ativa legendas bilíngues no painel, ele primeiro atualizará a página automaticamente (para exibir legendas bilíngues com mais precisão), e alguns sites ainda exigem que os usuários cliquem manualmente no botão "CC" no site para ativar as legendas.
- Otimizar Grease Monkey, detecção de idioma do Safari.
- Fornece acesso rápido a versões bilíngues de todos os artigos no site de artigos [Arxiv](https://arxiv.org/abs/1910.06709).
- [Suporte de hoverball configurado para ser fixado à esquerda #1168](https://github.com/immersive-translate/immersive-translate/issues/1168)
- [Corrigir problema de exibição do Modo de Aprendizagem #1180](https://github.com/immersive-translate/immersive-translate/issues/1180)
- [Ativar temporariamente a tradução da web por um tempo não cancela Sempre Traduzir #1172](https://github.com/immersive-translate/immersive-translate/issues/1172)
- Otimizar problemas de inicialização de arquivos PDF.

## 0.12.3

- Correção para o recurso [desativar permanentemente legendas de vídeo] não funcionando [#1175](https://github.com/immersive-translate/immersive-translate/issues/1175)

## 0.12.2

- Suporte a legendas bilíngues é fornecido para mais plataformas de vídeo, que agora são suportadas: [Youtube](https://www.youtube.com/), [Netflix](https://www.netflix.com), [Udemy](https://www.udemy.com/), [Khanacademy](https://www.khanacademy.org/), [Coursera](https://www.coursera.org/), [Vimeo](https://vimeo.com/), [Nebula](https://nebula.tv), [Bloomberg](https://www.bloomberg.com), [Bilibili](https://www.bilibili.com/), etc. (Note que devido a limitações técnicas, alguns sites precisam atualizar a página após ativar as legendas bilíngues pela primeira vez ou esperar a tradução ser concluída para exibir as legendas bilíngues).
- Otimização significativa do tamanho do zip do plugin, reduzido pela metade em comparação com o original, download e atualização mais rápidos.
- Corrigir problemas de download de PDF estendido.
- Adicionado um portal de tradução rápida de PDF ao lado direito do site de artigos [Arxiv](https://arxiv.org/abs/1910.06709), que vai para uma página HTML limpa (apenas suportado por alguns artigos, pois requer que os autores originais enviem o código-fonte, então aproximadamente 50% dos artigos mostrarão este portal).
- Páginas PDF online sem extensão .pdf agora podem pular diretamente para a página de tradução de PDF clicando no hoverball na página.
- Corrigir alguns problemas de aprimoramento de caixa de entrada no Safari.
- Otimizar a detecção de idioma no Grease Monkey e Safari.

## 0.11.6

- Adicionado 11 novos idiomas de interface para o plugin e o site oficial, agora os idiomas de interface suportados chegam a 14, incluindo Chinês Simplificado, Chinês Tradicional, Inglês, Japonês, Coreano, Russo, Espanhol, Português, Hindi, Italiano, Alemão, Francês, Árabe e Persa.
- Modificar o compartilhamento bilíngue (modo de atualização) adicionado na última versão para compartilhamento de instantâneo de página bilíngue, para que o conteúdo compartilhado seja mais original, bem como maior adaptabilidade.
- Corrigir emoji no final da caixa de entrada do Twitter que não pode ser traduzido.
- Corrigir a situação em que o conteúdo de plug-ins de terceiros é traduzido em alguns cenários.
- Reparar clique não responsivo do hoverball em pdf online.

## 0.11.5

- Agora você pode gerar um link público para a página bilíngue traduzida para o Immersive Translate.
  - [Clique](/docs/share/) no ícone de compartilhamento do Immersive Translate para gerá-lo com um clique!
- Resolvido o problema de que algumas plataformas não conseguiam reconhecer se o mouse era suportado ou não.
  - Existem alguns navegadores de desktop que suportam tanto touchscreen quanto mouse, e o Immersive Translate é tecnicamente incapaz de detectar se tais plataformas suportam mouse, então adicionamos a opção [Forçar Ativar Suporte a Mouse] na configuração [Mouse Hover].

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

- Suporte para configurar botões de tradução rápida do hoverball (suporte para PC/móvel).
- Otimizar julgamento de idioma do Grease Monkey.
- Corrigir tradução de arquivo txt.

## 0.10.7

- Suporte a mouse hover pressione Ctrl novamente para mostrar o texto original.
- Mouse Hover Ignorar Idioma Nunca Traduzir.
- Otimização de Legendas Bilíngues do Youtube.

## 0.10.6

- Suporte a legendas do Youtube apenas para traduções.
- Adicionar Alerta de Atualização de Versão Baixa do Grease Monkey.
- Corrigir o problema de que arquivos txt locais não podem ser traduzidos.

## 0.10.5

- Corrigir o Youtube ocasionalmente retornando à página inicial.

## 0.10.4

- Corrigir conflito de legendas do Youtube com plugin de legenda dupla (Tradução de legendas do Youtube do Immersive Translate não é ativada quando o plugin de legenda dupla do Youtube é detectado para evitar conflito).
- Adicionado [Função de Desativar Permanentemente Legendas de Vídeo], se houver outros problemas de conflito e você não quiser ativar a função de legendas bilíngues com o Immersive Translate.
- Otimizar quebras de legendas.

## 0.10.3

- Corrigir problema de tradução de chave de autenticação personalizada do DeppL.

## 0.10.3

- Suporte perfeito para vídeos do Youtube com legendas bilíngues 🎉.
- Para páginas de artigos, o texto principal agora será traduzido primeiro antes do restante do conteúdo da barra lateral.
- Otimizar Contextualização de Tradução DeepL.
- Otimizar tradução de arquivos de legendas do OpenAI para contextualização.

## 0.10.1

- Aumentar a prioridade da tradução do corpo para otimizar a experiência de tradução
- Corrigir o problema de texto não traduzido ao clicar mais em ins

## 0.9.8

- Otimizar a experiência, corrigir alguns bugs

## 0.9.7

- Corrigir a tradução automática quando readwise está destacado

## 0.9.6

- Corrigido o problema de limpar o cache ao fazer logout do utilizador.

## 0.9.5

- Correções de bugs em eBooks online

## 0.9.4

- Otimizar a deteção de melhoria de entrada para reduzir toques falsos
- Tradução de e-books e legendas online

## 0.9.3

- Tradução da Caixa de Entrada: exibe um lembrete pop-up quando é usado pela primeira vez, e o utilizador pode optar por desativá-lo desta vez ou permanentemente para evitar toques acidentais.
- Otimização da velocidade de exportação apenas de tradução em PDF, se optar por exportar apenas a tradução, pode chamar diretamente a pré-visualização de PDF do sistema para exportar, mais rápido.
- Deeplx suporta múltiplos URLs, basta separá-los com .

## 0.9.2

- A ferramenta de tradução de PDF é migrada para a versão online: https://app.immersivetranslate.com/pdf/ , para que Grease Monkey e Safari possam usar a tradução de PDF, e os problemas podem ser melhor iterados sem a necessidade de emitir uma versão para resolver o problema.
- Otimização da UI POPUP, o painel está mais bonito!

## 0.9.1

- Corrigir problemas de nome de ficheiro com a criação de eBooks Epub

## 0.8.8

- Suporte a pdf para ajustes de espaçamento de linha e espaçamento de palavras para re-reconhecer parágrafos
- Correção do problema de rolagem automática na leitura online de epub em dispositivos móveis

## 0.8.7

- Suporte a pdf para downloads apenas de tradução
- Corrigir problema de login do Google no Safari

## 0.8.2 - 0.8.6

- Permite definir o intervalo entre os gatilhos de combinação de melhoria de entrada
- Corrigir alguns bugs

## 0.8.1

- Otimização da Deteção de Idioma
- Funcionalidades Beta: API Personalizada (Beta ativada nas definições de desenvolvedor)
- Suporte para Tradução AliCloud
- Corrigidos alguns bugs

## 0.8.0

- Sistemas de Utilizadores Suportados
- Suporta [Ativar Pro Membership](/pricing), que permite aos utilizadores desfrutar de traduções Deepl e OpenAI e definições de sincronização na nuvem.
- O serviço de tradução ao passar o mouse pode ser configurado individualmente
- O serviço de tradução da caixa de entrada pode ser configurado separadamente
- Otimização da Tradução de PDF
- Corrigidos alguns bugs

## 0.7.16

- Tradução de PDF com novas opções para controlo rápido do estilo de tradução (os ficheiros PDF são muito estranhos e ativar estas opções pode ser útil para alguns ficheiros PDF com formatação confusa)
- As versões iOS e macOS estão de volta na Apple Store Country Store

## 0.7.15

- Fomos notificados pela Apple de que as Traduções OpenAI foram temporariamente removidas do iOS e macOS, e estamos a tentar relançá-las na China.

## 0.7.11- 0.7.14

- Corrigir: problema de Tradução de Todas as Regiões no Gmail
- Desativar temporariamente a função de exportação de PDF do Safari devido à restrição do Safari sobre downloads de plug-ins (bug).
- Corrigir alguns outros problemas

## 0.7.10

- Atualização da UI do Painel de Ícones do Navegador Pop-up, um pouco mais de design ～
- Corrigir o problema de que algumas passagens em japonês não são traduzidas.

## 0.7.9

- Finalmente, o PDF suporta a exportação de versões bilíngues! Pode clicar no botão [Guardar] para exportar o ficheiro PDF bilíngue traduzido.
- As regras personalizadas agora suportam a fusão com as regras padrão incorporadas, por exemplo: `{"id": "youtube", "selectors.add":["#test"]}` significa adicionar um `#test` aos seletores existentes, `selectors` significa substituir o padrão, `selectors.remove` significa eliminar um dos seletores padrão, e `selectors.remove` significa eliminar um dos seletores padrão.
- Atualizado o ícone do Safari, um pouco maior.
- Outras Correções de Bugs

## 0.7.8

- Correções de Bugs

## 0.7.7

- Adaptado ao estilo do sistema do Safari, o ícone da extensão do Safari mudou para contorno transparente.
- Adicionar mudança de estado do ícone do navegador, quando uma página web foi traduzida, um ✅ será adicionado automaticamente ao canto inferior direito do ícone do navegador.
- Ativar automaticamente a tradução de sites em inglês frequentemente usados para novos utilizadores
- Corrigir problemas de tradução com https://claude.ai/

## 0.7.6

- Suporte a Resultados de Tradução Melhorados na Entrada ctrl+z Desfazer
- Suporte a tradução no modo de leitura de documentos do Flying Book
- Adaptação https://pi.ai/talk

## 0.7.5

- Corrigir ícone do Grease Monkey não exibido
- Corrigir vários problemas

## 0.7.4

- Corrigir vários problemas
- A página de configuração suporta a eliminação em massa de URLs selecionados.
- Suporta ativar/desativar a tradução de legendas do Youtube para evitar conflitos com outros plugins relacionados.
- O Arigato Translator suporta a definição de campos e id de terminologia

## 0.7.2

- Melhoria da Caixa de Entrada: permite omitir o prefixo // e acionar a tradução de toda a caixa de entrada com 3 espaços, ou pode desativar esta opção na página de configurações.

## 0.7.1

- Suporte a Melhoria de Pesquisa, quando ativado, ao pesquisar no Google/Google News em chinês, a coluna da direita mostrará automaticamente os resultados de pesquisa das palavras-chave correspondentes em inglês, que está ativado por padrão.
  - Razão: Descobrimos que na pesquisa do Google, os resultados de pesquisa para palavras-chave em chinês e palavras-chave em inglês podem ser muito diferentes, com a Melhoria de Pesquisa Traduzida Imersiva ativada, pesquisamos automaticamente as mesmas palavras-chave em inglês para si e exibimos no lado direito. Pode optar por desativá-la se não precisar da funcionalidade.
  - O Safari não é suportado devido a limitações da API.

## 0.6.20

- Modificar as configurações padrão: Devido ao grande número de feedbacks dos utilizadores de que não usarão a ferramenta de tradução após a instalação, a sua expectativa da ferramenta de tradução é que ela traduza automaticamente páginas web em inglês após a instalação, por isso, a partir desta versão, para utilizadores chineses, a opção de traduzir páginas em inglês por padrão foi ativada (se o utilizador tiver uma configuração anterior do idioma que será sempre traduzido, então será respeitada, e a alteração apenas modifica as configurações iniciais da extensão), e precisa ser cancelada, pode ser facilmente cancelada no [Painel Pop-up ou página de configurações](/docs/faq/#%E5%A6%82%E4%BD%95%E5%85%B3%E9%97%AD%E8%87%AA%E5%8A%A8%E7%BF%BB%E8%AF%91)

## 0.6.19

- Corrigir Bugs de PDF
- Corrigir Bug da web of science
- Adaptação feeder.com
- Corrigir epub não traduzindo alguns livros

## 0.6.18

- Corrigir problema de largura de Popup no Safari.
- Otimização do Processo de Construção

## 0.6.17

- Otimizar alertas de erro
- Otimizar a seleção do idioma alvo, agora só mostrará os idiomas suportados pelo serviço de tradução correspondente
- Otimização da Tradução de PDF
- Adaptado para o site Good Reads, Amazon e South China Morning Post

## 0.6.16

- Adicionar exibição de página sem permissão em PDF
- Reparar a exibição de parágrafos da lista de texto em PDF
- Ampliar a escala de fonte pequena em PDF no chrome e safari

## 0.6.15

- Reparar o problema de que ao abrir ficheiros PDF, o painel de extensão avisa que não há permissões.
- Corrigir o problema de que a melhoria da caixa de entrada não é ativada quando o site está configurado para nunca traduzir.

## 0.6.14

- Otimização da tradução de PDF, a área de tradução agora pode ser editada/arrastada/excluída
  - Arrastar no canto superior esquerdo, excluir no canto superior direito, alterar tamanho no canto inferior direito
- Alinhamento à esquerda da Caixa de Seleção do Windows
- Suporte a Chinês Tradicional e Chinês Simplificado

## 0.6.13

- Corrigir o problema de tradução repetida ao passar o mouse
- Suporte a tradução de PDF para arrastar para alterar o tamanho e editar o conteúdo da tradução

## 0.6.12

- Corrigir imagens de tradução de Epub ficando menores em alguns navegadores
- Otimização da tradução da caixa de entrada, agora funciona suavemente no Bard!

## 0.6.10

- Modelo padrão do OpenAI alterado para a versão 0613
- Corrigir alguns estilos de caixa de entrada
- Mais inteligente para determinar se é uma área de navegação, e se for, não é realizada tradução
- Corrigir possíveis ataques de injeção XSS

## 0.6.8

- O painel de extensão agora pode indicar páginas não suportadas (por exemplo, páginas sem permissões e páginas não-HTML)
- Melhoria da caixa de entrada para mostrar o estado de Carregamento na tradução
- Atualizar cores de carregamento padrão nas traduções
- Quando a caixa de entrada é configurada sem prefixo, suporta tradução `ja Hello` para japonês e `English Hello` para inglês.

## 0.6.6

- Correção para: algumas áreas não traduzindo (quora)

## 0.6.5

- Otimização do Google Bard
- Tradução da Caixa de Entrada suporta tradução direta de toda a caixa de texto sem prefixos.
- Otimizar o problema de traduções do OpenAI adicionando pontos sem sentido, (se nenhum ponto for detetado no texto original, se o openai retornar um ponto, então removê-lo)
- Problemas com ficheiros de legendas do safari não sendo reconhecidos

## 0.6.3

O idioma padrão para tradução da caixa de entrada agora pode omitir o espaço, ou seja, //Hello World pode ser traduzido também.

## 0.6.2

A melhoria mais emocionante da caixa de entrada está aqui:

- Digite: // Hello World na caixa de entrada em qualquer página web, depois clique três vezes na barra de espaço para traduzir o parágrafo para inglês
- Também pode especificar a tradução para um determinado idioma: /ja Hello World, depois clique três vezes na barra de espaço para traduzir o parágrafo para japonês

[Clique aqui para uma introdução rápida de 30 segundos](/docs/input/)

## 0.6.0

- Primeiro lançamento em junho, migrado do subdomínio pessoal anterior https://immersive-translate.owenyoung.com para o novo domínio https://immersivetranslate.com/
- A funcionalidade é em grande parte inalterada (novas funcionalidades estarão disponíveis no próximo lançamento!)

## 0.5.17

- Corrigir o problema de que: eBooks bilíngues não têm imagens após a exportação

## 0.5.16

- Corrigir: problema de tradução openai em Chinês Tradicional

## 0.5.15

- Otimizar: O número mínimo de caracteres em um parágrafo que aciona a tradução foi modificado para um mínimo de 4 caracteres para reduzir a confusão, enquanto usa outras funcionalidades para evitar traduzir a navegação e áreas finais do site.
- Corrigir: detalhes do Github não traduzindo após a expansão.

## 0.5.14

- Corrigir o problema de que imagens em algumas páginas web: ficam maiores após a cópia
- Corrigir: seção de comentários do medium não traduzindo
- Corrigir o problema de que imagens em algumas páginas: foram copiadas incorretamente

## 0.5.12

- Feature: O estilo de tradução de linha dividida adiciona uma linha de divisão vertical para traduções de linha única
- Fix: Casos muito raros de divisão de parágrafos.
- Uma excelente página de orientação para configuração inicial para novos utilizadores de iOS.

## 0.5.11

- Suporte à tradução de legendas apenas para exportação de traduções
- Fix: Alguns elementos não são reconhecidos ao passar o mouse
- Fix: Quebras de linha parciais em tweets não reconhecidas
- Fix: Estilo de autoria de eBook não funcionando

## 0.5.10

- Fix: Quebras de linha em tweets não reconhecidas
- Fix: Página de detalhes do Reddit retorna alguns parágrafos que não podem ser traduzidos
- Corrigido um problema com: onde algumas das tags de código não eram reconhecidas corretamente.

## 0.5.9

- Corrige quebras de parágrafo em alguns casos em:
- Fix: Tampermonkey Toggle mostra apenas traduções
- Fix: Problema de estilo de leitura online de eBook não funcionando

## 0.5.8

- Corrige o problema de que: a configuração temporária da duração da tradução do site não tem efeito.

## 0.5.7

- Super atualização!

- A funcionalidade Mostrar Apenas Traduções chegou! Clique em [Mais] -> [Alternar para mostrar apenas traduções].

  - Suporte a atalhos personalizados, configurados em configurações de interface -> Configurações de Atalho

- Otimizar o problema de limitação de frequência de solicitações do OpenAI

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

- Corrige o problema de tela branca após a tradução de sites com hidratação, como Next.js.

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

- Corrigido o problema de tela branca após a tradução de sites com hidratação, como Next.js

- Corrigido o problema em que mudar o atalho de passar o mouse exigia uma atualização da página para ter efeito

- Corrigido o problema com o reconhecimento de quebras de linha em arquivos TXT.

## 0.5.6

- Fix: problema de pop-up de nova aba no macOS.
- Feat: Nova página de guia para novos utilizadores.

## 0.5.5

- Fix: Problema de área de passar o mouse.

## 0.5.4

- Fix: Página Spa duplicada

## 0.5.3

- Fix: Listener de tecla de atalho de passar o mouse.
- Fix: Tradução de documento PDF
- Feat: Adicionar nova página de guia do cliente

## 0.5.2

- Fix: configurações de atalhos de passar o mouse do userscript

## 0.5.1

- Fix: OpenAI API não funciona.

## 0.5.0

- Feat: Traduzir o parágrafo atual ao passar o mouse.
- Feat: Refatorar tradução de PDF, agora você pode traduzir a maioria dos PDFs com Immersive Translate
- Fix: Desativar Menu de Contexto não funcionando [#428](https://github.com/immersive-translate/immersive-translate/issues/428)
- Fix: Evitar Content Security Policy para [Mastondon](https://mastodon.social/)

## 0.4.11

- Fix: permissão de userscript (apenas para userscript).

## 0.4.8

- Feat: Bing Translate para Microsoft Translate para qualidade mais estável.
- Fix: Página web TXT pura como [esta](https://edoras.sdsu.edu/~vinge/misc/singularity.html)
- Performance: Excluir algumas páginas de publicidade infantil no site, e o desempenho melhorou um pouco

## 0.4.7

- Fix: Pop-up de userscript do Firefox ausente.

## 0.4.6

- Feat: Permitir que terceiros enviem evento de documento para chamar `toggleTranslatePage`
- Feat: Aplicativo iOS adiciona botão de ativar extensão e link de comunidades
- UI: Modelo de campo de configurações do OpenAI usa seleção em vez de caixa de entrada de texto.

## 0.4.5

- Fix: Problema de extensão do safari no iOS 15.0.
- Fix: Atalhos de extensão do safari no macOS
- Fix: Pop-up de política de segurança de conteúdo para extensão, e parcialmente para userscript.

## 0.4.4

- Chore: Remover console.log

## 0.4.3

- Fix: Detecção de espaço em branco em tags sup, sub.
- Feat: suporte ao ChatGPT Plus Website como Serviço de Tradução, Este é um recurso beta, então você pode acessá-lo ativando o Recurso Beta nas configurações de desenvolvedor. Isso é muito lento, pois o chatgpt só pode enviar uma solicitação por vez. Certifique-se de ter uma Conta ChatGPT Plus, pois há mais limites na Conta Gratuita, e não tenho certeza se isso traz risco para sua conta, tenha cuidado para Certifique-se de ter uma Conta ChatGPT Plus, pois há mais limites na Conta Gratuita, e não tenho certeza se isso traz risco para sua conta, tenha cuidado ao usá-lo.

## 0.4.1

- Fix: menu de contexto do firefox desapareceu após reiniciar.
- Suporte ao Azure openai

## 0.4.0

- Feat: Suporte a Tradução de Arquivo de Legenda Local (.srt,.ass,etc.)

## 0.3.17

- Feat: Suporte a tradução de arquivo .txt local.
- Fix: Menu de Contexto pode não estar disponível às vezes. [#273](https://github.com/immersive-translate/immersive-translate/issues/273)

## 0.3.16

- Fix: manter &nbsp; como espaço em branco.
- Remover: Remover Papago, pois [o serviço está fora do ar](https://github.com/immersive-translate/immersive-translate/issues/310)

## 0.3.15

- UI: permitir sem chave de API para openai
- UI: permitir que o Open AI redefina para as configurações padrão

## 0.3.14

- Dependência: Atualizar pdf.js para a versão mais recente
- Fix: cor de fundo da seleção de pdf
- Fix: detecção de espaço em branco

## 0.3.13

- Fix: problema de caractere específico do construtor de ebook, como alguns caminhos de capítulo são `xxx' xxxx`.
- UI: dobrar opções personalizadas do openai por padrão.
- UI: Adicionar status de exportação para exportação de epub.
- Fix: Prompt padrão do Gpt4

## 0.3.12

- Feat: Agora podemos personalizar a cor de fundo do tema de tradução do Marcador.
- Fix: postMessage quando a página inicial quebrou alguns sites, agora faremos isso apenas quando realmente traduzirmos páginas
- Fix: problema de progresso do ebook.
- Fix: melhor para dividir parágrafo longo, 1.5 bilhões, 25.5%, Sr. não será considerado como um limite

## 0.3.11

- Fix: cor do texto no modo escuro do leitor de ebook
- Fix: prompt do openAI

## 0.3.10

- Melhor: detectar contêiner japonês/coreano.
- Fix: Progresso do Construtor de Ebook parou em 99%.

## 0.3.9

- Fix: Estado de entrada de serviços de tradução de switch UI de Opções não alterado.

## 0.3.8

- UI: cor de carregamento mais transparente
- Fix: Detectar Idioma do Ebook.
- Feat: Adicionar progresso de tradução para o construtor de ebook, e um belo confete após o sucesso.
- Feat: Adicionar botão de tentar novamente todos os parágrafos falhados.
- Fix: Manipulação de Erro do Deepl

## 0.3.7

- Fix: leitor de ebook não pode carregar imagens no Chrome.

## 0.3.6

- UI: melhor para fazer UI de página de ebook

## 0.3.5

- Fix: exportação de ebook do userscript
- Feat: adicionar endpoint de API personalizado para OpenAI
- Feat: adicionar opções de tempo de tradução temporária do site em `Configurações Avançadas`

## 0.3.4

- CI: Build falhou

## 0.3.3

- Fix: criador de ebook para Kindle
- Alterar: Cor do ícone de carregamento, de preto para azul, para adaptar a página web em modo escuro.
- Feat: Suporte a tradução de html local para extensão

## 0.3.2

- Fix: Movimento do cursor de entrada do Formulário de Opções.
- Feat: OpenAI suporta apiUrl personalizado para configurações de desenvolvedor.

## 0.3.1

- Feat: atualizar ícone escuro para transparência.
- Fix: Ordem errada para parágrafo longo

## 0.3.0

- Versão: A partir de agora, mudaremos o número da versão menor uma vez por mês, por exemplo, agora em março, a versão começará a partir de 0.3.0, em abril, o número da versão começará a partir de 0.3.0, em abril, o número da versão começará a partir de 0.4.0, no próximo abril, o número da versão será 1.4.0, e assim por diante. Isso ocorre porque não faz sentido para extensões seguir Isso ocorre porque não faz sentido para extensões seguir semântica, mas padronizar números de versão de acordo com as leis do tempo é motivação para o desenvolvimento continuar atualizando, e para os utilizadores encontrarem problemas mais facilmente.
- Feat: Suporte a ícone escuro para firefox

## 0.2.86

- Adicionar opção de comprimento máximo de texto por solicitação com Open AI
- Fix: identificador de ebook duplicado
- Feat: Suporte a tradução de página web txt

## 0.2.85

- Fix: alguns arquivos epub não podem ser encontrados.

## 0.2.84

- Feat: Suporte a Leitor e Criador de Ebook

## 0.2.83

- Feat: Permitir que o Formulário de entrada de senha mostre a senha.

## 0.2.82

- Fix: Alguns sites usam `span` para estilos, então usamos `font` em vez de span para o wrapper de alvo de tradução
- Fix: Limite máximo de tokens do OpenAI, alterar caracteres máximos de 1500 para 1300.

## 0.2.81

## 0.2.80

- Feat: Adicionar Menu de Ativar/Desativar para popup -> mais
- Fix: Conflito de Mensagem DingTalk

## 0.2.79

- Fix: Open AI para parágrafo com espaço

## 0.2.78

- Feat: suporte OpenAI CHATGPT 3.5 (suporta interface OpenAI ChatGPT 3.5)
- Feat: Adicionar novo tema Solid Border (新增新主题，实线边框)

## 0.2.77

- Fix: erro de múltiplas tags de código.[#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.76

- Fix: erro de múltiplas tags de código [#178](https://github.com/immersive-translate/immersive-translate/issues/178)

## 0.2.75

- Feat: Suporte para contagem de texto de tradução imediata personalizada para diferentes serviços de tradução.

## 0.2.74

- Feat: Suporte Tencent (alpha)
- Fix: tradução openai
- Fix: verificação de tags desconhecidas inline

## 0.2.73

- Feat: Suporte Tema de Tradução Cinza
- Fix: Página de Tendências do Github

## 0.2.72

- Fix: problema de rede do serviço de tradução de verificação no firefox mobile.

## 0.2.71

- Fix: permissão do userscript Open AI

## 0.2.70

- Fix: placeholder do Open AI

## 0.2.69

- Feat: Suporte Open AI como serviço de tradução.
- Feat: Suporte para verificar serviço de tradução em options.html
- Feat: Suporte para quadro principal personalizado, pois alguns sites não usam o corpo como quadro principal

## 0.2.68

- Suporte Caiyun (Alpha)
- Fix tags de bloco desconhecidas

## 0.2.67

- Feat: Adicionar `<all>` para sempre traduzir idiomas, então agora você pode usá-lo para traduzir todos os idiomas, exceto o idioma alvo, e nunca traduzir idiomas
- Fix: Permitir configuração personalizada da API do Google
- Melhor: Suporte Deepl Free
- Fix: alto uso de memória para userscripts e extensão (removendo opencc zh-CN para zh-TW, em vez disso com Google translate)
- Fix: Relingo [#159] (https://github.com/immersive-translate/immersive-translate/issues/159)
- Fix: configuração de tradução Azure, mas ainda mostra (precisa de configuração)

## 0.2.66

- Fix: tradução de arquivo PDF falhou, Bug da 0.2.60 para suportar deepl de zh-CN para zh-TW

## 0.2.65

- Suporte para limitar solicitações para múltiplos quadros
- Não traduzir título da página quando em iframe

## 0.2.64

- Fix: escolha de serviços de tradução openl
- Feat: Suporte para opção de traduzir título

## 0.2.63

- Feat: Suporte Serviço de Tradução Azure
- Feat: Suporte Serviço de Tradução Papago
- Fix: sincronização do google drive no firefox android nativo.
- Fix: mudar transparência de 0.4 para 0.618 [#147] (https://github.com/immersive-translate/immersive-translate/pull/147)
- Fix: dicas de atalhos do popup
- Performance: solicitações de serial para concorrência
- Melhor para detectar contagem de japonês

## 0.2.62

- Feat: Adicionar regra waitForSelectors, para corrigir alguns sites como reddit

## 0.2.61

- Fix: userscript é muito grande para greasy fork
- Melhor: reduzir tamanho do arquivo

## 0.2.60

- Feat: Suporte zh-CN para zh-TW para Deepl
- Feat: Recurso Deepl de Tradução Imersiva
- Feat: Suporte para zoom de tamanho de fonte personalizado
- Fix: estilo do fórum Steam
- Fix: estilo global não mudou após elementos dinâmicos gerados
- Fix: promover prioridade de exclusão
- UI: mudança na página sobre
- Fix: alguns elementos matemáticos permanecem originais

## 0.2.59

- Fix: Elemento de Bloqueio de Tags Desconhecidas
- Fix: elemento translate=no sobreposto
- Fix: correspondência de URL com múltiplos \*

## 0.2.58

- Feat: Suporte para cor de texto de tradução personalizada, cor da borda.

## 0.2.57

- Sem alterações, reconstruir

## 0.2.56

- Fix tradução duplicada para elementos inline com elemento de código.
- Fix verificação de tags desconhecidas inline/bloco
- Feat: suporte para css injetado no painel do desenvolvedor
- Feat: aparar authKey, appid appSecret
- Melhor: abrir página de configurações em nova aba (mas não para Stay)

## 0.2.55

- Tentar corrigir charset da API deepl

## 0.2.54

- Remover permissão de abas para rejeição da loja do chrome
- Fix traduzir a página inteira, rodapé é ignorado
- Adicionar notas à página sobre
- Suporte para URL personalizado da Configuração embutida

## 0.2.53

- Fix erro de sincronização do google drive no userscript.

## 0.2.52

### Código

- Usar a última versão do esbuild
- Usar a última versão do deno
- CI: enviar código-fonte para firefox

## 0.2.51

- Fix Google Auth Necessita de Login no Chrome/Firefox
- Substituir links de serviço de tradução
- Melhor para permissão.
- remover minify.

## 0.2.50

- Fix problema de upload do google drive (realmente) [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.49

- Remover atalhos alt+d, alt+s pois podem conflitar com atalhos nativos.
- Fix problema de upload do google drive [#81](https://github.com/immersive-translate/immersive-translate/issues/81)

## 0.2.48

- Melhor para velocidade, adicionando minLength para 50 para detecção de idioma.
- Fix validação de token do Google Drive.

## 0.2.47

- Fix API deepl

## 0.2.46

- corrigir marca de bloco

## 0.2.45

- Fix innerText do elemento é indefinido
- Fix tradução caiyun idioma de origem indefinido

## 0.2.44

- Fix alternar máscara do userscript
- Fix lógica de alternar máscara

## 0.2.43

- Fix alternar máscara do userscript com evento de toque.
- Fix velocidade (removendo sleep(300))

## 0.2.42

- Fix máscara ao passar o mouse quando alternar máscara novamente.
- Adicionar atalhos de máscara para mobile
- Fix problema de sincronização em nuvem do userscript
- Mover página de opções avançadas para o menu à esquerda.
- Adicionar lógica de tentativa para serviço de tradução

## 0.2.41

- Fix tradução niu do userscript
- Fix tradução xhtml

## 0.2.40

- Fix exibição de recurso beta
- Fix página de configuração do popup em nova aba
- Fix substituição de placeholder de tradução

## 0.2.39

- Suporte para atalhos para mostrar tradução de máscara
- Suporte para ativar recurso beta no painel do desenvolvedor
- Fix atalhos na extensão móvel

## 0.2.38

- Suporte para tema de carregamento
- Fix getpocket.com
- Fix rodapé lateral para área do corpo
- Fix ícone de importação/exportação

## 0.2.37

- Fix marca de exclusão de quadro

## 0.2.36

- Suporte para sincronização com Google Drive

## 0.2.35

- Fix ignorar tag rb, rt em japonês.
- Melhor para popup ui mais
- Melhor para dicas de userscript ruins
- Adicionar contribuição à página sobre
- Fix tradução volc para detecção automática de idioma

## 0.2.34

- Fix velocidade de múltiplos idiomas

## 0.2.33

- Suporte para modo de escrita vertical, como japonês.
- Adicionar 3 temas
- Adicionar serviço de tradução Niu

## 0.2.32

- Fix tradução básica de PDF
- Fix selecionar um serviço não configurado no popup, ir para a página de opções.
- Fix permanecer aberto configurações.
- Fix velocidade de detecção de múltiplos idiomas

## 0.2.31

- Fix injeção de css em iframe dinâmico

## 0.2.30

- Suporte para tradução de iframe inline do userscript.
- Suporte para tradução shadowroot. Por exemplo:
  https://www\.foxnews.com/politics/minnesota-senate-passes-abortion-bill-opponents-call-most-extreme-nation
  Área de conversa.
- também verificar regra de sincronização no popup

## 0.2.29

- Fix tradução do Facebook
- Suporte para mostrar opção de menu de contexto.

## 0.2.28

- Remover correspondência não padrão para userscript

## 0.2.27

- Suporte para tradução de iframe inline. (Apenas para extensão, não disponível para
  userscript)
- Fix tradução de múltiplos idiomas

## 0.2.26

- Fix addon do firefox android
- Adicionar configurações avançadas para nova linha de tradução

## 0.2.25

- Suporte para tradução de iframe, como QQ mail, tweet incorporado.

## 0.2.24

- Adicionar site de tradução temporária por um tempo
- Fix API do navegador do userscript stay.app
- Fix página de opções do stay.app

## 0.2.23

- Fix tradução de página de múltiplos idiomas

## 0.2.22

- Fix build do userscript

## 0.2.21

- Fix tradução online de pdf no firefox

## 0.2.20

- Fix problema de solicitação de macaco
- Fix marca de linha de destaque

## 0.2.19

- Fix japonês inteligente da tencent
- Fix navegador haikuo world

## 0.2.18

- Fix mudança de URL do cliente, permanecer automaticamente no estado de tradução.
- Remover contêiner lateral como contêiner de tradução.
- Refatorar posição do popup.

## 0.2.17

- Mudar destaque para marca
- Adicionar tema de tradução de destaque

## 0.2.16

- Compatibilidade com Macaque

## 0.2.15

- Fix problema de rebote de toque

## 0.2.14

- Fix globalThis.GM do safari não funcionando

## 0.2.13

- Suporte para Arrastar Popup do Userscript
- Suporte para Três Dedos em dispositivo de toque para acionar alternar páginas de tradução
- Suporte para Ocultar o ícone do popup do userscript.

## 0.2.12

- Melhor para inoreader

## 0.2.11

- Fix
  [#28](https://github.com/immersive-translate/immersive-translate/issues/28)
  Annas archive O conteúdo principal da página não pôde ser traduzido

## 0.2.10

- Fix distância de altura de linha de pdf

## 0.2.9

- Corrigir marca de elementos excluídos
- Corrigir verificação de tipo deno
- remover importmap
- Corrigir tradução de menus de contexto
- restaurar página quando "nunca traduzir este site" estiver ativado
- Adicionar descrição para adicionar URL

## 0.2.8

- Detectar a linguagem do agente do utilizador para a linguagem da interface
- Corrigir bug de quebra de linha.

## 0.2.7

- Corrigir pedido grease monkey

## 0.2.6

- Corrigir
  [#30](https://github.com/immersive-translate/immersive-translate/issues/30),
  problema de correspondência de URL de ficheiro

## 0.2.5

- aumentar versão para teste ci

## 0.2.4

- capturar erro de conexão de mensagem para popup.

## 0.2.3

- Corrigir
  [#26](https://github.com/immersive-translate/immersive-translate/issues/26)
  criar contexto múltiplas vezes

## 0.2.2

- Corrigir ficheiro de exemplo PDF
- Corrigir ficheiro local pdf no Firefox
- Corrigir atalhos pdf

## 0.2.1

- Suporte para Gerenciador de Atalhos Grease Monkey.
- Corrigir regex de correspondência
- Corrigir comentários do youtube.
- Corrigir versão compacta móvel do reddit
- Corrigir problema de tradução de texto completo

## 0.2.0

- Corrigir PDF de duas colunas.
- Corrigir bug da versão da Chrome/Edge Store.
- Corrigir
  [#21](https://github.com/immersive-translate/immersive-translate/issues/21)

## 0.1.2

- Publicar para addon do Firefox
- Publicar para Edge
- corrigir margem do pdf.
- Alterar ficheiro de exemplo pdf

## 0.0.62

- Corrigir formato pdf, indentação.
- Corrigir mudança de elemento em telegra.ph

## 0.0.61

- Corrigir fechamento de elemento span.
- Corrigir permissão para navegador inicial

## 0.0.60

- Corrigir PDF no Chrome

## 0.0.59

- Suporte Inicial para PDF

## 0.0.58

- Editar descrição do tema de tradução

## 0.0.57

- Alterar UI do popup, para facilitar o uso

## 0.0.56

- Corrigir timeout no chrome
- Corrigir erro de divisão de sentença.

## 0.0.55

- Corrigir exibição de elemento none.
- refatorar marca de elemento

## 0.0.54

- Suporte para quebra de linha para X caracteres.

## 0.0.53

- usar sendMessage em vez de connect, pois o chrome desconectará a porta após
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

- Corrigir tradução de img bloqueada.

## 0.0.49

- Corrigir extensão do firefox

## 0.0.48

- Corrigir extensão do chrome

## 0.0.47

- reescrever mensagem com fundo, usar connect em vez de sendMessage
- adicionar suporte móvel para reddit
- corrigir espaço em branco pré para alguns artigos

## 0.0.46

- Formatar informações meta do userscript

## 0.0.45

- userscript usa um arquivo.
- adicionar timeout para pedido de cache

## 0.0.44

- Corrigir erro de divisão tencent.
- Corrigir erro de elemento sup inline.
- Melhor para twitter

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

- Corrigir serviço de tradução contém mock2

## 0.0.38

- Suporte para resultado de Cache para userscript
- Adicionar UI de Opções
- Suporte para detectar mais contêineres de conteúdo

## 0.0.37

- Corrigir mudança de serviço de tradução no popup não funciona
- Corrigir tradução de conteúdo de post móvel do reddit.

## 0.0.36

- Corrigir caractere especial da Wikipedia
  [#6](https://github.com/immersive-translate/next-immersive-translate/issues/6)
- Corrigir tamanho do ícone do userscript.
- habilitar todos os sites para detectar linguagem de parágrafo.

## 0.0.35

- Corrigir youtube ir para a próxima página
- Suporte para página de pesquisa do Youtube.
- Corrigir alternância avançada de opções.
- Corrigir tag img, tag oculta
  [#5](https://github.com/immersive-translate/next-immersive-translate/issues/5)
- Corrigir atualização forçada de pesquisa do Google
  [#4](https://github.com/immersive-translate/next-immersive-translate/issues/4)
- Suporte para resultado de Tabela do Google
  [#3](https://github.com/immersive-translate/next-immersive-translate/issues/3)
- Corrigir espaço em branco na Wikipedia
  [#2](https://github.com/immersive-translate/next-immersive-translate/issues/2)

## 0.0.34

### Alterações de Ruptura

- A tecla de atalho padrão para alternar tradução foi alterada para `alt+A`, pois
  é a tecla mais conveniente para digitar.

### Outros

- Suporte para definir modo de tradução imediata, para que possa deixar a página web traduzir
  o mais rápido possível.
- Suporte para definir área da página que precisa ser traduzida. para que possa traduzir mais área.
- Suporte para definir a primeira contagem de texto x para traduzir imediatamente.
- Corrigir tradução duplicada ao mudar tradução
- Melhor UI do popup

## 0.0.33

- Suporte para mais idiomas, zh-TW, en

## 0.0.32

- Corrigir tradução de ficheiro local após salvo. Corrigido
  [#1](https://github.com/immersive-translate/next-immersive-translate/issues/1)
- Adicionar ficheiro dist js ao repositório público

## 0.0.31

- Suporte para Traduzir a Página Inteira
- Suporte para Traduzir página imediatamente
- Mais UI de Configuração
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
- Corrigir cabeçalho detectado

## 0.0.27

- Suporte para translationTheme

## 0.0.26

- Corrigir permissão de conexão do userscript volc alpha.
- Corrigir versão clicável.

## 0.0.25

- Suporte para selectorMatches, para que possamos corresponder todos os manstondon agora.
- Corrigir erro de userscript no Firefox.

## 0.0.23

- Melhor para detecção de Chinês
- Corrigir problema de innerText no reddit

## 0.0.22

- Suporte para deeplx
- Corrigir tradução múltipla ao mudar serviço

## 0.0.21

- Corrigir algumas tags span são elementos de bloco

## 0.0.20

- Suporte para não traduzir hashtags como #hash, at tags como @xxx, $tag, como $APPL
- Suporte para elemento de bloco

## 0.0.18

- Suporte para deepl, bing, baidu, youdao, volc, openl, caiyun.

## 0.0.13

- Suporte para userscript

## 0.0.4.8

- Corrigir ordem do código.
- Suporte para UI básica do popup

## 0.0.4.6

- Suporte para verificar nova versão

## 0.0.3

- Suporte para ficheiros locais

## 0.0.2

- Suporte para Elementos Dinâmicos
- Suporte para tradução visível