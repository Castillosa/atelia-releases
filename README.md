# atelia-releases

Repositorio **público** de distribución de [Atelia](https://github.com/Castillosa/atelia).
Contiene únicamente binarios y los manifiestos de auto-update; **el código fuente vive en el repo privado** `Castillosa/atelia`.

## Por qué existe

El updater de Tauri descarga el manifiesto y los binarios **sin credenciales**. Con el
repo de código en privado, GitHub bloquea el acceso anónimo y el auto-update deja de
funcionar. Publicando aquí (público) se resuelve sin exponer el código.

## Endpoints estables del updater (vía GitHub Pages)

La app apunta a estas URLs, que **no cambian aunque se mueva el hosting**:

- Estable: `https://castillosa.github.io/atelia-releases/stable/latest.json`
- Nightly: `https://castillosa.github.io/atelia-releases/nightly/latest.json`

Cada release del workflow en el repo privado publica aquí los artefactos firmados y
actualiza el `latest.json` correspondiente. Si algún día se cambia dónde se alojan los
binarios, basta regenerar el manifiesto (o reapuntar un dominio propio sobre Pages):
**las apps instaladas no necesitan recompilarse**.
