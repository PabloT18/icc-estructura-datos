![Logo Universidad](Files/ups-cc.png "UPS")



# Introducción a Git - Comandos Básicos

Git es un sistema de control de versiones distribuido que facilita el seguimiento de los cambios en los archivos y la colaboración entre múltiples personas. A continuación, se presentan algunos comandos básicos para empezar con Git:

## Configuración Inicial
Antes de comenzar a utilizar Git, es recomendable configurar tu nombre de usuario y correo electrónico, ya que esta información se utilizará en tus commits.

- **Configurar tu nombre de usuario**:
  ```bash
  git config --global user.name "Tu Nombre"
  ```
- **Configurar tu correo electrónico**:
  ```bash
  git config --global user.email "tuemail@example.com"
  ```

## Crear 
- **Iniciar un nuevo repositorio local**:
  ```bash
  git init
  ```

## Realizar Cambios
- **Verificar el estado del repositorio**:
  ```bash
  git status
  ```
- **Agregar cambios al próximo commit**:
  ```bash
  git add nombre_del_archivo
  ```
  Para agregar todos los cambios:
  ```bash
  git add .
  ```
- **Realizar un commit con los cambios**:
  ```bash
  git commit -m "Mensaje descriptivo del commit"
  ```

## Ramas
- **Crear una nueva rama**:
  ```bash
  git branch nombre_de_la_rama
  ```
- **Cambiar a otra rama**:
  ```bash
  git checkout nombre_de_la_rama
  ```
- **Combinar cambios de una rama a la actual**:
  ```bash
  git merge nombre_de_la_rama
  ```


## Inspeccionar y Comparar
- **Ver el historial de commits**:
  ```bash
  git log
  ```
- **Comparar cambios**:
  ```bash
  git diff
  ```

  ## Versiones
- **Cambiar a otro punto de historial**:
  ```bash
  git checkout <commit_hash>
  ```
- **Ultimo punto**:
  ```bash
  git checkout -- .
  ```

- **Deshacer cambios en tu repositorio local**:

  Según el flag que utilices (--soft, --mixed, --hard), puedes afectar el directorio de trabajo, el área de staging, y tu historial de commits.

  - **reset**
  
      Para eliminar los cambios hasta un commit específico, manteniendo los cambios en tu directorio de trabajo:
      ```bash
      git reset --soft <commit_hash>
      ```

  - **mixed**
  
      Para eliminar los cambios hasta un commit específico, manteniendo los cambios en tu directorio de trabajo y área de staging:
      ```bash
      git reset --mixed <commit_hash>
      ```

  - **hard**
  
     Para eliminar todos los cambios hasta un commit específico:
      ```bash
      git reset --hard <commit_hash>
      ```


- **Invierte los cambios**:

  A diferencia de git reset, git revert crea un nuevo commit que invierte los cambios especificados. Esto es útil para deshacer cambios en repositorios compartidos sin alterar el historial.
  ```bash
  git revert <commit_hash>
  ```

## Repositorios Remotos 
- **Clonar un repositorio existente**:

  Para obtener una copia local de un repositorio que se encuentra alojado en un servidor remoto (como GitHub, GitLab, Bitbucket, etc.):

  ```bash
  git clone url_del_repositorio
  ```

- **Añadir un Repositorio Remoto**:

  Si has iniciado un repositorio local y deseas conectarlo a un repositorio remoto:

  ```bash
  git remote add nombre_remoto url_del_repositorio
  ```

  Donde nombre_remoto es generalmente origin, que es el nombre estándar para el repositorio principal de donde se clonó.

- **Subir Cambios a un Repositorio Remoto**:

  Después de hacer commit a tus cambios en el repositorio local, puedes subirlos al repositorio remoto:

  ```bash
  git push nombre_remoto nombre_de_la_rama
  ```

- **Bajar Cambios del Repositorio Remoto**:

  Para actualizar tu repositorio local con los cambios más recientes del repositorio remoto:

  ```bash
  git pull nombre_remoto nombre_de_la_rama
  ```

  Este comando es una combinación de git fetch (que descarga contenido del repositorio remoto) y git merge (que integra el contenido recién descargado en tu rama de trabajo local).


- **Subir una Nueva Rama al Remoto**:

  Para actualizar tu repositorio local con los cambios más recientes del repositorio remoto:

  ```bash
  git push -u nombre_remoto nombre_de_la_rama
  ```

  El flag -u establece el upstream para tu rama, lo que facilita futuros git pull sin necesidad de especificar el nombre de la rama.

