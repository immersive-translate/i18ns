---
sidebar_position: 9
---

# FAQ

## Relacionado com Segurança

### 1. Aplicação Android, a bola flutuante desapareceu

As extensões de versões antigas estão desativadas, desinstale e instale a versão mais recente a partir do [site oficial](https://immersivetranslate.com/).

## Relacionado com Instalação

### 1. Como atualizar a extensão

De modo geral, as extensões instaladas na loja do navegador serão atualizadas automaticamente, geralmente dentro de um dia após a atualização da extensão. Se quiser atualizar imediatamente para a versão mais recente, pode ir à [Gestão de Extensões] do navegador, ativar o [Modo de Desenvolvedor] e clicar em [Atualizar] no topo para atualizar imediatamente para a versão mais recente na loja.

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/update-extension.png)

### 2. Navegadores suportados pelo Immersive Translate Tampermonkey

iOS:

- [Tamper Monkey Browser](https://www.tampermonkey.net/)
- Navegador Safari com a extensão Tampermonkey instalada, extensões compatíveis:
  - [Userscripts](https://itunes.apple.com/us/app/userscripts/id1463298887)
  - [Stay](https://apps.apple.com/cn/app/stay-safari%E6%B5%8F%E8%A7%88%E5%99%A8%E4%BC%B4%E4%BE%A3/id1591620171): Recomenda-se procurar diretamente o Script de Otimização do Immersive Translate na própria loja do Stay (especialmente otimizado para o Stay).

Android:

- [Firefox Latest Version](https://www.firefox.com.cn/download/#product-android-release): Após a instalação, instale a extensão [Tamper Monkey](https://www.tampermonkey.net/).
- [X Browser](https://www.xbext.com/?ref=immersive-translate): Após a instalação, abra diretamente o [endereço do script do Immersive Translate Tampermonkey](https://download.immersivetranslate.com/immersive-translate.user.js) para instalar.

Navegadores conhecidos que não suportam extensões Tampermonkey (estes navegadores não implementaram a API Tampermonkey necessária):

- Android Via Browser
- iOS Alook Browser

### 3. Erro ao instalar o instalador de plugins no Chrome

Erro `invalid value for web_accessible_resource[0]`: É necessário uma versão do Chromium superior a 88 para suportar manifest_version 3.

### 4. Como instalar o 360 Browser

Apenas o 360 Extreme Browser X é suportado, lembre-se que é com X. Se puder aceder à loja de Extensões do Google, pode ir diretamente lá para instalá-lo. Se não puder aceder, [instale manualmente](/docs/installation/#manual-installation-to-keep-track-of-the-latest-development-features).

### 5. O navegador Opera não funciona

Não funciona no google.com e em outras páginas de pesquisa, o plugin exibe `Por favor, atualize a página atual antes de iniciar a tradução` e atualizar a página ainda mostra esta mensagem: Você precisa encontrar "Immersive Translate" nas configurações do plugin Opera e ativar a opção "Permitir acesso aos resultados da página de pesquisa".

<!-- ![](https://s.immersivetranslate.com/static/official-static/assets/opera-allow-search.png) -->

### 6. Não é possível ativar extensões em dispositivos iOS

Se não conseguir ativar extensões no seu dispositivo iOS, siga estes passos:

1. Abra a aplicação [Definições]
2. Desça e toque em [Tempo de Ecrã]
3. Selecione [Restrições de Conteúdo e Privacidade]
4. Toque em [Restrições de Conteúdo]
5. Selecione [Conteúdo Web] e defina para [Sem Restrições]

Se não precisar das outras funcionalidades das Restrições de Conteúdo e Privacidade, também pode optar por simplesmente desativar as Restrições de Conteúdo e Privacidade:

1. Abra a aplicação [Definições]
2. Selecione [Tempo de Ecrã]
3. Desative [Restrições de Conteúdo e Privacidade]

### 7. Página de configurações do Safari continua a carregar

Definições do Sistema -> Navegador Safari -> Avançado -> Dados do Website -> Editar, encontre immersivetranslate.com e elimine-o.

### 8. Após instalar o iOS18, redirecionado para página em branco ao fazer login a partir da página de configurações

Pressione longamente a bola flutuante e clique no avatar para fazer login.

### 9. "Arquivo não existe" ao arrastar arquivo crx para extensões do navegador

É necessário primeiro extrair o arquivo zip, depois arrastar apenas o arquivo CRX.

### 10. Por que o download do crx está instalando a versão 1.13.5 em vez da mais recente

Porque o seu motor Chrome foi detectado como estando abaixo da versão 115, que não suporta alguns recursos avançados do plugin, então ele faz automaticamente o downgrade para a versão 1.13.5.

## Relacionado com Tradução Básica

### 1. O conteúdo principal em sites como Youtube, Facebook é traduzido, mas algumas barras laterais não, quero traduzir tudo

Para a legibilidade da página, a tradução imersiva por padrão traduz apenas a área de conteúdo principal. Se quiser traduzir todas as áreas:

Abra o painel da bola flutuante (pressione longamente no celular) -> Clique em mais no canto inferior direito -> Selecione todas as áreas.

### 2. Bolha Flutuante Não Exibida em Aplicações no Celular

- O plugin Immersive Translate é um plugin de navegador que pode **apenas ser executado em navegadores**, não pode ser usado em outras aplicações, e não suporta tradução dentro de outras aplicações.

- O plugin funciona apenas no navegador onde está instalado e **não pode funcionar entre navegadores** (por exemplo, instalando no Safari não permite usá-lo no Chrome)

### 3. Clicar no YouTube no navegador iOS abre diretamente a App

Pressione e segure o link do YouTube para abrir uma janela flutuante e escolha abrir em uma página web.

### 4. Como desativar a tradução automática

- Cancele no painel Popup ou na página de Configurações.
- Ou altere através da página de configurações

<img src="https://s.immersivetranslate.com/assets/turn_off_automatic_translation_en.jpeg" alt="desativar tradução automática" width="250" />

### 5. Sem permissão para traduzir a página atual

- Página padrão do navegador (sem endereço na barra de endereços)
- Página de plugin de terceiros
- Plugin do Google desativa a página da loja do Google

### 6. Como não mostrar o texto original?

Toque no ícone do Immersive Translate para abrir o painel de expansão, toque em [Mais], [Mudar para Modo Apenas Tradução].

### 7. Aparece um ponto de exclamação na página

Um ponto de exclamação na página indica que o serviço de tradução encontrou um problema e retornou um erro. Pode mover o mouse sobre o ponto de exclamação para ver o erro específico.

#### Exemplo: Erro 429

Este é um dos erros mais comuns, 429 indicando que a frequência de pedidos é muito rápida. A tradução de páginas web tem um número muito grande de parágrafos a serem traduzidos, embora tenhamos feito uma grande otimização, incluindo a fusão de parágrafos, controle de frequência, etc., mas às vezes ainda há alguns serviços de tradução que estão sobrecarregados, retornando um erro de limite de frequência 429. Neste caso, geralmente pode mudar temporariamente para outros serviços de tradução, ou esperar um pouco e tentar novamente.

Se estiver a usar o serviço do Google e a experimentar um erro 429, geralmente é um caso de o Google fazer um limite de tráfego contra o seu nó, e é recomendado mudar de nó.

### 8. Como mudar a fonte de tradução e o idioma de destino

No celular, pressione longamente a bola flutuante; no desktop, mova o mouse para a bola flutuante para abrir as configurações, selecione outro serviço de tradução/outro idioma de destino.

### 9. Problema de Interface do Google Translate Bloqueada

Por favor, adicione o domínio `translate.googleapis.com` à regra de proxy.

### 10. A proibição da OpenAI sobre API Keys na China afeta os serviços de IA para membros

Sem impacto, o produto usa Azure Enterprise OpenAI, que não está sujeito a restrições regionais de API.

### 11. Erro de Tradução da Nuvem de Cores

Clicar na mensagem de erro `?` mostra "trans_type não suportado". Pode selecionar manualmente para definir o idioma detectado automaticamente para um idioma específico.

### 12. Leitura do WeChat Não Pode Ser Traduzida

Não pode ser traduzida porque a Leitura do WeChat fez um processamento especial para o conteúdo para impedir o acesso ao conteúdo através de meios de terceiros.

### 13. Alguns conteúdos em páginas web não são traduzidos

Geralmente, é porque o administrador do site definiu áreas para não serem traduzidas usando `translate="no"` ou `notranslate class`, mas pode resolver isso:

1. Ativando a função de passar o mouse
2. Usando o passar do mouse para forçar a tradução do conteúdo do parágrafo nessa área

### 14. Acionar tradução não tem efeito

Quando outros sites podem ser traduzidos, mas um site específico não pode:

- Se este site tem menos visitantes
  - É sugerido traduzir parágrafos passando o mouse
  - Se precisar traduzir o site inteiro, pode adaptá-lo via [regras de usuário](/docs/advanced/#user-rules)
- Se este site é usado por muitas pessoas
  - Pode começar usando o passar do mouse para traduzir
  - Relate no grupo, e será adaptado mais tarde

### 15. Como salvo o meu feedback da página web se tiver problemas com a tradução da página web?

É necessário clicar com o botão direito em "Salvar como" ou usar o atalho Ctrl+S na página web, escolher arquivo único para opção de salvar, e salvar com o formato de arquivo .mht/.mhtml. Depois envie o arquivo para support@immersivetranslate.com.

<!-- ![save mht](https://s.immersivetranslate.com/static/official-static/assets/save_mht.png) -->

### 16. Feedback do log de depuração

1. Ative o registro de depuração: Abra o Painel -> Configurações -> Configurações de Desenvolvedor -> Ative "Imprimir log de depuração no console".
2. Abra o console do site: Clique com o botão direito para abrir a inspeção -> Mude para o console no topo da coluna direita -> Realize a ação para ver os logs.

### 17. Como desativar a bola flutuante

- Ocultar na página atual: Defina para "Nunca traduzir este site"
- Ocultar em todas as páginas: Abra [Página de Configurações] - [Configurações de Interface] e desative [Mostrar Bola Flutuante na Página]

### 18. Função de tradução de passar o mouse + tecla de atalho não funciona

Para ativar a função de tradução de passar o mouse mais tecla de atalho, a página deve primeiro ter foco. Se encontrar que a função não está a ser acionada, tente estes passos:

1. Clique em qualquer lugar na página uma vez para garantir que a página tem foco.
2. Tente usar o passar do mouse e a tecla de atalho para tradução novamente.
3. Se a função de tradução ainda não responder, verifique se as suas configurações de tecla de atalho estão corretas.

### 19. Como atualizar as regras mais recentes

A extensão em si irá sincronizar regularmente com as regras de adaptação mais recentes do site oficial quando a usar. Também pode sincronizar manualmente com as regras mais recentes clicando no ícone da Extensão Immersive Translate no navegador para abrir uma janela popup onde a extensão irá automaticamente detectar as regras de adaptação mais recentes e sincronizar com elas. O mesmo se aplica aos scripts Tampermonkey.

### 20. Tradução falha / Tradução continua a girar

### 21. Como verificar a quota e uso de tradução para membros Pro

- Os membros Pro desfrutam de uma quota base de tradução de 20 milhões de Tokens por mês, que pode ser usada para todos os serviços de tradução. Quer use tudo para DeepL (equivalente a 20 milhões de caracteres), tudo para OpenAI (20 milhões de Tokens), ou uma mistura de múltiplos serviços, pode alocar livremente a quota de acordo com as suas necessidades reais.

  > A precificação do OpenAI é baseada em tokens. Para texto em inglês, 1 token é aproximadamente 4 caracteres ou 0,75 palavras. Normalmente, 1000 Tokens equivalem a cerca de 750 palavras em inglês ou 400-500 caracteres chineses.

- Endereço de consulta de uso: [https://immersivetranslate.com/accounts/usage](https://immersivetranslate.com/accounts/usage)

### 22. Por que a qualidade da tradução do Google no plugin não é tão boa quanto a tradução na página web do Google

Porque o plugin utiliza a API gratuita do Google, que é uma API antiga que o Google não mantém continuamente, enquanto a tradução oficial da página web do Google é mantida continuamente. Teoricamente, a qualidade não é tão boa quanto a tradução oficial do Google, e recentemente a qualidade da tradução da API gratuita do Google diminuiu significativamente. Recomendamos mudar para outros serviços de tradução, e estamos ativamente procurando soluções alternativas. Discussão relacionada: [#2574](https://github.com/immersive-translate/immersive-translate/issues/2547)

### 23. Mostrando modo de toque quando em modo de rato

Em [Configurações Avançadas](https://dash.immersivetranslate.com/#advanced), ative o modo apenas para rato. A versão 1.14.9 otimizará esta detecção de modo.

## Relacionado à Tradução de Vídeo

### 1. Estilo de configuração de legendas do Youtube

Pode clicar nas configurações de legendas próprias do Youtube, [Opções], e então pode ajustar o tamanho, cor, etc.

![](https://s.immersivetranslate.com/assets/youtube_subtitle_options2_en.jpeg)

### 2. Legendas bilíngues do YouTube em chinês tradicional não são exibidas

O YouTube vem com legendas traduzidas por máquina, e o Chinês Tradicional terá erros de formatação, fazendo com que todas as legendas apareçam com uma grande seção de legendas no início. Com base neste cenário, é recomendado ativar a opção [Usar Immersive Translate para Traduzir Legendas] em [Configurações] [Legendas de Vídeo].

### 3. Como ativar a tradução de legendas para Bilibili

Ao traduzir legendas de vídeo do Bilibili, siga estes passos:

1. Primeiro, ative as legendas embutidas do Bilibili clicando no botão "Legenda" no canto inferior direito do player. Se o vídeo não tiver botão de legenda ou conteúdo de legenda, legendas bilíngues não são suportadas.
2. Clique no ícone "Immersive Translate" no player para ativar o recurso de legendas bilíngues.

Nota ao usar:

1. Certifique-se de que as legendas embutidas do Bilibili estão ativadas.
2. Certifique-se de que a língua alvo do Immersive Translate é diferente da língua das legendas embutidas do Bilibili para acionar a função de tradução.

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

## Relacionado à Tradução de Arquivos

### 1. Tradução de documentos locais

- Método 1: Vá para o [site de Tradução de Arquivos Immersive Translate](https://app.immersivetranslate.com/), ou clique no ícone da extensão Immersive Translate e clique em [Tradução de Arquivos] para entrar.

- Método 2: Se estiver a usar navegadores semelhantes ao Chrome, como (Chrome, Arc, Edge), há outra maneira: abra a página de gestão de extensões do navegador `chrome://extensions`, encontre o plugin [Immersive Translate], [Permitir que a extensão acesse arquivos locais], e então diretamente no navegador para abrir o arquivo HTML local ou PDF local, pode clicar com o botão direito [Tradução].

**Nota**: O navegador Safari tem restrições rigorosas sobre o acesso de extensões a arquivos locais. Os usuários do Safari devem usar diretamente o Método 1 - vá para o [site de Tradução de Arquivos Immersive Translate](https://app.immersivetranslate.com/) para traduzir arquivos locais.

### 2. A tradução de PDF é lenta quando há muitas páginas

Recomenda-se dividir o documento em várias partes de menos de 100 páginas cada, traduzi-las separadamente e depois juntá-las após a tradução.

### 3. Traduções duplicadas ou sobrepostas em PDF

Isto deve-se a problemas de reconhecimento do arquivo de origem. Atualmente, recomenda-se clicar manualmente nessa seção e excluir as caixas de texto extras. Continuaremos a otimizar esta situação em futuras atualizações.

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

Atualmente, há alguns problemas técnicos com a exportação de arquivos Word. Recomenda-se manter o formato existente. Estamos continuamente a trabalhar na otimização.

### 6. Como ajustar o tamanho mínimo da fonte em PDFs

Isto deve-se à restrição de tamanho mínimo de fonte do navegador. Ajuste a fonte do navegador para a configuração mais baixa. Para o Chrome, por exemplo: clique em [Configurações de tamanho de fonte do Chrome](chrome://settings/fonts?search=%E5%AD%97%E5%8F%B7)

## Relacionado à Tradução de Caixa de Entrada

### 1. O aprimoramento da caixa de entrada não surte efeito

- Navegadores conhecidos por não serem suportados: Veja a seção de compatibilidade de [Tradução de Caixa de Entrada](https://immersivetranslate.com/docs/input/)
- Não é possível traduzir na barra de URL ou na página inicial do navegador, apenas suporta barras de pesquisa. Pode testar em https://www.bing.com/
- Tente pressionar a tecla de espaço mais rapidamente

## Relacionado ao Pagamento

### 1. Posso usar o WeChat Pay

Os pagamentos via WeChat exigem que os membros do grupo enviem mensagens privadas aos funcionários e anotem "pagamento WeChat". Após os funcionários fornecerem o código QR de pagamento, faça o pagamento e forneça os detalhes do pagamento. Os funcionários fornecerão o código de resgate de associação anual/mensal necessário, que pode ser resgatado na [Página de Resgate de Membros](https://immersivetranslate.com/exchange/)

### 2. Posso obter uma fatura

Atualmente, apenas associações anuais podem receber faturas. Usuários que já pagaram e precisam de uma fatura devem enviar mensagens privadas aos funcionários do grupo e anotar "emissão de fatura". Usuários não pagos podem verificar: [Informações de Fatura de Associação Anual](https://immersivetranslate.com/bill/)

## Mais perguntas (incomuns)

<details>
<summary>Como limpar meu cache com Tampermonkeys?</summary>
<p>
Devido à limitação da API do Tampermonkeys, o cache do Immersive Translate Tampermonkeys será salvo no cache do site correspondente, então se quiser limpá-lo, pode abrir o painel de ferramentas de desenvolvedor do site correspondente no seu navegador e depois limpar o cache desse site.
</p>
</details>

<details>
<summary>Falha no pedido de endereço de interface personalizada do Tampermonkey?</summary>
<p>
O Tampermonkeys exige que todos os pedidos do script declarem permissões no início do script, por exemplo: `@connect api.google.com`, então se precisar adicionar um novo nome de domínio que não seja o padrão, por favor, declare-o no início do Tampermonkey modelado após o outro nome de domínio.
</p>
</details>

<details>
<summary>O plugin do navegador Edge abre em branco e o navegador relata erro MANIFEST-000001</summary>
<p>
Abra a aplicação [Quick File Finder (Everything)](https://www.voidtools.com/en-us/downloads/), procure pela pasta de armazenamento do navegador `amkbmndfnliijdhojkpoglbnaaahippg` (o ID da extensão Immersive), exclua-a, depois desinstale e reinstale o plugin.
</p>
</details>

<details>
<summary>Como baixar legendas bilíngues / As legendas bilíngues podem ser baixadas de outros sites?</summary>
<p>
- Atualmente, o download de legendas é suportado apenas em desktop.
- Incluindo o YouTube, quando há um botão de download de legendas, o site atual suporta o download de legendas bilíngues.
</p>
</details>