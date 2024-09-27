---
sidebar_position: 9
---

# Perguntas Frequentes - Immersive Translate

## Tradução de Conteúdo em Sites como YouTube e Facebook

**P:** O conteúdo principal é traduzido, mas algumas barras laterais não. Quero traduzir tudo.

**R:** Por padrão, o Immersive Translate traduz apenas a área de conteúdo principal. Para traduzir tudo:

1. Abra o painel da extensão (pressione longamente no celular).
2. Clique em "Mais" no canto inferior direito.
3. Selecione "Todas as áreas".

## Botão Flutuante não Exibido em Aplicativos do YouTube (ou Outros) no Celular

**P:** Por que não vejo o botão flutuante no app do YouTube?

**R:** Plugins de navegador funcionam apenas em navegadores.

- **iOS:** Pressione e segure o link do YouTube para abrir em uma página da web.

## Como Desativar a Tradução Automática?

**R:** Cancele a tradução automática no painel pop-up ou na página de Configurações.

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="como desativar a tradução automática" width="250" />

<!-- - Ou alterando através da página de configurações

![](https://github.com/immersive-translate/immersive-translate/assets/62473795/d33ac7c0-a47b-4901-b5f6-c6a991164dc0) -->

## Não há Permissão para Traduzir a Página Atual

**R:** Isso pode ocorrer em:

- Página padrão do navegador (sem endereço na barra de endereço)
- Página de plugin de terceiros
- Página da Google Store com plugin do Google desativado

## Como Ocultar o Texto Original?

**R:** Abra o painel da extensão, toque em [Mais] e selecione [Mudar para o modo somente tradução].

## Ponto de Exclamação na Página

**R:** Indica um erro no serviço de tradução. Passe o mouse sobre o ponto de exclamação para ver o erro específico.

**Erro 429:** Frequência de solicitações muito rápida. Tente mudar de serviço de tradução ou esperar um pouco. Se usar o Google, mude de nó.

## Tradução de Documentos Locais

**R:** Clique no ícone da extensão, em [Mais], e selecione [Traduzir arquivos PDF] ou [Traduzir arquivos HTML/TXT].

**Chrome (Chrome, Arc, Edge):**

1. Abra `chrome://extensions`.
2. Encontre o plugin [Immersive Translate].
3. Ative [Permitir acesso a URLs de arquivo].
4. Abra o arquivo local no navegador e clique com o botão direito para traduzir.

## Como Atualizar a Extensão?

**R:** Geralmente, as extensões são atualizadas automaticamente. Para atualizar manualmente:

1. Abra [Gerenciar Extensões] no navegador.
2. Ative o [Modo Desenvolvedor].
3. Clique em [Atualizar].

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

## Estilo de Legendas do YouTube

**R:** Ajuste tamanho, cor e outros aspectos nas configurações de legendas do próprio YouTube, em [Opções].

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

## Navegadores Compatíveis com o Immersive Translate Tampermonkey

**Desktop:**

- Chrome e Firefox: [Tampermonkey](https://www.tampermonkey.net/)
- Safari: [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)

<!-- > Se você usa o [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171) no Safari, busque pelo Script de Otimização Immersive Translate para baixar diretamente da loja do Stay (otimizado especificamente para o Stay) -->

**Android:**

1. Instale o [Firefox](https://www.mozilla.org/firefox/browsers/mobile/android/) mais recente.
2. Instale o [Tampermonkey](https://www.tampermonkey.net/).

<!-- 2. Você também pode usar diretamente o [X Browser](https://www.xbext.com/?ref=immersive-translate). Após a instalação, abra o [Endereço do Immersive Translate para o Tampermonkey ](https://download.immersivetranslate.com/immersive-translate.user.js) para instalá-lo! -->

<!-- Extensões Grease Monkey conhecidas por serem incompatíveis:

- Android Via Browser
- iOS Alook Browser -->

## Bloqueio da Interface do Google Tradutor

**R:** Adicione o nome de domínio `translate.googleapis.com` à regra de proxy.

## Atualização das Regras

**R:** A extensão sincroniza as regras automaticamente. Você também pode sincronizar manualmente no painel da extensão.

## Feedback de Problemas na Tradução

**P:** Como salvar o feedback da página da web se eu estiver com problemas com a tradução da página?

**R:** Salve a página como arquivo .mht/.mhtml (Ctrl+S) e envie para support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

## Erro de Tradução na Color Cloud

**R:** Remova a mensagem "Unsupported trans_type" e selecione o idioma para detecção automática.

## Leitura do WeChat não Pode Ser Traduzida

**R:** O WeChat Reading impede o acesso ao conteúdo por terceiros.

## Tradução Acionada não Funciona em um Site Específico

**R:**

- **Poucos visitantes:** Sugira parágrafos para tradução ou adapte o site com [regras do usuário](/docs/advanced/#user-rules).
- **Muitos usuários:** Use a tradução por mouse e relate o problema no grupo.

## Aprimoramento da Caixa de Entrada não Funciona

**R:** A pesquisa do Google deve estar na página [Google](https://www.google.com/), não na página inicial do navegador ou em espaços em branco na barra de endereço.

## Log de Depuração

**R:**

1. Ative o registro de depuração em Painel -> Configurações -> Configurações do desenvolvedor.
2. Abra o console do site (clique com o botão direito e selecione "Inspecionar").
3. Veja os logs no console.

## Como Desativar o Botão Flutuante

**R:**

- Ocultar na página atual
- Definir como "Nunca traduzir este site"
- Ocultar em todas as páginas: Vá em [Página de Configurações] - [Configurações da Interface] e desative [Mostrar Botão Flutuante na Página].

## Erro ao Instalar o Plugin no Chrome

**R:** "Valor inválido para web_accessible_resource[0]" requer Chromium 88 ou superior.

## Como Instalar no Navegador 360?

**R:** Use o 360 Extreme Browser x. Se tiver acesso à loja do Google, instale por lá. Caso contrário, [instale manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

## O Navegador Opera não Funciona

**P:** Não funciona em sites como o google.com e outras páginas de pesquisa. E aparece a seguinte mensagem: `Atualize a página atual antes de iniciar a tradução`, persistindo mesmo depois de atualizar a página.

**R:** Ative "Permitir acesso aos resultados da página de pesquisa" nas configurações do plugin Immersive Translate no Opera.

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

## Legendas Bilíngues no YouTube

**P:** As Legendas Bilíngues do YouTube em Chinês Tradicional não São Exibidas

**R:** Ative [Usar Immersive Translate para traduzir legendas] em [Configurações] [Legendas de vídeo].

## Mais Perguntas

<details>
<summary>Como limpar o cache com Tampermonkey?</summary>

Limpe o cache do site correspondente nas ferramentas do desenvolvedor do navegador.

</details>

<details>
<summary>A solicitação de endereço da interface personalizada do Tampermonkey falhou?</summary>

Declare as permissões no início do script do Tampermonkey, seguindo o modelo de outros nomes de domínio, por exemplo: `@connect api.google.com`.

</details>
