# 🎨 ractuzed

Mis dotfiles personales para **Sway** con estética **Nord** minimalista y atajos fáciles de aprender.

> Inspirado en [fluix-dev/dotfiles](https://github.com/fluix-dev/dotfiles), pero optimizado para ser **fácil de usar** sin necesidad de compilar ni usar AUR.

---

## 📸 Características

- **Estilo visual**: Paleta Nord (azules fríos, grises suaves)
- **Fuente**: JetBrains Mono
- **Barra**: Waybar completo con iconos de red, batería, audio, reloj y bandeja de sistema
- **Lanzador**: Wofi con bordes redondeados
- **Notificaciones**: Mako con bordes cyan
- **Fondo de pantalla**: Imagen personalizada (o color sólido Nord)

---

## 📦 Requisitos

Solo paquetes oficiales de Arch Linux (nada de AUR, nada de `yay`, nada de compilar):

```bash
sudo pacman -S sway waybar wofi mako alacritty ttf-jetbrains-mono ttf-font-awesome wget
```

---

## 🚀 Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/plandezerr-commits/ractuzed.git ~/.config/ractuzed
```

O si no usas Git, descarga el ZIP y descomprímelo en `~/.config/ractuzed/`.

### 2. Descargar wallpaper (opcional)

Si quieres usar el fondo de pantalla incluido:

```bash
mkdir -p ~/.config/ractuzed/wallpapers
wget -O ~/.config/ractuzed/wallpapers/nord-wallpaper.jpg "https://images.unsplash.com/photo-1557683316-973673baf926?w=1920"
```

O usa tu propia imagen y edita la línea `output * bg` en `sway/config`.

### 3. Crear enlaces simbólicos

Para que los programas encuentren la configuración, ejecuta:

```bash
ln -sf ~/.config/ractuzed/sway ~/.config/sway
ln -sf ~/.config/ractuzed/waybar ~/.config/waybar
ln -sf ~/.config/ractuzed/wofi ~/.config/wofi
ln -sf ~/.config/ractuzed/mako ~/.config/mako
ln -sf ~/.config/ractuzed/alacritty ~/.config/alacritty
```

### 4. Iniciar Sway

Cierra sesión y selecciona **Sway** en tu pantalla de inicio (GDM, SDDM, LightDM, etc.).

---

## ⌨️ Atajos de teclado

Todos los atajos usan la tecla **`Super`** (tecla Windows). Diseñados para ser intuitivos:

| Acción | Atajo |
|--------|-------|
| 🖥️ Abrir terminal | `Super + Enter` |
| 🔍 Lanzador de apps | `Super + Espacio` |
| ❌ Cerrar ventana | `Super + Shift + Q` |
| 🔄 Recargar configuración | `Super + Shift + R` |
| 🚪 Salir de Sway | `Super + Shift + E` |
| ➡️ Mover foco | `Super + Flechas` |
| 📦 Mover ventana | `Super + Shift + Flechas` |
| 📏 Redimensionar | `Super + R` (luego flechas, `Escape` para salir) |
| 🖼️ Pantalla completa | `Super + F` |
| 🎈 Ventana flotante | `Super + Shift + Espacio` |
| 🔀 Dividir horizontal | `Super + H` |
| 🔀 Dividir vertical | `Super + V` |
| 📂 Cambiar workspace | `Super + 1-5` |
| 📤 Mover a workspace | `Super + Shift + 1-5` |

---

## 📂 Estructura de archivos

```
ractuzed/
├── sway/
│   ├── config          # Configuración principal de Sway
│   └── colors.conf     # Paleta de colores Nord
├── waybar/
│   ├── config          # Módulos de la barra (red, batería, audio, reloj, bandeja)
│   └── style.css       # Estilos Nord para Waybar
├── wofi/
│   ├── config          # Configuración del lanzador
│   └── style.css       # Estilos Nord para Wofi
├── mako/
│   └── config          # Notificaciones minimalistas
├── alacritty/
│   └── alacritty.toml  # Terminal con colores Nord
├── wallpapers/
│   └── nord-wallpaper.jpg  # Fondo de pantalla (opcional)
└── README.md           # Este archivo
```

---

## 🎨 Programas incluidos

| Programa | Función |
|----------|---------|
| **Sway** | Window manager tiling para Wayland |
| **Waybar** | Barra superior con workspaces, red, batería, audio, reloj y bandeja de sistema |
| **Wofi** | Lanzador de aplicaciones estilo Rofi |
| **Mako** | Daemon de notificaciones ligero |
| **Alacritty** | Terminal rápida con colores Nord |

---

## 🎨 Paleta de colores (Nord)

| Color | Código | Uso |
|-------|--------|-----|
| Nord0 | `#2e3440` | Fondo principal |
| Nord1 | `#3b4252` | Fondo secundario |
| Nord3 | `#4c566a` | Comentarios / inactivo |
| Nord4 | `#eceff4` | Texto principal |
| Nord8 | `#88c0d0` | Acento cyan |
| Nord11 | `#bf616a` | Errores / urgente |
| Nord14 | `#a3be8c` | Éxito / batería |

---

## 🔧 Waybar - Módulos incluidos

La barra superior incluye estos módulos de izquierda a derecha:

- **Izquierda**: Workspaces con iconos
- **Centro**: Título de la ventana activa
- **Derecha**:
  - 🌐 **Red**: WiFi/Ethernet con nombre de red y señal
  - 🔊 **Audio**: Volumen con iconos dinámicos
  - 🔋 **Batería**: Porcentaje con iconos de carga
  - 🕐 **Reloj**: Hora actual con calendario en tooltip
  - 📥 **Bandeja**: Iconos de aplicaciones (Discord, Steam, etc.)

---

## 🙏 Créditos

- Estética original: [fluix-dev/dotfiles](https://github.com/fluix-dev/dotfiles)
- Paleta de colores: [Nord Theme](https://www.nordtheme.com/)
- Fuente: [JetBrains Mono](https://www.jetbrains.com/lp/mono/)
- Wallpaper: [Unsplash](https://unsplash.com/)

---

## 📝 Licencia

Libre para usar, modificar y compartir. ¡Disfruta tu setup! ✨

---

## 🔄 Actualizar en el futuro

Cuando hagas cambios, solo necesitas:

```bash
cd ~/.config/ractuzed
git add .
git commit -m "Descripción del cambio"
git push
```

O sube los archivos directamente desde la web de GitHub arrastrándolos.
