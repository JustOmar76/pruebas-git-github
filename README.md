# 🚀 Pruebas en Git y GitHub

Esta es una carpeta de pruebas para practicar, testear y aprender comandos de Git y GitHub de manera segura.

---

## 📌 Resumen de Comandos Aprendidos

### 1. Configuración Inicial
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu_email@ejemplo.com"
```

### 2. Inicializar y Vincular Repositorio
```bash
# Iniciar Git en una carpeta local
git init

# Crear/Cambiar el nombre de la rama principal a main
git branch -M main

# Conectar el repositorio local con GitHub
git remote add origin https://github.com/JustOmar76/pruebas-git-github.git

# Corregir la URL del remoto si te equivocas
git remote set-url origin https://github.com/JustOmar76/pruebas-git-github.git

# Verificar los remotos vinculados
git remote -v
```

### 3. Flujo Diario de Trabajo
```bash
# Ver el estado de los archivos (untracked, modified, staged)
git status

# Preparar archivos para la foto (Staging Area)
git add README.md
git add .               # Agrega todos los cambios

# Guardar la foto en el historial (Commit)
git commit -m "mensaje explicativo"

# Subir los cambios a GitHub por primera vez
git push -u origin main

# Subir cambios en futuros commits
git push
```
### 4. Ramas (Branches)
```bash
# Ver ramas locales y en que rama estas (*)
git branch

# Ver todas las ramas (locales + remotas)
git branch -a

# Crear una rama nueva y moverte a ella
git checkout -b feature/mi-primera-rama

# Forma moderna (equivale a lo anterior)
git switch -c feature/mi-primera-rama

# Cambiar entre ramas existentes
git checkout main
git switch main

# Subir una rama nueva a GitHub por primera vez
git push -u origin feature/mi-primera-rama

# Borrar rama local ya fusionada
git branch -d feature/mi-primera-rama

# Borrar rama remota + limpiar referencias viejas
git push origin --delete feature/mi-primera-rama
git fetch --prune
```

### 5. Pull Request y Merge
```bash
# 1. En GitHub: Pull requests > New pull request
# Base: main <- Compare: feature/mi-primera-rama
# Create pull request > Merge pull request > Confirm merge

# 2. Actualizar tu local despues del merge en GitHub
git checkout main
git pull
git log --oneline -5
```

### 6. Conflictos (Merge Conflict)
```bash
# Provocar: editar la MISMA linea en dos ramas y luego:
git checkout main
git merge feature/conflicto
# CONFLICT (content): Merge conflict in README.md

# Git marca el archivo asi:
# <<<<<<< HEAD
# Hola desde main
# =======
# Hola desde rama conflicto
# >>>>>>> feature/conflicto

# Resolver: editar el archivo, dejar UNA sola linea final,
# borrar las marcas <<<<<<< ======= >>>>>>>, guardar y luego:
git add README.md
git commit -m "fix: resolve merge conflict in greeting"
git push
```

> Saludo de prueba tras resolver el conflicto:
> Hola resuelto, aprendi a resolver conflictos!

### 7. Ver Historial y Comparar (solo lectura)
```bash
# Historial compacto con ramas y grafico
git log --oneline --graph --all -10

# Ver detalle y archivos de un commit
git show HEAD --stat
git show HEAD

# Evitar que el pager te atrape (q para salir del pager)
git --no-pager show HEAD --stat
git --no-pager log --oneline -5
git --no-pager diff
```

### 8. Deshacer Cambios y Stash
```bash
# Ver que cambio sin commitear
git status
git diff

# Descartar cambios de un archivo (volver a clean)
git restore README.md

# Sacar un archivo de staging (mantiene el cambio)
git restore --staged README.md

# Guardar cambios a medias en un bolsillo temporal
git stash
git status        # queda en working tree clean
git stash list    # stash@{0}: WIP on main...

# Recuperar lo guardado y borrar el stash
git stash pop
```

---
*Documento actualizado automáticamente durante la sesión de aprendizaje.*
