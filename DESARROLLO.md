# Flujo de Desarrollo - Aretaslab Web

## Arquitectura

- **Sitio web:** Hugo (generador estático)
- **Hosting:** GitHub Pages (palpidcourses.github.io/aretaslab-web)
- **Desarrollo local:** Cloudflare Tunnel (nono.aretaslab.tech)
- **Dominio Cloudflare:** nono.aretaslab.tech → puerto 80 local

## Workflow

### 1. Desarrollo Local

```bash
# Iniciar entorno de desarrollo completo
/home/ubuntu/.openclaw/workspace/scripts/aretaslab_dev_full.sh
```

Este script:
- Compila Hugo en modo watch (recarga automática al editar archivos)
- Sirve el contenido con nginx (Docker) en puerto 80
- Acceso externo via Cloudflare Tunnel: http://nono.aretaslab.tech

### 2. Editar Archivos

**Estructura del proyecto:**
```
aretaslab-web/
├── content/           # Contenido en Markdown
│   └── _index.md    # Página principal
├── layouts/           # Templates HTML personalizados
│   ├── _default/
│   │   └── baseof.html  # Template base
│   └── index.html      # Página principal
├── static/            # Archivos estáticos (CSS, JS, imágenes)
├── hugo.yaml         # Configuración
└── docker-compose.dev.yml  # Nginx para desarrollo
```

**Archivos clave:**
- `hugo.yaml` - Configuración, colores, menús
- `content/_index.md` - Contenido de la home
- `layouts/index.html` - Layout de la home
- `layouts/_default/baseof.html` - Template base

### 3. Testing

- Editar archivos en `/home/ubuntu/development/aretaslab-web`
- Hugo recompila automáticamente
- Ver cambios en: http://nono.aretaslab.tech
- Probar en móvil, tablet, desktop

### 4. Deploy a GitHub Pages

Cuando esté todo bien:

```bash
/home/ubuntu/.openclaw/workspace/scripts/aretaslab_deploy.sh
```

Este script:
- Compila Hugo en modo producción
- Pide mensaje del commit
- Hace commit y push a GitHub
- GitHub Actions despliega automáticamente

### 5. Verificar

- URL pública: https://palpidcourses.github.io/aretaslab-web/
- GitHub Actions: https://github.com/PalpidCourses/aretaslab-web/actions

## Scripts Disponibles

| Script | Uso |
|--------|------|
| `aretaslab_dev_full.sh` | Iniciar desarrollo completo (Hugo + nginx) |
| `aretaslab_dev.sh` | Solo servidor Hugo (puerto 1313) |
| `aretaslab_deploy.sh` | Deploy a GitHub Pages |

## Comandos Hugo Útiles

```bash
# Compilar sitio
hugo

# Compilar para producción
hugo --minify

# Servir en modo desarrollo
hugo server --buildDrafts

# Crear nueva página
hugo new content/nueva-pagina.md
```

## Cloudflare Tunnel

- **Dominio:** nono.aretaslab.tech
- **Puerto local:** 80
- **Estado:** ✅ Activo

Para desarrollo, el Docker nginx sirve en puerto 80 y Cloudflare Tunnel lo expone externamente.

## GitHub Actions

**Workflow:** `.github/workflows/hugo.yml`

Se ejecuta automáticamente con cada push a `main`:
1. Checkout código
2. Instala Hugo
3. Compila sitio
4. Deploy a GitHub Pages

## Personalización

### Cambiar Colores

Editar `hugo.yaml`:
```yaml
style:
  colors:
    background: '#F7F3F0'    # Fondo
    primary: '#D4A373'        # Color principal
    secondary: '#A98467'      # Acento
```

### Añadir Páginas

```bash
# Crear nueva página
hugo new content/nueva-pagina.md
```

Luego editar el archivo y añadir al menú en `hugo.yaml`.

### Modificar Layout

Editar archivos en `layouts/`:
- `layouts/_default/baseof.html` - Template base (header, footer)
- `layouts/index.html` - Página principal
- `layouts/_default/single.html` - Páginas individuales

## Gestión del Equipo

### Añadir Nuevo Miembro

1. Editar `data/equipo.yml`:
```yaml
equipo:
  - nombre: "Nombre Apellido"
    rol: "Cargo o rol"
    bio: "Descripción breve"
    imagen: "/images/equipo/nombre.svg"  # o .jpg/.png
    linkedin: "https://linkedin.com/in/..."   # Opcional
    bluesky: "https://bsky.app/profile/..."   # Opcional
    github: "https://github.com/..."            # Opcional
```

2. Añadir foto al directorio `/static/images/equipo/`:
```bash
# Copiar imagen (se recomienda 400x400px)
cp /ruta/foto.jpg /home/ubuntu/development/aretaslab-web/static/images/equipo/nombre.jpg
```

### Generar Nuevos Avatares

Para crear avatares SVG con iniciales:
```bash
/home/ubuntu/.openclaw/workspace/scripts/generar_avatares_equipo.sh
```

Este script genera avatares con círculos de colores terrosos y las iniciales de cada miembro.

### Reemplazar Avatar con Foto Real

```bash
# Copiar foto al directorio del equipo
cp /ruta/foto-real.jpg /home/ubuntu/development/aretaslab-web/static/images/equipo/david.jpg

# Actualizar data/equipo.yml para usar .jpg en lugar de .svg
```

### Miembros del Equipo

| Miembro | Rol | Avatar |
|---------|------|---------|
| David Palazón | Fundador & Desarrollador Principal | /images/equipo/david.svg |
| Nono | Daemon Digital & Operaciones | /images/equipo/nono.svg |
| Laia Puig | Secretaria & Operaciones | /images/equipo/laia.svg |
| Hugo Fernández | Asesor Legal | /images/equipo/hugo.svg |
| Marc Solé | Desarrollador Full-stack | /images/equipo/marc.svg |
| Àlex Riera | Desarrollador MCP / C# | /images/equipo/alex.svg |
| Carla Vidal | Marketing & Redes Sociales | /images/equipo/carla.svg |
| Pau Martí | Product Owner: Gastos Familia & Mcpone | /images/equipo/pau.svg |
| Marta López | Product Owner: Solorol | /images/equipo/marta.svg |
| Leo Costa | Coach de Salud | /images/equipo/leo.svg |
