---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você é responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar uma implantação do GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de mesclá-lo.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma maneira simples de experimentá-lo. Publicar o site de arquivo único no GitHub Pages o disponibiliza em uma URL pública sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site, se necessário, e o implante no GitHub Pages. Adicione um README descrevendo o aplicativo e como executá-lo localmente, caso ainda não exista. Crie um pull request com essas alterações e faça a mesclagem depois que as verificações obrigatórias forem aprovadas. Monitore a implantação até que ela seja concluída com êxito e, em seguida, informe a URL final do site ativo. Se você não tiver permissão para habilitar o Pages ou mesclar o pull request, diga exatamente o que preciso aprovar ou fazer; não informe sucesso até que o site esteja no ar.
```

![Diagrama em três etapas: um pull request do space-quiz mesclado; uma execução bem-sucedida do GitHub Actions para implantação do site, com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz no ar em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e mescle um pull request e altere as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de implantação e quaisquer solicitações de aprovação do GitHub.

## Revise o fluxo de trabalho e verifique a implantação

1. Confirme que o README só é adicionado se o repositório ainda não tiver um.
2. Revise as alterações do pull request, incluindo as etapas de compilação e implantação do fluxo de trabalho.
3. Faça a mesclagem somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução da implantação do GitHub Actions até que ela seja concluída com êxito.
5. Abra a URL informada e confirme que o Space Quiz é carregado.

Se o agente não puder habilitar o Pages ou mesclar o pull request, siga as instruções específicas fornecidas por ele. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz agora está disponível como um site ativo, e você verificou a implantação em vez de depender do relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
