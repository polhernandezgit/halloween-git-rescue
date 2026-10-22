
# Bloc 1: Invocació del Repositori i Línia Base

## Acció 3.1: Crear el repositori

S'ha creat el directori del projecte i s'ha inicialitzat Git amb la branca principal `main`.

```bash
mkdir server-room-horror
cd server-room-horror
git init -b main
git status
```

![alt text](<../captures/Captura de pantalla 2026-10-22 190643.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 190928.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 190938.png>)

## Acció 3.2: Configurar la identitat

S'ha configurat el nom i el correu que identifiquen l'autor dels commits.

```bash
git config --global user.name "El teu nom i cognom"
git config --global user.email "el_teu_correu@example.com"
git config --global --list
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191001.png>)

## Acció 3.3: Crear el fitxer principal i fer el primer commit

S'ha creat `main.js` amb el missatge inicial del sistema de monitoratge.

```bash
git add main.js
git commit -m "feat: initialize server room monitoring"
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191012.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191020.png>)

## Acció 3.4: Registrar les dues modificacions successives

S'han afegit l'estat inicial de seguretat i el missatge que mostra aquest estat. Cada canvi s'ha registrat en un commit independent.

```bash
git add main.js
git commit -m "feat: define initial building security status"
git add main.js
git commit -m "feat: display building security status"
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191027.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191035.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191042.png>)

## Acció 3.5: Consultar l'historial

S'ha consultat l'historial simplificat per verificar els tres commits inicials.

```bash
git log --oneline
git status
```

![alt text](<../captures/Captura de pantalla 2026-10-22 191050.png>)

![alt text](<../captures/Captura de pantalla 2026-10-22 191058.png>)
