---
title: "Git: Controle de Versão"
author: "Gean MArtins"
date: 2024-05-05 18:30:00 -0300
categories: [Git]
tags: [git]
image: /assets/img/controle-de-versao.webp
abstract: "Este documento oferece uma visão abrangente sobre como utilizar o Git, um sistema de controle de versão distribuído, para gerenciar projetos de software. Abrange desde a instalação até o uso avançado de branches e merges."
---

# Sumário
1. [Introdução ao Controle de Versão](#introdução-ao-controle-de-versão)
2. [O que é Git?](#o-que-é-git)
3. [Os Três Estados do Git](#os-três-estados-do-git)
4. [Configuração e Uso do Git](#configuração-e-uso-do-git)
5. [Trabalhando com Branches](#trabalhando-com-branches)
6. [Links e Recursos Adicionais](#links-e-recursos-adicionais)


## Introdução ao Controle de Versão
O controle de versão é essencial para registrar alterações em arquivos ao longo do tempo, permitindo recuperar versões específicas mais tarde. Este guia foca no Git, mas menciona outros sistemas como CVS, Mercurial, e Subversion para contextualização.

## O que é Git?
Git é um sistema de controle de versão distribuído, ideal para coordenação com múltiplas pessoas editando os mesmos arquivos simultaneamente. Desenvolvido originalmente por Linus Torvalds, é uma ferramenta fundamental para o desenvolvimento moderno de software.

### Como o Git Funciona?
O Git trata dados como grupos de snapshots de um sistema de arquivos. A cada commit, o Git captura uma imagem do estado atual dos arquivos, o que difere de VCSs que registram apenas as diferenças entre os arquivos.

## Os Três Estados do Git
Entender os três estados dos arquivos no Git é crucial:

- **Modificado (Modified)**: Arquivos que foram alterados mas não marcados para commit.
- **Preparado (Staged)**: Arquivos marcados para o próximo commit.
- **Consolidado (Committed)**: Dados seguramente armazenados em seu diretório local do Git.

### Diagrama dos Estados do Git
![Diagrama simplificado dos estados do Git](https://linkparaumdiagrama.com/git-states.png)

## Configuração e Uso do Git

### Instalação do Git
Para instalar o Git, use o gerenciador de pacotes conforme seu sistema operacional:

```bash
sudo apt update && sudo apt install git  # Debian, Ubuntu
```

### Configuração Inicial do Git
Configurar seu usuário e email no Git:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu_email@example.com"
```

### Gerenciamento de Arquivos com .gitignore
Para evitar o versionamento de arquivos desnecessários como logs, compilações ou arquivos temporários, utilize o `.gitignore`:

```plaintext
# Excluir todos os arquivos temporários
*.tmp

# Excluir diretório de logs
logs/
```

## Trabalhando com Branches

### Criando e Alternando Branches
Branches permitem que você desenvolva funcionalidades isoladamente sem afetar o branch principal (master/main).

```bash
git branch nova-feature
git checkout nova-feature
```

### Merge de Branches
Integrar mudanças de um branch de feature de volta ao branch principal:

```bash
git checkout master
git merge nova-feature
```

## Links e Recursos Adicionais
- [Documentação Oficial do Git](https://git-scm.com/doc)
- [Tutorial Interativo de Git](https://learngitbranching.js.org/)