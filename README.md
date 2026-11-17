# SITTAX REC — Releases

Repositório público só com os instaladores do app desktop **SITTAX REC** (sem código-fonte).
O código fica em `Sittax/Sittax.Rec.App` (privado) e a landing de download em `Sittax/Sittax.Rec`.

Os instaladores ficam anexados em cada [release](https://github.com/Sittax/Sittax.Rec.Releases/releases)
(tag `vX.Y.Z`). Links diretos usados pela landing:

```
https://github.com/Sittax/Sittax.Rec.Releases/releases/download/vX.Y.Z/SittaxRec-Windows-X.Y.Z-Setup.exe
https://github.com/Sittax/Sittax.Rec.Releases/releases/download/vX.Y.Z/SittaxRec-Linux-X.Y.Z.AppImage
https://github.com/Sittax/Sittax.Rec.Releases/releases/download/vX.Y.Z/SittaxRec-Mac-X.Y.Z-Installer.dmg
```

## Aviso de atualização do app
O app até a 1.4.2 inclusive (instalada antes de 17/11/2026) baixa a atualização **sem seguir redirecionamento**, e o GitHub
responde 302 → o app salvaria um arquivo de 0 bytes. Por isso o fluxo n8n de versão aponta para o fluxo de download do n8n
(`https://n8n.sittax.com.br/webhook/gdswk9q379vUtiyv/download/vX.Y.Z/SittaxRec.{exe,AppImage}`), que busca o arquivo
aqui no GitHub e devolve direto. A partir do build de 17/11/2026 o app segue redirect.

## Publicar uma versão nova
1. Gerar os instaladores no `Sittax.Rec.App` (`npm run build`, Linux via Docker, `.dmg` num Mac).
2. Criar a release `vX.Y.Z` aqui e anexar os arquivos com os nomes acima.
3. Atualizar `constants.ts` da landing, criar os webhooks da versão no fluxo n8n de download (nó "GitHub - Download")
   e apontar o fluxo n8n "Sittax REC - Verificar versão do app" para eles.
