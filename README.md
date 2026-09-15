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
### 4. Pruebas en ramas
```bash
# Saludo desde mi-primera-rama
Hola resuelto, aprendi a resolver conflictos!
```
---
*Documento actualizado automáticamente durante la sesión de aprendizaje.*
