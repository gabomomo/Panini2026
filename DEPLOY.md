# Instrucciones para subir a Git

## 1. Crear un repositorio en GitHub/GitLab

### En GitHub:
1. Ve a https://github.com/new
2. Nombre: `panini-2026-tracker`
3. Descripción: `Panini FIFA World Cup 2026 Figuritas Tracker`
4. Privado/Público (tu elección)
5. Crea el repositorio
6. Copia el URL (ej: `https://github.com/tu-usuario/panini-2026-tracker.git`)

## 2. Inicializar Git localmente

```bash
cd /Volumes/UNDERGROUND/CLIENTES/PANINI2026

# Inicializar repositorio
git init

# Agregar archivos
git add .

# Commit inicial
git commit -m "Initial commit: Panini 2026 Tracker app"

# Agregar repositorio remoto (reemplaza URL)
git remote add origin https://github.com/tu-usuario/panini-2026-tracker.git

# Push a main/master
git branch -M main
git push -u origin main
```

## 3. Para usar desde Git en otra máquina

```bash
# Clonar
git clone https://github.com/tu-usuario/panini-2026-tracker.git
cd panini-2026-tracker

# Abrir en navegador
# Opción 1: Directamente
open index.html

# Opción 2: Servidor local
python -m http.server 8000
# Accede a http://localhost:8000/index.html
```

## 4. Futuros cambios

```bash
# Hacer cambios, luego:
git add .
git commit -m "Descripción del cambio"
git push
```

## Estructura del repositorio

```
panini-2026-tracker/
├── index.html       # Aplicación principal
├── README.md              # Documentación
├── package.json           # Metadatos del proyecto
├── .gitignore             # Archivos a ignorar en Git
└── DEPLOY.md              # Este archivo
```

## Notas importantes

- Los credenciales de Supabase están en el HTML (anon key, que es segura públicamente)
- No hagas commit de datos sensibles (tokens, passwords, etc.)
- Si cambias la key de Supabase, recuerda actualizar el HTML antes de pushear
- El archivo es autocontenido: no necesita build ni dependencias

## Alternativas de hosting

Puedes servir directamente desde Git:

### Vercel
```bash
vercel --prod
```

### Netlify
```bash
netlify deploy --prod --dir=.
```

### GitHub Pages
```bash
# En settings del repo: GitHub Pages → Deploy from branch
# Selecciona main, root directory
# La app estará en: https://tu-usuario.github.io/panini-2026-tracker/
```

---

Una vez en Git, podés compartir el URL directamente y otros usuarios pueden:
1. Clonar el repo
2. Abrir el HTML en navegador o servir localmente
3. Usar la app sin instalar nada
