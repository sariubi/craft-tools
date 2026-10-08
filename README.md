# craft-tools

Versioni Linux x86_64 già compilate delle sette **Crafting Apps** open source dell'ArtCraft team, per usarle da Claude in cloud senza ricompilarle (installazione in pochi secondi invece di circa un'ora).

| File | Programma | Alternativa a | Sorgente |
|---|---|---|---|
| bin/pdfcraft-cli.gz | PdfCraft | Acrobat Pro | https://github.com/storytold/pdfcraft |
| bin/photocraft-cli.gz | PhotoCraft | Photoshop | https://github.com/storytold/photocraft |
| bin/designcraft-cli.gz | DesignCraft | InDesign | https://github.com/storytold/designcraft @ 5382fd4 |
| bin/vectorcraft-cli.gz | VectorCraft | Illustrator | https://github.com/storytold/vectorcraft @ f12188a |
| bin/effectcraft-cli.gz | EffectCraft | After Effects | https://github.com/storytold/effectcraft @ 929a9c0 |
| bin/filmcraft-cli.gz | FilmCraft | Premiere Pro | https://github.com/storytold/filmcraft @ 5231852 |
| bin/lightcraft-cli.gz | LightCraft | Lightroom | https://github.com/storytold/lightcraft @ 2472021 |

## Installazione

```sh
git clone -q --depth 1 https://github.com/sariubi/craft-tools ~/craft-tools
mkdir -p ~/bin && for f in ~/craft-tools/bin/*-cli.gz; do n=$(basename $f .gz); gunzip -c $f > ~/bin/$n; chmod +x ~/bin/$n; done
```

La guida d'uso completa per Claude è in `skills/craft-tools/SKILL.md`.

## Licenze

I programmi sono distribuiti con licenza MIT OR Apache-2.0 (vedi i file `LICENSE-*`). Il nome, il marchio e i loghi ArtCraft sono marchi dell'ArtCraft Team e non sono coperti da queste licenze.
