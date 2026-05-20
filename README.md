# Panini FIFA World Cup 2026 - Tracker

Aplicación web para rastrear y coleccionar figuritas del álbum oficial de Panini para la Copa Mundial FIFA 2026.

## 🎯 Características

- ✅ Registro e inicio de sesión con PIN de 4 dígitos
- 📊 Seguimiento de figuritas por grupo, equipo y secciones especiales
- 🏆 Ranking global de coleccionistas
- 📋 Vista de faltantes completa por equipo y grupo
- 💾 Sincronización automática en Supabase
- 🎨 Interfaz moderna y responsiva

## 🚀 Inicio rápido

### Opción 1: Usar directamente en el navegador
Simplemente abre `index.html` en tu navegador:
```bash
# En macOS
open index.html

# O arrastra el archivo al navegador
```

### Opción 2: Servidor local (recomendado)
```bash
# Con Python 3
python -m http.server 8000

# Con Node + http-server
npx http-server
```
Luego accede a `http://localhost:8000/index.html`

## 📋 Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Conexión a Internet
- Cuenta en Supabase (ya configurada)

## 🔐 Autenticación

- **Registro**: Email único + Nombre + Avatar + PIN de 4 dígitos
- **Inicio de sesión**: Email + PIN de 4 dígitos
- Los datos se sincronizan automáticamente en Supabase

## 📦 Estructura

```
panini-2026/
├── index.html        # Aplicación principal
├── .gitignore        # Configuración de Git
├── package.json      # Metadatos del proyecto
├── README.md         # Documentación
└── DEPLOY.md         # Instrucciones de despliegue
```

## 🛠️ Tecnologías

- **Frontend**: React 18 (via CDN)
- **Backend/DB**: Supabase
- **Estilos**: CSS inline
- **Transpilador**: Babel (via CDN)

## 📊 Datos de la colección

- **Total de figuritas**: 980
- **Grupos**: A–L (12 grupos)
- **Equipos por grupo**: 3–4 equipos
- **Figuras por equipo**: 20 figuras
- **Secciones especiales**: 3 (FWC, FIFA Museum, Coca-Cola)

## 🔧 Configuración de Supabase

La app ya viene configurada con credenciales de Supabase. Si necesitas cambiar el proyecto:

1. Abre `index.html`
2. Busca las líneas:
   ```javascript
   const SB   = "https://lzkkobgdtzfxfcbhvjzj.supabase.co";
   const KEY  = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...";
   ```
3. Reemplaza con tus credenciales de Supabase

## 📱 Funcionalidades principales

- Registro e inicio de sesión con email + PIN
- Vista de seguimiento por grupos y equipos
- Búsqueda de equipos y figuritas
- Lista de faltantes organizada por grupo/equipo
- Ranking global de coleccionistas

## 💾 Almacenamiento

- **Local**: `localStorage` para usuarios y sesión
- **Cloud**: Supabase para progreso y perfiles

## 🐛 Solución de problemas

### Error de rate limit (429)
Si ves `over_email_send_rate_limit`:
- Espera 5-10 minutos antes de intentar nuevamente
- No intentes crear múltiples cuentas en corto tiempo
- Revisa tu conexión a Internet

### No carga Babel/React
- Verifica tu conexión a Internet
- Intenta recargar la página (Ctrl+F5)
- Los scripts se cargan desde CDN (jsDelivr)

### Datos no se sincronizan
- Verifica que tengas acceso a Internet
- Abre la consola del navegador (F12) para ver errores
- Confirma que tu sesión sea válida

## 📄 Licencia

Privado - Uso exclusivo

## 👤 Autor

Panini 2026 Tracker v1.0
