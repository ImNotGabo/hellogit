# Uso de `git checkout`

El comando `git checkout` se utiliza para cambiar entre ramas en un repositorio de Git, o para restaurar archivos en el área de trabajo. Al ejecutar `git checkout <nombre_rama>`, se cambia a la rama especificada, actualizando el área de trabajo con el contenido de esa rama. También puede utilizarse para hacer un "checkout" de un commit específico o de una etiqueta, creando un estado de "detached HEAD". En este caso, si se desea hacer modificaciones, se debe crear una nueva rama a partir de ese commit o etiqueta con el comando `git checkout -b <nueva_rama>`. Este comando es esencial para navegar entre diferentes versiones de un proyecto y realizar cambios sin afectar la rama principal.

# Uso de `git reset --hard`

El comando `git reset --hard` se utiliza para deshacer commits y restaurar el estado del repositorio a un punto anterior, eliminando tanto los cambios en el historial como en el área de trabajo y el staging. Es especialmente útil para descartar modificaciones de manera permanente, pero debe usarse con precaución ya que los cambios eliminados no se pueden recuperar fácilmente. Si necesitas deshacer un `reset --hard`, puedes utilizar `git reflog` para encontrar el commit perdido y restaurarlo. Este comando es ideal para situaciones donde quieres revertir por completo el estado de tu proyecto a un commit específico.

# Uso de `git tag`

El comando `git tag` se utiliza para crear referencias específicas a un punto en la historia de un repositorio, comúnmente para marcar versiones o lanzamientos importantes del proyecto. Existen dos tipos de etiquetas: las ligeras, que actúan como un marcador simple a un commit, y las anotadas, que almacenan metadatos adicionales como el nombre del autor, la fecha y un mensaje descriptivo. Las etiquetas no se envían automáticamente al repositorio remoto, por lo que es necesario usar `git push origin <nombre_etiqueta>` o `git push origin --tags` para publicarlas. Esto facilita la gestión de versiones y permite identificar rápidamente hitos importantes en el desarrollo.

# Uso de `git branch`

El comando `git branch` se utiliza para gestionar ramas en Git, permitiendo crear, listar, cambiar, renombrar y eliminar ramas en un repositorio. Para listar las ramas locales, se usa `git branch`, mientras que `git branch -a` muestra tanto las ramas locales como remotas. Para crear una nueva rama sin cambiar a ella, se emplea `git branch <nombre-rama>`, y para crearla y cambiar a ella simultáneamente, se utiliza `git switch -c <nombre-rama>`. Además, puedes renombrar una rama con `git branch -m <nuevo-nombre>` o eliminarla con `git branch -d <nombre-rama>`. Este comando es esencial para trabajar con múltiples flujos de trabajo y colaborar eficientemente en proyectos.

# Uso de `git switch`

El comando `git switch` se utiliza para cambiar entre ramas en un repositorio de Git de forma rápida y sencilla. Puedes cambiar a una rama existente con `git switch <nombre_rama>`, o crear y cambiar a una nueva rama con `git switch -c <nombre_nueva_rama>`. Este comando es una alternativa más clara y específica a `git checkout` cuando se trabaja exclusivamente con ramas, mejorando la legibilidad y evitando confusiones. Además, puedes forzar el cambio de rama descartando cambios locales no guardados con `git switch -f <nombre_rama>`.

## Uso de `git merge`

El comando `git merge` se utiliza para **combinar los cambios de una rama en otra**, integrando las diferencias en la rama actual. Si las ramas tienen una línea de desarrollo común, Git puede realizar un **merge fast-forward**, avanzando el puntero de la rama principal al último commit de la rama fusionada. Sin embargo, si ambas ramas han divergido, Git realizará una **fusión de tres vías**, creando un commit de merge para unir los historiales de ambas ramas.
