---
sidebar_position: 4
---

# Ajuda com PDF

O Leitor Bilíngue de Tradução Imersiva de PDF é uma ferramenta de tradução em tempo real cruzada e bilíngue adequada para uso como auxílio à leitura.

Atualmente, caracteres especiais como fórmulas matemáticas, tabelas, etc., não podem ser tratados corretamente devido à técnica de reconhecimento de texto simples.

Se o seu PDF contém tabelas e fórmulas matemáticas, e há requisitos de tradução de maior qualidade para eles e você possui algumas habilidades de programação, é recomendado consultar este artigo [Nouga-OCR + Tradução Imersiva](https://app.immersivetranslate.com/pdf-pro/)

Veja [a documentação aqui](/docs/usage/#pdf-file-translation) para perguntas básicas de uso

Aqui estão algumas dicas avançadas de tradução de PDF:

<!--
## Mover para ajustar a caixa de tradução

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-move.png) -->

### Editar Caixa

A tradução padrão é editável. Você pode até clicar em "Mostrar texto original" no painel, e o conteúdo da caixa de texto será exibido como o texto original reconhecido inteligentemente, e você pode fazer correções ao texto original na caixa de edição neste momento. Então, re-clique na tradução do painel

### Mover Caixas de Texto

Quando alguns parágrafos são reconhecidos em uma posição incorreta, você pode escolher mover a posição de toda a caixa de edição do parágrafo, colocando o mouse no canto superior esquerdo. (Se você encontrar uma situação em que não pode arrastar, você pode ampliar e arrastar para baixo o canto inferior direito, e o canto superior esquerdo se moverá normalmente)

### Excluir caixa de texto

Quando alguns parágrafos podem ter problemas de reconhecimento, manualmente fundir o parágrafo anterior, este parágrafo pode ser redundante, desta vez você pode clicar neste botão para excluí-lo!### Ajustando o tamanho da caixa de texto

Porque a altura e largura padrão da tradução são as mesmas do parágrafo original por padrão, quando o conteúdo da tradução excede o texto original, haverá um transbordamento, nesse caso, você pode visualizá-lo através da rolagem interna. Você também pode arrastar e soltar no canto inferior direito para aumentar essa caixa de texto apropriadamente, permitindo que o conteúdo seja totalmente exibido.

<!-- ## Botões de Estilo de Controle

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-control.png) -->

### Modo Bandwagon

O padrão é restaurar a imagem do texto original para a área traduzida à direita. É normal ver uma moldura de fundo branco para o texto traduzido, porque é necessário cobrir o texto original desenhado pelo canvas para que o texto traduzido possa ser exibido corretamente.

Se você achar que o modo de subcamada afeta sua leitura, basta desativá-lo.

### Limite de Sobreposição

Porque usamos o máximo possível para restaurar o efeito tipográfico original, então a posição de início do parágrafo é a do canto superior esquerdo do parágrafo original que prevalece. Sob circunstâncias normais da tradução de inglês para chinês, o conteúdo em chinês geralmente será menor que o inglês, dessa vez a tradução pode ser totalmente demonstrada. Isso ocorre quando o texto traduzido é redundante com o texto original em alguns casos. Para evitar isso, demos à tradução uma altura igual à do parágrafo original.

Isso pode ser desativado quando sentimos que a distância entre os parágrafos superior e inferior é suficiente para a apresentação da parte traduzida que excede

### Espaçamento Apertado

Este objetivo é na verdade semelhante ao acima, porque há um certo espaçamento entre cada linha de texto para garantir a legibilidade do texto traduzido.

Se a tela for pequena e o espaçamento entre os parágrafos superior e inferior pode não ser suficiente para mostrar o transbordamento do texto traduzido, você pode ativar este item e remover o espaçamento entre as linhas de texto, para que o texto dos parágrafos possa ser totalmente exibido### Indentação do cabeçalho do parágrafo

Devido à complexidade dos diversos layouts de PDF, não é possível identificar inteligentemente se um parágrafo está em conformidade com as características de indentação, mas se não houver indentação, então você pode achar que olhar para o parágrafo do artigo é um pouco complicado. Assim, para este tipo de parágrafo no artigo, o usuário pode ativá-lo e o primeiro parágrafo de cada parágrafo será indentado para mostrar

### Linhas são amplamente espaçadas e parágrafos não são reconhecidos

Alguns PDFs podem, por motivos de exibição, ter um espaçamento entre parágrafos relativamente grande, resultando em que, durante a identificação inteligente, essa sentença seja julgada como um parágrafo independente. Portanto, precisa ser ajustado apropriadamente, por exemplo, para 10, de modo que 10px seja usado como o espaçamento entre linhas para reconhecer novamente os parágrafos na página.

### Ajustando a posição horizontal das traduções

Como as coordenadas horizontais do texto traduzido são lidas a partir dos dados originais do PDF, algumas das coordenadas horizontais do PDF serão grandes. Neste caso, você pode fazer o conteúdo traduzido mover-se para a esquerda arrastando a barra de progresso.

### Ajustando a escala das traduções

O tamanho do texto traduzido é basicamente o mesmo que o texto original, quando você sentir que o tamanho do texto traduzido não é apropriado, você pode arrastar a barra de progresso para permitir que o tamanho da fonte seja ajustado de acordo com a proporção

## Ajuste manual de segmentos com erro

Se o parágrafo reconhecido inteligentemente estiver incorreto, ele pode ser ajustado manualmente seguindo os passos abaixo

- Clique no painel de tradução para exibir o texto original reconhecido
- Em seguida, ajuste manualmente o parágrafo em relação ao texto original à esquerda, copiando e fazendo quebras de linha, etc.
- Quando o parágrafo for confirmado como correto, clique em Traduzir novamente

<!-- ## Baixar Impressão

Clique no ícone de download no canto superior direito

![](https://s.immersivetranslate.com/static/official-static/assets/docs/doc-assets/pdf-download.png) -->

Como nossa ferramenta depende do navegador, a velocidade de download e os resultados dependem muito do próprio navegador. Portanto, é recomendado não lidar com mais de 300 páginas de PDF

### Download da Tradução (Impressão)

Esta funcionalidade baixa apenas as traduções, não o bilingue.
Quando a tradução padrão é exibida, o modo de zoom é ajustado para a largura da página para efeito de leitura.

No entanto, quando houver a necessidade de imprimir e economizar tempo, é recomendado ajustar o modo de zoom, geralmente é recomendado ajustar para 100 por cento ou o tamanho real, o efeito de impressão será melhor.

### Preservação Bilíngue

Devido a limitações técnicas nos efeitos de preservação bilíngue, as traduções são preservadas na forma de imagens, possibilitando a preservação WYSIWYG dos efeitos de tradução online. Leva cerca de 5/6 minutos para exportar 300 páginas de PDF.

## Outras situações

### Intraduzível

- Verifique se o texto original à esquerda pode ser copiado, se não puder ser copiado, prova ser um PDF em imagem, o suporte temporário atual para a tradução de PDF em imagem
- Verifique se a tradução é reconhecida mas não traduzida, que 🔄❓ não aparece no final do parágrafo, e que o botão no painel do plug-in mostra "Traduzir". Neste ponto, clique no botão de traduzir para acionar a tradução.
- Se 🔄❓ existir, clique em ❓ para ver a mensagem de erro

### Documento de Feedback por Email

Você pode enviar uma descrição do seu problema + uma captura de tela com o PDF original para support@immersivetranslate.com\. Nós verificaremos a situação do PDF e organizaremos para que o plano seja inserido nas regras de reconhecimento inteligente.
