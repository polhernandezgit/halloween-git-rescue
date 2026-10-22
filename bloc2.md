
# Bloc 2: Les Branques del Més Enllà i Resolució del Conflicte

## Acció 3.6: Crear les branques

S'han creat dues branques a partir de `main` per treballar en paral·lel. Aquesta topologia permet que totes dues parteixin del mateix codi base i que les modificacions siguin independents.

```bash
git branch feature-nightmare
git branch feature-sanctuary
git branch
```

![alt text](<captures/Captura de pantalla 2026-10-22 191106.png>)

## Acció 3.7: Modificar la branca nightmare

S'ha canviat l'estat de seguretat a `NIGHTMARE DETECTED` i s'ha registrat el canvi.

```bash
git switch feature-nightmare
git add main.js
git commit -m "feat: inject nightmare security state"
```

![alt text](<captures/Captura de pantalla 2026-10-22 191113.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191120.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191129.png>)

## Acció 3.8: Modificar la branca sanctuary

S'ha canviat la mateixa línia per establir l'estat `SANCTUARY ACTIVE` i s'ha creat un commit independent.

```bash
git switch feature-sanctuary
git add main.js
git commit -m "feat: activate sanctuary security protocol"
```

![alt text](<captures/Captura de pantalla 2026-10-22 191137.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191143.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191154.png>)

## Acció 3.9: Integrar les branques

S'ha integrat primer la branca nightmare i després s'ha intentat integrar sanctuary.

```bash
git switch main
git merge --no-ff feature-nightmare -m "merge: integrate nightmare timeline"
git merge --no-ff feature-sanctuary
```

La segona integració ha provocat un conflicte perquè les dues branques han modificat la mateixa línia.

![alt text](<captures/Captura de pantalla 2026-10-22 191205.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191211.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191219.png>)

## Acció 3.10: Resoldre el conflicte

S'han eliminat manualment les marques de conflicte i s'ha establert l'estat definitiu `SANCTUARY ACTIVE - NIGHTMARE CONTAINED`.

```bash
git add main.js
git status
git commit -m "merge: resolve security timeline conflict"
git log --oneline --graph --all
```

![alt text](<captures/Captura de pantalla 2026-10-22 191225.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191235.png>)

![alt text](<captures/Captura de pantalla 2026-10-22 191243.png>)
