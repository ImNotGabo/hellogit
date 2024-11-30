# Uso de `git reset --hard`

El comando `git reset --hard` se utiliza para deshacer commits y restaurar el estado del repositorio a un punto anterior, eliminando tanto los cambios en el historial como en el área de trabajo y el staging. Es especialmente útil para descartar modificaciones de manera permanente, pero debe usarse con precaución ya que los cambios eliminados no se pueden recuperar fácilmente. Si necesitas deshacer un `reset --hard`, puedes utilizar `git reflog` para encontrar el commit perdido y restaurarlo. Este comando es ideal para situaciones donde quieres revertir por completo el estado de tu proyecto a un commit específico.

# Uso de `git tag`

El comando `git tag` se utiliza para crear referencias específicas a un punto en la historia de un repositorio, comúnmente para marcar versiones o lanzamientos importantes del proyecto. Existen dos tipos de etiquetas: las ligeras, que actúan como un marcador simple a un commit, y las anotadas, que almacenan metadatos adicionales como el nombre del autor, la fecha y un mensaje descriptivo. Las etiquetas no se envían automáticamente al repositorio remoto, por lo que es necesario usar `git push origin <nombre_etiqueta>` o `git push origin --tags` para publicarlas. Esto facilita la gestión de versiones y permite identificar rápidamente hitos importantes en el desarrollo.
