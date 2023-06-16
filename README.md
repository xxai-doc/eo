<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Parto de la retejo-kodo estas malferma fonto, bonvena helpi optimumigi la tradukon.

## antaŭa kodo

* [antaŭa kodo](https://github.com/xxai-art/web)
* [Lingvaj pakoj por la retejo kiel tutaĵo](https://github.com/xxai-art/web/tree/main/i18n)
* [Lingvaj pakoj por ensalutmoduloj](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Retejo Plurlingva Dokumentado](https://github.com/xxai-doc)

La antaŭfina programlingvo estas [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , kiu aldonas kelkajn funkciojn bazitajn sur la coffeescript sintakso, vidu [./coffee_plus.md](./coffee_plus.md) .

## Internaciigo de retejoj kaj dokumentoj

Konstruu sur la sekvaj 3 projektoj

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  La sufikso estas `.mdt` , vi povas uzi la sintakson similan al `<+ ./coffee_plus/import.js>` por rilati al eksteraj dosieroj, kaj generi markdown per la sufikso `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Markdown-traduko ne tradukos kodojn kaj ligilojn, kaj konservos tradukitajn frazojn. Se la traduko estas modifita sed la originala teksto ne estas modifita, ekzekuti ĝin denove ne anstataŭigos la modifon de la traduko.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Lingvaj dosieroj por traduki `yaml` generitajn retejojn.
