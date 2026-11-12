# CTUBE — releases públicas

Este repositório **não tem código-fonte**. Ele existe só para hospedar os
instaladores do CTUBE, porque o repositório do código é privado: releases em
repositório privado obrigam todo mundo a fazer login no GitHub para baixar e
impedem a atualização automática do app.

## Baixar

Última versão: **[Releases](../../releases/latest)**

| Plataforma | Arquivo |
| --- | --- |
| Windows (desktop) | `CTUBE-Setup.exe` |
| Android | `CTUBE.apk` |
| iOS | `CTUBE-iOS.zip` / `CTUBE.ipa` |

O site/app também fica em https://distribuicao-multiplataforma.vercel.app

## Como é alimentado

Cada tag `v*` no repositório privado dispara as Actions **CTUBE Windows**,
**CTUBE Android** e **CTUBE iOS**, que anexam os instaladores na release da
mesma tag **aqui** (secret `RELEASES_TOKEN`). A rota `/api/update` do app lê a
release mais recente deste repositório e mostra o alerta de nova versão.

Não edite releases manualmente: elas são geradas pelo build.
