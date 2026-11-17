# SITTAX REC — Releases

Repositório público só com os instaladores do app desktop **SITTAX REC** (sem código-fonte).
O código fica em `Sittax/Sittax.Rec.App` (privado) e a landing de download em `Sittax/Sittax.Rec`.

Os instaladores ficam anexados em cada [release](https://github.com/Sittax/Sittax.Rec.Releases/releases)
(tag `vX.Y.Z`). Links diretos usados pela landing e pelo aviso de atualização do app:

```
https://github.com/Sittax/Sittax.Rec.Releases/releases/download/vX.Y.Z/SittaxRec-Windows-X.Y.Z-Setup.exe
https://github.com/Sittax/Sittax.Rec.Releases/releases/download/vX.Y.Z/SittaxRec-Linux-X.Y.Z.AppImage
https://github.com/Sittax/Sittax.Rec.Releases/releases/download/vX.Y.Z/SittaxRec-Mac-X.Y.Z-Installer.dmg
```

## Publicar uma versão nova
1. Gerar os instaladores no `Sittax.Rec.App` (`npm run build`, Linux via Docker, `.dmg` num Mac).
2. Criar a release `vX.Y.Z` aqui e anexar os arquivos com os nomes acima.
3. Atualizar `constants.ts` da landing e o fluxo n8n "Sittax REC - Verificar versão do app".
