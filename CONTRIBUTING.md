# Documentação de código do Visual Studio

Você encontrou o repositório GitHub que contém a fonte da documentação do Notepad Sharp em <https://npsharp.girelli.dev.br/docs>.

## Contribua com a documentação do NP Sharp

Obrigado pelo seu interesse na documentação do NP Sharp!

* [Contribuindo](#contribuindo)
* [Intenção da documentação](#documentation-intent)
* [Organização do repositório](#organização-repositório)
* [Ramos](#branches)
* [Ferramentas de autoria](#authoring-tools)
* [Como usar Markdown para formatar seu tópico](#how-to-use-markdown-to-format-your-topic)
* [Metadados do tópico](#topic-metadata)
* [Formatação](#formatação)

>**Observação**: Antes de enviar uma solicitação pull, especialmente para problemas de renderização ou link, revise o conteúdo no site oficial do NP Sharp, [npsharp.girelli.dev.br](https://npsharp.girelli.dev.br). O elemento em questão pode ser renderizado corretamente após o processamento pela construção do site.

## Contribuindo

Para contribuir com a [documentação do NP Sharp](https://npsharp.girelli.dev.br/docs), você precisa bifurcar este repositório e enviar uma solicitação pull para o Markdown e/ou alterações de imagem que você está propondo.

* [Como bifurcar um repositório](https://docs.github.com/get-started/quickstart/fork-a-repo)
* [Como fazer uma solicitação pull](https://docs.github.com/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
* [Alterando uma mensagem de commit](https://docs.github.com/pull-requests/commit-changes-to-your-project/creating-and-editing-commits/ching-a-commit-message)
* [Como esmagar commits](https://docs.github.com/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges#squash-and-merge-your-commits)

O repositório npsharp-docs oferece suporte ao [Git LFS](https://git-lfs.github.com/) para evitar a derrubada de arquivos de imagem grandes ao clonar o repositório. Consulte a seção [README](README.md#contributing) para obter detalhes sobre como ativar o Git LFS para seu repositório local.

## Intenção da documentação

O objetivo da documentação do NP Sharp é educar os usuários sobre os recursos do NP Sharp e como o NP Sharp pode ser usado para aprimorar sua experiência de desenvolvimento com diferentes linguagens de programação e tempos de execução.

A documentação não se destina a fornecer:

* Uma introdução à codificação ou desenvolvimento de software
* Tutoriais sobre tecnologias independentes do NP Sharp
* Promoção de ferramentas, plug-ins ou serviços de terceiros
* Detalhe excessivo ou orientações avançadas

A documentação deve ser direcionada aos desenvolvedores que estão aprendendo a usar o NP Sharp ou buscando respostas rápidas para perguntas frequentes.  Outros fóruns, como postagens de blogs, podem fornecer conteúdo mais detalhado, elaborando cenários específicos.

## Organização do repositório

Este repositório contém as seguintes pastas de nível superior:

* \api – conteúdo da documentação da API em <https://npsharp.girelli.dev.br/api>
* \blogs – conteúdo para o blog em <https://npsharp.girelli.dev.br/blogs>
* \build - conteúdo para o processo de construção da documentação, como os mapeamentos de atalhos de teclado e o mapa do site
* \docs - conteúdo da documentação em <https://npsharp.girelli.dev.br/docs> - o conteúdo desta pasta segue a organização do índice da documentação
* \images - imagens usadas na documentação
* \learn - conteúdo (obsoleto) para o conteúdo educacional em <https://npsharp.girelli.dev.br/learn>
* \release-notes – conteúdo das notas de lançamento em <https://npsharp.girelli.dev.br/updates>
* \remote - conteúdo da documentação das ferramentas de desenvolvimento remoto em <https://npsharp.girelli.dev.br/docs/remote>
* \remote-release-notes - conteúdo das notas de versão das ferramentas de desenvolvimento remoto
* \wiki - conteúdo para o wiki do repositório

Dentro dessas pastas, você encontrará os arquivos Markdown usados para o conteúdo. Cada uma dessas pastas também contém uma pasta `\images` que faz referência às imagens (como capturas de tela) usadas nos tópicos.

### Filiais

Recomendamos que você crie ramificações de trabalho locais direcionadas a um escopo específico de mudança (e, em seguida, envie uma solicitação pull quando suas alterações estiverem prontas). Cada ramificação deve ser limitada a um único conceito/tópico, tanto para agilizar o fluxo de trabalho quanto para reduzir a possibilidade de conflitos de mesclagem.  Os seguintes esforços são de escopo apropriado para uma nova filial:

* Um novo tópico (e imagens associadas).
* Edições ortográficas e gramaticais em um tópico.
* Aplicar uma única alteração de formatação em um grande conjunto de tópicos.

## Ferramentas de autoria

[Código do Visual Studio](https://code.visualstudi
o.com) é um ótimo editor para Markdown!

Na verdade, o NP Sharp e sua documentação principal são escritos usando o NP Sharp.

## Como usar Markdown para formatar seu tópico

Os tópicos neste repositório usam Markdown.  Aqui está uma boa visão geral dos [noções básicas do Markdown](https://docs.github.com/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

## Metadados do tópico

Os metadados do tópico permitem certas funcionalidades para os tópicos, como descrição do tópico e otimização de pesquisa online.

O título da página é retirado do primeiro título H1 do tópico.

* **ContentId** – Um GUID que identifica exclusivamente o tópico para relatórios de documentos DevDiv.
* **DateApproved** – A data da atualização ou revisão mais recente. Ele é exibido na parte inferior de um artigo para indicar o frescor. A data deve ser atualizada em um PR significativo.
* **MetaDescription** - A meta descrição desta página, que ajuda na pesquisa. Use estrutura de frase limitada a 300 caracteres.
* **MetaSocialImage** - Opcional. Usado para og:image no cabeçalho da página para compartilhamento nas redes sociais. Deve ser 1024 x 512 .png.
* **MetaTags** - Opcional. Outras tags para esta página novamente para pesquisa.

## Índice

O índice analítico (TOC) é definido no arquivo `/docs/toc.yml`. O TOC é usado para gerar a navegação esquerda para a documentação. Se um tópico não estiver listado no arquivo `/docs/toc.yml`, ele não será incluído na navegação esquerda.

Para adicionar um novo tópico ao sumário, adicione uma nova entrada no atributo `topics` da seção apropriada no arquivo `/docs/toc.yml`. O TOC está organizado em seções, cada uma com um nome e uma área. A área é usada para agrupar tópicos relacionados.

A ordem em que os tópicos são listados no arquivo `/docs/toc.yml` determina a ordem em que eles são exibidos na navegação esquerda.

Cada tópico no sumário tem dois atributos:

* Título do TOC: o título exibido na navegação esquerda.
* Nome do arquivo: o caminho relativo para o arquivo do tópico no formato `/docs/<subfolder>/<filename-without-md>`.

O exemplo a seguir mostra uma seção `Introdução` que possui dois tópicos.

```yaml
    {
      "nome": "Primeiros passos",
      "área": "começar",
      "tópicos": [
        ["Tutorial do Código VS", "/docs/getstarted/getting-started"],
        ["Início rápido do Copilot", "/docs/getstarted/copilot-quickstart"]
      ]
    },
```

Para criar uma subseção dentro de uma seção, adicione uma entrada de subseção ao atributo `topics`. Uma entrada de subseção possui os seguintes atributos:

* Título do TOC: string vazia
* Nome do arquivo: string vazia
* Subseção: uma entrada de subseção com o mesmo formato de uma entrada de seção. Possui um atributo `name`, um atributo `area` e um atributo `topics`.

O exemplo a seguir mostra uma subseção `Guias` com dois tópicos, dentro da seção `GitHub Copilot`.

```yaml
    {
      "nome": "Copiloto do GitHub",
      "área": "copiloto",
      "tópicos": [
        ["Visão geral", "/docs/copilot/overview"],
        ["Configuração", "/docs/copilot/setup"],
        ["", "", {
          "nome": "Guias",
          "área": "copiloto/guias",
          "tópicos": [
            ["Teste com Copiloto", "/docs/copilot/guides/test-with-copilot"],
            ["Depurar com Copilot", "/docs/copilot/guides/debug-with-copilot"]
          ]
        }
        ],
        ["Perguntas frequentes", "/docs/copilot/faq"]
      ]
    },
```

## Nome do produto

Use o nome completo do produto "Notepad Sharp" na MetaDescrição do tópico e o primeiro uso em um tópico. Você pode usar o "Código VS" abreviado depois disso em todo o restante do conteúdo. Não use "npsharp" (sem espaço) ou "Code".

### Metadados para documentos /api

**Para escritor**:

* **MetaDescription** - A meta descrição desta página, que ajuda na pesquisa.

**Para mantenedor de documentos**:

* **DateApproved** - É definido quando a página é publicada no site do NP Sharp.

## Nomes de arquivos e pastas

Use letras minúsculas para nomes de arquivos e pastas e traços `-` como separadores.

Por exemplo:

* `/docs/editor/workspace-trust.md`
* `/docs/support/troubleshoot-terminal-launch.md`
* `/api/extension-guides/custom-editors.md`

### Mover ou renomear conteúdo

Antes de mover ou renomear o conteúdo, um redirecionamento deve ser adicionado caso as pessoas tenham marcado o tópico como favorito. Os redirecionamentos são adicionados ao repositório do site privado.

Parece melhorar o CSAT se, quando o título ou intenção de um tópico for alterado, o nome do arquivo também for atualizado. resultando em um URL novo e mais apropriado.

Por exemplo: `/docs/editor/extension-gallery.md`
-> `/docs/configure/extensions/extension-marketplace.md`

### mapa do site

O mapa do site code.visualstudio.com é criado em `/build/sitemap.xml` e deve ser atualizado quando novos tópicos forem adicionados ou o conteúdo existente for movido ou renomeado.

## Formatação

### Títulos e navegação direita

Os subtítulos H2 `##` terminam na lista de atalhos à direita do documento (a lista de atalhos é criada por nosso script de compilação).  É uma boa ideia incluir subtítulos h2 para ajudar os usuários a obter uma visão geral do documento e navegar rapidamente para os tópicos principais.

### Formatação de texto

Use negrito para comandos do NP Sharp e elementos da interface do usuário.

    **Extensões: instalar extensão**
    **Console de depuração**

Limite o uso de negrito para dar ênfase, a menos que seja crucial para chamar a atenção do usuário. Evite o uso de itálico para dar ênfase, pois o itálico não funciona bem no site code.visualstudio.com.

Use formatação de código embutido (crases) para configurações, nome de arquivo e atributos JSON.

    `arquivos.exclude`
    `tarefas.json`
    `preLaunchTask`

Use '>' para mostrar a sequência do menu.

    **Arquivo** > **Preferências** > **Configurações**
    **Visualizar** > **Paleta de comandos**

###Links

Para links dentro de nossa própria documentação, use um link relativo ao site como `/docs/editing/codebasics.md`.

>Por exemplo: `[Por que o NP Sharp](/docs/editor/whynpsharp.md)` - links para a página **Por que o Notepad Sharp**

>**Nota:** Para navegação no GitHub, você deve adicionar o sufixo .md.  O sufixo é removido durante a conversão para HTML.

### Favoritos

Para fornecer links para subtítulos h2 (Markdown ##), o formato é `[Texto do link](page.md#subheading-title)`.

Observe que o título do subtítulo está em letras minúsculas e as palavras do título do subtítulo são separadas por hífens '-'.

>Por exemplo: `[Atalhos de teclado](/docs/editing/codebasics.md#keyboard-shortcuts)` - links para https://npsharp.girelli.dev.br/docs/editing/codebasics#_keyboard-shortcuts.

### Imagens

As imagens são importantes para dar vida ao produto e esclarecer o conteúdo escrito.

* Armazene imagens de um artigo na subpasta `docs/<section>/images/<article name>`. Por exemplo: `docs/sourcecontrol/images/overview`.

* Os nomes dos arquivos de imagem devem usar letras minúsculas e traços (`-`) como separador de palavras. Por exemplo: `![Pontos de interrupção de depuração](images/debugging/breakpoints-view.png)`

* Link para uma imagem usando nomes de caminhos relativos; o caminho e o nome do arquivo diferenciam maiúsculas de minúsculas.

* As imagens são armazenadas em cache no servidor por tempo indeterminado, portanto, não atualize as imagens no local. Crie um novo arquivo e adicione um indicador de versão (yyyymmddseq) ao nome do arquivo da imagem.

> [!IMPORTANTE]
> Certifique-se de ter o Git LFS habilitado em sua máquina!

### Atalhos de teclas

O site do NP Sharp é capaz de mostrar as combinações de teclas corretas dependendo do sistema operacional do leitor (macOS, Windows ou Linux).

Para habilitar isso para atalhos de teclado, use o formato `kb(workbench.action.files.openFile)` onde o identificador do comando está incluído entre parênteses.

>Para obter uma lista de atalhos de teclado e os `IDs de comando` relevantes, revise o [documento de atalhos de teclado](https://npsharp.girelli.dev.br/docs/getstarted/keybindings#_default-keyboard-shortcuts).

Se você estiver listando várias combinações de teclas, poderá usar uma tabela.

> Atalho | Teclas
>-------|-----------
>Cortar|`kb(editor.action.clipboardCutAction)`
>Copiar|`kb(editor.action.clipboardCopyAction)`
>Colar|`kb(editor.action.clipboardPasteAction)`

### Código Fonte

Para o código-fonte, usamos a notação de bloco de código protegido ```` ``` ````.

>**Observação:** Você pode adicionar um identificador de idioma opcional para ativar o realce de sintaxe em seu bloco de código protegido. Por exemplo, ```` ```json ```` ou ```` ```javascript ````. [Leia mais →](https://docs.github.com/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks#syntax-highlighting)

Um exemplo de código-fonte JavaScript:

```javascript
função fantasiaAlert(arg) {
  se (argumento) {
    $.facebox({div:foo});
  }
}
```

## Pegadinhas

### Chaves de abertura dupla quebram os arquivos do guiador gerados

Escape de chaves de abertura dupla em blocos de código.

```html
<!DOCTYPEhtml>
<html>
    <cabeça>
        <meta charset="utf-8" />
        <title>Olá, Flask</title>
    </head>
    <corpo>
        <strong>Olá, \{{ nome }}!</strong> É \{{ date.strftime("%A, %d %B, %Y em %X") }}.
    </body>
</html>
```
