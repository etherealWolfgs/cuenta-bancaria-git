# Cuenta bancaria — Git y pull requests

**Autor:** Genaro Salvador Morales Paoli

## Cómo correr

    ./correr.sh

## Mis pull requests

| # | Qué cambió |
|---|---|
| 1 | El estado de cuenta muestra cuántos retiros se hicieron y cuántos fueron gratis |
| 2 | README y evidencia de la práctica |

## Boleto de salida

1. ¿Qué diferencia hay entre `git add` y `git commit`?

   Respuesta: `git add` elige qué cambios van a entrar en el siguiente commit y los pasa al área de preparación (staging). `git commit` guarda en el historial una foto de lo que está en esa área, con un mensaje. Sin `add` no hay nada que commitear, y sin `commit` los cambios no quedan registrados.

2. ¿Por qué después del merge en GitHub tu `main` de Ubuntu no tenía el cambio hasta que hiciste `git pull`?

   Respuesta: Porque el merge ocurrió en el repositorio de GitHub (el remoto), y mi repositorio de Ubuntu es una copia aparte que no se actualiza sola. `git pull` trae los commits nuevos de `origin/main` y los integra en mi `main` local.

3. Abriste un PR y después hiciste otro commit en la misma rama. ¿Qué pasó con el PR?

   Respuesta: Se quedó abierto y se actualizó con el commit nuevo, porque un PR apunta a una rama y no a un commit fijo. Eso sí, el commit tiene que subirse con `git push` para aparecer en el PR.

4. ¿Por qué en un equipo nadie hace cambios directamente en `main`?

   Respuesta: Porque `main` debe ser la versión estable que funciona. Con ramas y pull requests los cambios se revisan y se prueban antes de entrar, así que un error no rompe el trabajo de los demás, y es más fácil ver qué cambió y deshacerlo si hace falta.