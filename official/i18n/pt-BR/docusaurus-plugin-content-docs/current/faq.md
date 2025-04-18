---
sidebar_position: 9
---

# FAQ

## Relacionado à Segurança

### 1. Aplicativo Android, a bola flutuante desapareceu

Versões antigas de add-ons estão desativadas, desinstale e instale a versão mais recente do [site oficial](https://immersivetranslate.com/).

## Relacionado à Instalação

### 1. Como atualizar a extensão

De modo geral, as extensões instaladas na loja do navegador serão atualizadas automaticamente, geralmente dentro de um dia após a atualização da extensão. Se você quiser atualizar imediatamente para a versão mais recente, pode ir à [página de Gerenciamento de Extensões] do navegador, habilitar o [Modo Desenvolvedor] e clicar em [Atualizar] no topo para atualizar imediatamente para a versão mais recente na loja.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Navegadores compatíveis com Immersive Translate Tampermonkey

iOS:

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Navegador Safari com extensão Tampermonkey instalada, extensões compatíveis:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): Recomenda-se procurar o Script de Otimização do Immersive Translate diretamente na própria loja do Stay (especialmente otimizado para Stay).

Android:

- [Firefox Latest Version](https://www.firefox.com.cn/download/#product-android-release): Após a instalação, instale a extensão [Tamper Monkey](https://www.tampermonkey.net/).
- [X Browser](https://www.xbext.com/?ref=immersive-translate): Após a instalação, abra diretamente o [endereço do script Tampermonkey do Immersive Translate](https://download.immersivetranslate.com/immersive-translate.user.js) para instalar.

Navegadores conhecidos que não suportam extensões Tampermonkey (esses navegadores não implementaram a API Tampermonkey necessária):

- Android Via Browser
- iOS Alook Browser

### 3. Erro ao instalar o instalador de plugin no Chrome

Erro `invalid value for web_accessible_resource[0]`: É necessário que a versão do Chromium seja maior que 88 para suportar manifest_version 3.

### 4. Como instalar o 360 Browser

Apenas o 360 Extreme Browser X é suportado, lembre-se de que é com X. Se você puder acessar a loja de Extensões do Google, pode ir diretamente lá para instalá-lo. Se não puder acessar, [instale manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. O navegador Opera não funciona

Não funciona no google.com e em outras páginas de pesquisa, o plugin exibe `Por favor, atualize a página atual antes de iniciar a tradução` e atualizar a página ainda mostra esta mensagem: Você precisa encontrar "Immersive Translate" nas configurações do plugin Opera e habilitar a opção "Permitir acesso aos resultados da página de pesquisa".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. Não é possível habilitar extensões em dispositivos iOS

Se você não puder habilitar extensões no seu dispositivo iOS, siga estas etapas:

1. Abra o aplicativo [Configurações]
2. Role para baixo e toque em [Tempo de Uso]
3. Selecione [Restrições de Conteúdo e Privacidade]
4. Toque em [Restrições de Conteúdo]
5. Selecione [Conteúdo da Web] e defina como [Sem Restrições]

Se você não precisar dos outros recursos de Restrições de Conteúdo e Privacidade, também pode optar por simplesmente desativar as Restrições de Conteúdo e Privacidade:

1. Abra o aplicativo [Configurações]
2. Selecione [Tempo de Uso]
3. Desative [Restrições de Conteúdo e Privacidade]

### 7. Página de configurações do Safari continua carregando

Configurações do Sistema -> Navegador Safari -> Avançado -> Dados do Site -> Editar, encontre immersivetranslate.com e exclua-o.

### 8. Após instalar o iOS18, redirecionado para página em branco ao fazer login na página de configurações

Pressione longamente a bola flutuante e clique no avatar para fazer login.

### 9. "Arquivo não existe" ao arrastar arquivo crx para extensões do navegador

Você precisa primeiro extrair o arquivo zip, depois arrastar apenas o arquivo CRX.

### 10. Por que o download do crx está instalando a versão 1.13.5 em vez da mais recente

Porque seu mecanismo Chrome foi detectado como estando abaixo da versão 115, que não suporta alguns recursos avançados do plugin, então ele automaticamente faz o downgrade para a versão 1.13.5.

## Relacionado à Tradução Básica

### 1. O conteúdo principal em sites como Youtube, Facebook é traduzido, mas algumas barras laterais não, eu quero traduzir tudo

Para a legibilidade da página, a tradução imersiva por padrão traduz apenas a área de conteúdo principal. Se você quiser traduzir todas as áreas:

Abra o painel da bola flutuante (pressione longamente no celular) -> Clique em mais no canto inferior direito -> Selecione todas as áreas.

### 2. Bolha Flutuante Não Exibida em Aplicativos no Celular

- O plugin Immersive Translate é um plugin de navegador que pode **apenas rodar em navegadores**, ele não pode ser usado em outros aplicativos, e não suporta tradução dentro de outros aplicativos.

- O plugin funciona apenas no navegador onde está instalado e **não pode funcionar entre navegadores** (por exemplo, instalar no Safari não permite que você o use no Chrome)

### 3. Clicar no YouTube no navegador iOS abre diretamente o App

Pressione e segure o link do YouTube para abrir uma janela flutuante e escolha abrir em uma página da web.

### 4. Como desativar a tradução automática

- Cancele no painel Popup ou na página de Configurações.
- Ou altere através da página de configurações

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="desativar tradução automática" width="250" />

### 5. Sem permissão para traduzir a página atual

- Página padrão do navegador (sem endereço na barra de endereços)
- Página de plugin de terceiros
- Plugin do Google desativa a página da loja do Google

### 6. Como não mostrar o texto original?

Toque no ícone do Immersive Translate para abrir o painel de expansão, toque em [Mais], [Mudar para Modo Somente Tradução].

### 7. Exclamação aparece na página

Um ponto de exclamação na página indica que o serviço de tradução encontrou um problema e retornou um erro. Você pode mover o mouse sobre o ponto de exclamação para ver o erro específico.

#### Exemplo: Erro 429

Este é um dos erros mais comuns, 429 indicando que a frequência de solicitações é muito rápida. A tradução de páginas da web tem um número muito grande de parágrafos a serem traduzidos, embora tenhamos feito uma grande otimização, incluindo a fusão de parágrafos, controle de frequência, etc., mas às vezes ainda há alguns serviços de tradução que estão sobrecarregados, retornando um erro de limite de frequência 429. Nesse caso, você geralmente pode mudar temporariamente para outros serviços de tradução, ou esperar um pouco e tentar novamente.

Se você estiver usando o serviço do Google e estiver enfrentando um erro 429, geralmente é um caso de o Google fazer um limite de tráfego contra o seu nó, e é recomendável mudar de nó.

### 8. Como mudar a fonte de tradução e o idioma de destino

No celular, pressione longamente a bola flutuante; no desktop, mova o mouse para a bola flutuante para abrir as configurações, selecione outro serviço de tradução/outro idioma de destino.

### 9. Problema de Interface do Google Translate Bloqueada

Por favor, adicione o domínio `translate.googleapis.com` à regra de proxy.

### 10. A proibição da OpenAI sobre Chaves de API na China afeta os serviços de IA para membros

Sem impacto, o produto usa Azure Enterprise OpenAI, que não está sujeito a restrições regionais de API.

### 11. Erro de Tradução da Color Cloud

Clicar na mensagem de erro `?` mostra "trans_type não suportado". Você pode selecionar manualmente para definir o idioma detectado automaticamente para um idioma específico.

### 12. Leitura do WeChat Não Pode Ser Traduzida

Não pode ser traduzida porque a Leitura do WeChat fez um processamento especial para o conteúdo para impedir o acesso ao conteúdo por meios de terceiros.

### 13. Alguns conteúdos em páginas da web não são traduzidos

Geralmente, é porque o administrador do site definiu áreas para não serem traduzidas usando `translate="no"` ou `notranslate class`, mas você pode resolver isso:

1. Habilitando a função de passar o mouse
2. Usando o passar do mouse para forçar a tradução do conteúdo do parágrafo naquela área

### 14. Acionar tradução não surte efeito

Quando outros sites podem ser traduzidos, mas um site específico não pode:

- Se este site tem menos visitantes
  - É sugerido traduzir parágrafos passando o mouse
  - Se você precisar traduzir o site inteiro, pode adaptá-lo via [regras de usuário](/docs/advanced/#user-rules)
- Se este site é usado por muitas pessoas
  - Você pode começar usando o passar do mouse para traduzir
  - Relate no grupo, e ele será adaptado posteriormente

### 15. Como salvo meu feedback da página da web se tiver problemas com a tradução da página da web?

Você precisa clicar com o botão direito em "Salvar como" ou usar o atalho Ctrl+S na página da web, escolher arquivo único para opção de salvar e salvar com o formato de arquivo .mht/.mhtml. Em seguida, envie o arquivo para support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Feedback do log de depuração

1. Habilite o registro de depuração: Abra o Painel -> Configurações -> Configurações do Desenvolvedor -> Habilitar "Imprimir log de depuração no console".
2. Abra o console do site: Clique com o botão direito para abrir a inspeção -> Mude para o console no topo da coluna direita -> Execute a ação para ver os logs.

### 17. Como desativar a bola flutuante

- Ocultar na página atual: Defina como "Nunca traduzir este site"
- Ocultar em todas as páginas: Abra [Página de Configurações] - [Configurações de Interface] e desative [Mostrar Bola Flutuante na Página]

### 18. Função de tradução ao passar o mouse + tecla de atalho não funciona

Para habilitar a função de tradução ao passar o mouse mais tecla de atalho, a página deve primeiro ter foco. Se você achar que a função não está sendo acionada, tente estas etapas:

1. Clique em qualquer lugar da página uma vez para garantir que a página tenha foco.
2. Tente usar o passar do mouse e a tecla de atalho para tradução novamente.
3. Se a função de tradução ainda não responder, verifique se suas configurações de tecla de atalho estão corretas.

### 19. Como atualizar as regras mais recentes

A extensão em si irá sincronizar regularmente com as regras de adaptação mais recentes do site oficial quando você a usar. Você também pode sincronizar manualmente com as regras mais recentes clicando no ícone da Extensão Immersive Translate no navegador para abrir uma janela pop-up onde a extensão detectará automaticamente as regras de adaptação mais recentes e sincronizará com elas. O mesmo se aplica aos scripts Tampermonkey.

### 20. Tradução falha / Tradução continua girando

1. Verifique a razão da falha:
   - Se o limite de cota for atingido, significa que a cota mensal do membro para essa fonte de tradução está esgotada.
   - Se a tradução mostrar um erro de rede, primeiro verifique o status do seu nó/rede.

2. Altere a fonte de tradução: pressione longamente a bola flutuante para selecionar outra fonte de tradução.

### 21. Como verificar a cota e o uso de tradução do membro Pro

- Membros Pro desfrutam de uma cota base de tradução de 20 milhões de Tokens por mês, que pode ser usada para todos os serviços de tradução. Seja usando tudo para DeepL (equivalente a 20 milhões de caracteres), tudo para OpenAI (20 milhões de Tokens), ou uma mistura de vários serviços, você pode alocar livremente a cota de acordo com suas necessidades reais.

  > A precificação do OpenAI é baseada em tokens. Para texto em inglês, 1 token é aproximadamente 4 caracteres ou 0,75 palavras. Normalmente, 1000 Tokens equivalem a cerca de 750 palavras em inglês ou 400-500 caracteres chineses.

- Endereço de consulta de uso: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Por que a qualidade da tradução do Google no plugin não é tão boa quanto a tradução da página web do Google

Porque o plugin utiliza a API gratuita do Google, que é uma API antiga que o Google não mantém continuamente, enquanto a tradução oficial da página web do Google é mantida continuamente. Teoricamente, a qualidade não é tão boa quanto a tradução oficial do Google, e recentemente a qualidade da tradução da API gratuita do Google diminuiu significativamente. Recomendamos mudar para outros serviços de tradução, e estamos ativamente buscando soluções alternativas. Discussão relacionada: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Mostrando modo de toque quando em modo de mouse

Em [Configurações Avançadas](https://dash.immersivetranslate.com/#advanced), ative o modo apenas para mouse. A versão 1.14.9 otimizará essa detecção de modo.

## Tradução de Vídeo Relacionada

### 1. Configuração de estilo de legendas do Youtube

Você pode clicar nas configurações de legendas do próprio Youtube, [Opções], e então ajustar o tamanho, cor, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. Legendas bilíngues do YouTube em chinês tradicional não são exibidas

O YouTube vem com legendas traduzidas por máquina, e o Chinês Tradicional terá erros de formatação, fazendo com que todas as legendas apareçam com uma grande seção de legendas no início. Com base nesse cenário, é recomendado ativar a opção [Usar Immersive Translate para Traduzir Legendas] em [Configurações] [Legendas de Vídeo].

### 3. Como habilitar a tradução de legendas para Bilibili

Ao traduzir legendas de vídeo do Bilibili, siga estas etapas:

1. Primeiro, ative as legendas embutidas do Bilibili clicando no botão "Legenda" no canto inferior direito do player. Se o vídeo não tiver botão de legenda ou conteúdo de legenda, legendas bilíngues não são suportadas.
2. Clique no ícone "Immersive Translate" no player para ativar o recurso de legendas bilíngues.

Nota ao usar:

1. Certifique-se de que as legendas embutidas do Bilibili estejam ativadas.
2. Certifique-se de que o idioma alvo do Immersive Translate seja diferente do idioma das legendas embutidas do Bilibili para acionar a função de tradução.

### 4. Tradução de legendas da Netflix usando o estilo original de legendas

- A abordagem atual da Netflix usa tradução progressiva, com estilo de legenda auto-hospedado, e não suporta legendas manuais.
- A abordagem antiga requer esperar que todas as legendas sejam traduzidas antes de exibi-las, mas suporta legendas manuais.

Para reverter para a abordagem antiga, vá para [[Configurações de Desenvolvedor](https://dash.immersivetranslate.com/#developer)], encontre [Editar Regras de Usuário] e adicione a seguinte regra:

```json
[
  {
    "id": "netflix",
    "subtitleRule.add": {
      "attachRule": {
        "appendSelector": ""
      }
    }
  }
]
```

## Tradução de Arquivos Relacionada

### 1. Tradução de documentos locais

- Método 1: Vá para o [site de Tradução de Arquivos do Immersive Translate](https://app.immersivetranslate.com/), ou clique no ícone da extensão Immersive Translate e clique em [Tradução de Arquivos] para entrar.

- Método 2: Se você estiver usando navegadores semelhantes ao Chrome, como (Chrome, Arc, navegador Edge), há outra maneira: abra a página de gerenciamento de extensões do navegador `chrome://extensions`, encontre o plugin [Immersive Translate], [Permitir que a extensão acesse arquivos locais], e então diretamente no navegador para abrir o arquivo HTML local ou PDF local, você pode clicar com o botão direito [Tradução].

**Nota**: O navegador Safari tem restrições rigorosas sobre o acesso de extensões a arquivos locais. Usuários do Safari devem usar diretamente o Método 1 - vá para o [site de Tradução de Arquivos do Immersive Translate](https://app.immersivetranslate.com/) para traduzir arquivos locais.

### 2. Tradução de PDF é lenta quando há muitas páginas

Recomenda-se dividir o documento em várias partes de menos de 100 páginas cada, traduzi-las separadamente e depois mesclá-las após a tradução.

### 3. Traduções duplicadas ou sobrepostas em PDF

Isso se deve a problemas de reconhecimento do arquivo de origem. Atualmente, recomenda-se clicar manualmente nessa seção e excluir as caixas de texto extras. Continuaremos a otimizar essa situação em futuras atualizações.

### 4. Existe um glossário / tradução especial ou não tradução para certos termos

A versão 1.16.1+ suporta o recurso [Biblioteca de Terminologia AI](https://dash.immersivetranslate.com/#terms).

A biblioteca de terminologia AI não suporta terminologia de tradução automática do Google/Microsoft por padrão.

Método para forçar a ativação:
(ps: a tradução automática usa substituição de espaço reservado, a terminologia pode reduzir a qualidade da tradução)

Vá para [[Configurações de Desenvolvedor](https://dash.immersivetranslate.com/#developer)] -> [Editar Configuração Completa do Usuário]

```
{
  ....
  "enableMachineTranslateTerms":true,
  ...
}
```

### 5. Não é possível exportar arquivos Word traduzidos no formato Word

Atualmente, há alguns problemas técnicos com a exportação de arquivos Word. Recomenda-se manter o formato existente. Estamos continuamente trabalhando na otimização.

### 6. Como ajustar o tamanho mínimo da fonte em PDFs

Isso se deve à restrição de tamanho mínimo de fonte do navegador. Ajuste a fonte do navegador para a configuração mais baixa. Para o Chrome, por exemplo: clique em [Configurações de tamanho de fonte do Chrome](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Tradução de Caixa de Entrada Relacionada

### 1. O aprimoramento da caixa de entrada não surte efeito

- Navegadores conhecidos por não serem suportados: Veja a seção de compatibilidade de [Tradução de Caixa de Entrada](https://immersivetranslate.com/docs/input/)
- Não é possível traduzir na barra de URL ou na página inicial do navegador, apenas suporta barras de pesquisa. Você pode testar em https://www.bing.com/
- Tente pressionar a tecla de espaço mais rapidamente

## Pagamento Relacionado

### 1. Posso usar o WeChat Pay

Pagamentos via WeChat exigem que você envie uma mensagem privada para membros da equipe no grupo e anote "pagamento WeChat". Após a equipe fornecer o código QR de pagamento, faça o pagamento e forneça os detalhes do pagamento. A equipe fornecerá o código de resgate de associação anual/mensal necessário, que pode ser resgatado na [Página de Resgate de Membros](https://immersivetranslate.com/exchange/)

### 2. Posso obter uma fatura

Atualmente, apenas associações anuais podem receber faturas. Usuários que já pagaram e precisam de uma fatura devem enviar uma mensagem privada para membros da equipe no grupo e anotar "emissão de fatura". Usuários não pagos podem verificar: [Informações de Fatura de Associação Anual](https://immersivetranslate.com/bill/)

## Mais perguntas (incomuns)

<details>
<summary>Como limpar meu cache com Tampermonkeys?</summary>
<p>
Devido à limitação da API do Tampermonkeys, o cache do Immersive Translate Tampermonkeys será salvo no cache do site correspondente, então se você quiser limpá-lo, pode abrir o painel de ferramentas de desenvolvedor do site correspondente no seu navegador e então limpar o cache desse site.
</p>
</details>

<details>
<summary>Falha na solicitação de endereço de interface personalizada do Tampermonkey?</summary>
<p>
Tampermonkeys exigem que todas as solicitações do script precisem declarar permissões no início do script, por exemplo: `@connect api.google.com`, então se você precisar adicionar um novo nome de domínio que não seja o padrão, por favor, declare-o no início do Tampermonkey modelado após o outro nome de domínio.
</p>
</details>

<details>
<summary>Plugin do navegador Edge abre em branco e o navegador relata erro MANIFEST-000001</summary>
<p>
Abra o aplicativo [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/), procure por `amkbmndfnliijdhojkpoglbnaaahippg` (o ID da extensão Immersive) na pasta de armazenamento do navegador, exclua-a, depois desinstale e reinstale o plugin.
</p>
</details>

<details>
<summary>Como baixar legendas bilíngues / As legendas bilíngues podem ser baixadas de outros sites?</summary>
<p>
- Atualmente, o download de legendas é suportado apenas em desktop.
- Incluindo YouTube, quando há um botão de download de legendas, o site atual suporta download de legendas bilíngues.
</p>
</details>