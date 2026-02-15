<p align="center">
  <img src="https://i.postimg.cc/cLs9ttp1/Logo-Padrao.png" width="120" alt="logo Notepad Sharp" />
</p>

# Documentação do código do Notepad Sharp


Você encontrou o repositório GitHub de documentação do Notepad Sharp, que contém o conteúdo da [documentação do Notepad Sharp](https://npsharp.girelli.dev.br/docs).

Os tópicos enviados aqui serão publicados no portal [Notepad Sharp](https://npsharp.girelli.dev.br/).

Se você estiver procurando o repositório GitHub do produto NP Sharp, poderá encontrá-lo [aqui](https://github.com/Notepad-Sharp/npsharp).

>**Nota**: O repositório npsharp-docs usa [Git LFS](https://git-lfs.github.com/) (Large File Storage) para armazenar arquivos binários, como imagens e `.gif`s. Se você estiver contribuindo ou atualizando imagens, habilite o Git LFS de acordo com as instruções na seção [Contribuindo](#contribuindo) abaixo.

## Índice

- [Índice](#índice)
- [Código do Notepad Sharp](#código do Notepad Sharp)
- [Feedback](#comentários)
- [Problemas de documentação](#problemas de documentação)
- [Contribuindo](#contribuindo)
  - [Fluxo de trabalho](#fluxo de trabalho)
  - [Clonagem](#clonagem)
    - [Clonagem sem arquivos binários](#clonagem-sem-arquivos-binários)
- [Publicação](#publicação)

## Código do Notepad Sharp

[NP Sharp](https://npsharp.girelli.dev.br/) é um editor de código-fonte leve e um ambiente de desenvolvimento poderoso para criar e depurar aplicativos modernos da Web, móveis e em nuvem. É gratuito e está disponível em sua plataforma favorita – Linux, macOS e Windows.

Se você chegou aqui procurando outras informações sobre o NP Sharp, acesse [nosso site](https://npsharp.girelli.dev.br) para obter informações adicionais.

## Comentários

Se você quiser dar feedback sobre a documentação, use o controle de feedback localizado na parte inferior de cada página da documentação.

## Problemas de documentação

Para inserir bugs de documentação, crie um [novo problema no GitHub](https://github.com/Notepad-Sharp/npsharp-docs/issues). Verifique primeiro se há um problema existente.

Se você acha que o problema está no próprio produto NP Sharp, insira os problemas no repositório do produto NP Sharp [aqui](https://github.comNotepad-Sharp/npsharp/issues).

## Contribuindo

Para contribuir com novos tópicos/informações ou fazer alterações na documentação existente, leia a [Diretriz de Contribuição](./CONTRIBUTING.md#contribuindo).

### Fluxo de trabalho

Os dois fluxos de trabalho sugeridos são:

- Para pequenas alterações, use o botão "Editar" em cada página para editar o arquivo Markdown diretamente no GitHub.
- Se você planeja fazer alterações significativas ou visualizar os arquivos Markdown no NP Sharp, [clone](#clonagem) o repositório para [editar e visualizar](https://npsharp.girelli.dev.br/docs/languages/markdown) os arquivos diretamente no NP Sharp.

![Botão de visualização do Markdown](images/MDPreviewButton.png)

### Clonagem

1. Instale o [Git LFS](https://git-lfs.github.com/).
2. Execute `git lfs install` para configurar ganchos git globais. Você só precisa executar isso uma vez por máquina.
3. Autenticação SSH: `git clone git@github.com:microsoft/npsharp-docs.git`<br>Autenticação HTTPS: `git clone https://github.com/Notepad-Sharp/npsharp-docs.git`
4. Agora você pode `git add` arquivos binários e confirmá-los. Eles serão rastreados no LFS.

#### Clonagem sem arquivos binários

Você pode querer clonar o repositório sem as imagens de 1,6 GB. Aqui estão as etapas:

1. Instale o [Git LFS](https://git-lfs.github.com/).
2. Execute `git lfs install` para configurar ganchos git globais. Você só precisa executar isso uma vez por máquina.
3. Clone o repositório sem arquivos binários.
    - macOS/Linux:
      - Autenticação SSH: `GIT_LFS_SKIP_SMUDGE=1 git clone git@github.com:Notepad-Sharp/npsharp-docs.git`
      - Autenticação HTTPS: `GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/Notepad-Sharp/npsharp-docs.git`
    - Janelas:
      - Autenticação SSH: `$env:GIT_LFS_SKIP_SMUDGE="1"; git clone git@github.com:Notepad-Sharp/npsharp-docs.git`
      - Autenticação HTTPS: `$env:GIT_LFS_SKIP_SMUDGE="1"; clone do git https://github.com/Notepad-Sharp/npsharp-docs.git`
4. Agora você pode verificar seletivamente alguns arquivos binários para trabalhar. Por exemplo:
    - `git lfs pull -I "docs/nodejs"` para baixar apenas imagens em `docs/nodejs`
    - `git lfs pull -I "release-notes/images/1_4*/*"` para baixar apenas imagens em `release-notes/images/1_4*`
    - `git lfs pull -I "docs,api"` para baixar todas as imagens em `docs` e em `api`
    - `git lfs pull -I <PATTERN>`, desde que `<PATTERN>` seja um [padrão de inclusão e exclusão do Git LFS válido](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-fetch.adoc#include-and-exclude).

A história deste repositório antes de adotarmos o LFS pode ser encontrada em [microsoft/npsharp-docs-archive](https://github.com/microso
ft/npsharp-docs-archive).

## Publicação

A publicação de solicitações pull mescladas não é automática e é iniciada manualmente após a revisão das alterações em um servidor de armazenamento temporário interno. Não há garantia de tempo específico para quando as atualizações de RP estarão disponíveis em https://npsharp.girelli.dev.br, mas a intenção é que elas geralmente estejam no ar dentro de 24 horas.
