
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

## Crear y Clonar Repositorios
- **Iniciar un nuevo repositorio local**:
  ```bash
  git init
  ```
- **Clonar un repositorio existente**:
  ```bash
  git clone url_del_repositorio
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

## Actualizar y Publicar
- **Obtener los últimos cambios del servidor remoto**:
  ```bash
  git pull
  ```
- **Publicar cambios locales en el servidor remoto**:
  ```bash
  git push origin nombre_de_la_rama
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
