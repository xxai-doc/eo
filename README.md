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

### Instrukcioj pri Aŭtomatiga Tradukado de Dokumentoj

Vidu deponejon [xxai-art/doc](https://github.com/xxai-art/doc)

Oni rekomendas instali nodejs, [direnv](https://direnv.net) kaj [bun](https://github.com/oven-sh/bun) unue, kaj poste ruli `direnv allow` post eniro de la dosierujo.

Por eviti tro grandajn magazenojn tradukitajn al centoj da lingvoj, mi kreis apartan kodstokejon por ĉiu lingvo kaj kreis organizon por konservi ĉi tiun magazenon.

Agordi la mediovariablon `GITHUB_ACCESS_TOKEN` kaj poste ruli [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) aŭtomate kreos la magazenon.

Kompreneble, vi ankaŭ povas meti ĝin en magazenon.

Traduka skripto-referenco [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

La skriptokodo estas interpretita jene:

[bunx](https://bun.sh/docs/cli/bunx) estas anstataŭaĵo por npx, kiu estas pli rapida. Kompreneble, se vi ne havas bulkon instalitan, vi povas uzi `npx` anstataŭe.

`bunx mdt zh` bildigas `.mdt` en la dosierujo zh kiel `.md` , vidu la 2 ligitajn dosierojn sube

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` estas la kerna kodo por tradukado (se vi nur havas `nodejs` instalitaj, sed `bun` kaj `direnv` ne estas instalitaj, vi ankaŭ povas ruli `npx i18n` por traduki).

Ĝi analizos [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , la agordo de `i18n.yml` en ĉi tiu dokumento estas jena:

```
en:
zh: ja ko en
```

La signifo estas: ĉina traduko al japana, korea, angla, angla traduko al ĉiuj aliaj lingvoj. Se vi volas nur subteni la ĉinan kaj la anglan, vi povas simple skribi `zh: en` .

La lasta estas [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , kiu ĉerpas la enhavon inter la ĉefa titolo kaj la unua subtitolo de ĉiu lingvo `README.md` por generi enskribon `README.md` . La kodo estas tre simpla, vi povas rigardi ĝin mem.

Google API estas uzata por senpaga tradukado. Se vi ne povas aliri Guglon, bonvolu agordi kaj agordi prokurilon, kiel:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

La traduka skripto generos tradukan kaŝmemoron en dosierujo `.i18n` , bonvolu kontroli ĝin per `git status` kaj aldonu ĝin al la koda deponejo por eviti ripetajn tradukojn.
