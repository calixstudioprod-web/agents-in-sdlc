---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um workflow do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o workflow e orientar a publicação, mas você continua responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a publicação no GitHub Pages.
- revisar o workflow e o pull request antes de fazer o merge.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma forma simples de experimentá-lo. Publicar o site de um único arquivo com o GitHub Pages disponibiliza o site em uma URL pública sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um workflow do GitHub Actions que compile o site, se necessário, e faça o deploy no GitHub Pages. Adicione um `README` que descreva o aplicativo e como executá-lo localmente, caso ainda não exista. Crie um pull request com essas alterações e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe o deploy até que ele seja concluído com sucesso e, então, informe a URL final do site publicado. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que a tarefa foi concluída até que o site esteja no ar.
```

![Diagrama em três etapas: pull request do space-quiz mesclado; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente para criar e mesclar um pull request e alterar as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de deploy e todas as solicitações de aprovação do GitHub.

## Revise o workflow e verifique a publicação

1. Confirme que o `README` só será adicionado se o repositório ainda não tiver um.
2. Revise as alterações do pull request, incluindo as etapas de build e deploy do workflow.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de deploy do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz é carregado.

Se o agente não puder habilitar o Pages ou fazer o merge do pull request, siga as instruções específicas que ele fornecer. Não considere a tarefa concluída até que o deploy termine com sucesso e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz está disponível como um site publicado, e você verificou o deploy em vez de confiar apenas no relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
