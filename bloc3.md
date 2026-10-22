
# Bloc 3: Viatge Temporal, Exorcisme del Codi i Publicació Remota

## Acció 3.11: Crear el commit infectat

S'ha afegit una excepció al fitxer principal per simular una fallada del sistema i s'ha registrat el canvi.

```bash
git switch main
git add main.js
git commit -m "feat: unhandled spectral exception"
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191250.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191257.png>)

## Acció 3.12: Inspeccionar les diferències

S'ha comparat el commit infectat amb el commit anterior per identificar la modificació defectuosa.

```bash
git diff HEAD~1 HEAD
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191648.png>)

## Acció 3.13: Recuperar l'estat segur

S'ha retrocedit un commit i s'ha restaurat el contingut de la branca principal a l'estat anterior a la infecció.

```bash
git reset --hard HEAD~1
git status
git log --oneline -5
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191304.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191316.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191328.png>)

## Acció 3.14: Visualitzar l'historial final

S'ha representat gràficament l'historial de les branques i les fusions per verificar la topologia final del repositori.

```bash
git log --oneline --graph --decorate --all
git branch
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191338.png>)

## Acció 3.15: Publicar el repositori a GitHub

S'ha creat el repositori públic `halloween-git-rescue` i s'hi ha publicat el projecte amb els fitxers Markdown i les branques locals.

```bash
git remote add origin URL_DEL_REPOSITORI
git push -u origin main
git push -u origin feature-nightmare
git push -u origin feature-sanctuary
```

![alt text](<../captures/Captura de pantalla 2026-10-22 193537.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 193545.png>)
