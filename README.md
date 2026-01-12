# 📱 Instagram Stories Clone

> **Clon funcional de Instagram Stories construido con React, TypeScript y LocalStorage**

![React](https://img.shields.io/badge/React-18.2-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue)
![Vite](https://img.shields.io/badge/Vite-5.0-purple)
![Tailwind](https://img.shields.io/badge/Tailwind-3.4-cyan)

## 👤 Autor

**Xisco Rossello**  
IFC33 - 2º Curso  
Enero 2026

## 📝 Descripción del Proyecto

Este proyecto es una implementación completa de las historias de Instagram, desarrollado como práctica de desarrollo frontend con React y TypeScript. La aplicación permite subir, visualizar y gestionar historias que expiran automáticamente después de 24 horas, simulando fielmente el comportamiento de la aplicación original.

## ✨ Características Implementadas

- 📸 **Subida de imágenes** - Selector de archivos con conversión automática a historias
- ⏰ **Sistema de expiración** - Las historias se eliminan automáticamente tras 24 horas
- ⏱️ **Reproducción automática** - Timer de 3 segundos por historia con barra de progreso visual
- 👆 **Interacción intuitiva** - Gestos táctiles (swipe, tap, hold) para una navegación fluida
- 💾 **Persistencia local** - Almacenamiento en LocalStorage sin necesidad de backend
- 📱 **Diseño responsive** - Adaptado para dispositivos móviles y escritorio
- 🎨 **UI fiel al original** - Círculos con gradiente, animaciones y efectos visuales
- 🖼️ **Optimización de imágenes** - Redimensionado y compresión automática

## 🛠️ Stack Tecnológico

- **Framework**: React 18 con Hooks modernos
- **Lenguaje**: TypeScript para tipado estático
- **Build Tool**: Vite (compilación rápida)
- **Estilos**: Tailwind CSS (utility-first)
- **Almacenamiento**: LocalStorage API
- **Procesamiento**: Canvas API y FileReader para imágenes

## 📦 Instalación y Ejecución

```bash
# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev

# Compilar para producción
npm run build

# Previsualizar build de producción
npm run preview
```

La aplicación estará disponible en `http://localhost:5173`

## 🏗️ Estructura del Proyecto

```
src/
├── components/          # Componentes UI
│   ├── StoryList.tsx   # Lista horizontal de historias
│   ├── StoryViewer.tsx # Visor fullscreen
│   └── ProgressBar.tsx # Barras de progreso animadas
├── hooks/              # Custom Hooks
│   ├── useStories.ts   # Gestión de historias
│   └── useStoryViewer.ts # Control del visor
├── utils/              # Utilidades
│   ├── storage.ts      # LocalStorage + expiración
│   └── imageUtils.ts   # Procesamiento de imágenes
└── types/              # Tipos TypeScript
```

## 📚 Aprendizajes y Conceptos Aplicados

Este proyecto ha permitido aplicar y profundizar en diversos conceptos avanzados de desarrollo web:

### APIs del Navegador
- **FileReader API** - Lectura y conversión de archivos a formato Base64
- **Canvas API** - Manipulación, redimensionado y compresión de imágenes
- **LocalStorage** - Persistencia de datos sin necesidad de backend
- **Touch Events** - Detección de gestos táctiles para dispositivos móviles

### React Avanzado
- **Custom Hooks** - `useStories` y `useStoryViewer` para lógica reutilizable
- **Gestión de Estado** - useState para estados locales y sincronización
- **Efectos** - useEffect para timers y limpieza de recursos
- **Referencias** - useRef para evitar problemas de stale closures
- **Callbacks** - useCallback para optimización de rendimiento

### Patrones y Buenas Prácticas
- Arquitectura basada en componentes reutilizables
- Tipado fuerte con TypeScript e interfaces
- Separación de responsabilidades (hooks, utils, components)
- Limpieza automática de recursos y memory leaks
- Optimización de imágenes para mejorar rendimiento

## 🎮 Guía de Uso

### Crear una Nueva Historia
1. Haz click en el botón "+" de la interfaz
2. Selecciona una imagen desde tu dispositivo
3. La imagen se procesará automáticamente y aparecerá como una nueva historia

### Visualizar Historias
- **Click en un círculo**: Abre el visor de historias
- **Tap lado izquierdo**: Retrocede a la historia anterior
- **Tap lado derecho**: Avanza a la siguiente historia
- **Swipe horizontal**: Navega entre usuarios/historias
- **Mantener pulsado**: Pausa la reproducción automática
- **Flechas ←/→**: Navegación con teclado (escritorio)
- **Tecla ESC**: Cierra el visor de historias

### Gestión Automática
- Las historias se eliminan automáticamente tras 24 horas
- Las imágenes se optimizan automáticamente para ahorrar espacio
- El sistema limpia historias expiradas al cargar la aplicación

## 🔧 Detalles Técnicos

### Especificaciones
- **Tamaño máximo de imagen**: 1080x1920px (redimensionado automático)
- **Límite de almacenamiento**: ~5MB (LocalStorage browser)
- **Capacidad aproximada**: ~25-30 historias
- **Duración por historia**: 3 segundos con progreso visual
- **Tiempo de expiración**: 24 horas desde la creación

### Optimizaciones Implementadas
- Compresión JPEG al 85% de calidad
- Redimensionado inteligente manteniendo ratio de aspecto
- Limpieza automática de historias expiradas al iniciar
- Animaciones optimizadas a 60fps
- Lazy loading de imágenes

### Mejoras y Soluciones
- **Stale closures**: Solucionado mediante refs en los hooks
- **Memory leaks**: Limpieza exhaustiva de timers y eventos
- **Gestión de storage**: Sistema de compresión para maximizar capacidad

## � Documentación Adicional

- 📖 **[CLASE_MAGISTRAL.md](docs/CLASE_MAGISTRAL.md)** - Documentación técnica detallada
- 📝 **[bitacora.md](docs/bitacora.md)** - Registro del proceso de desarrollo

---

## 🎓 Conclusiones

Este proyecto representa una implementación completa de una funcionalidad compleja de redes sociales, demostrando dominio de:
- React y su ecosistema moderno
- TypeScript y tipado estático
- APIs nativas del navegador
- Gestión de estado y efectos secundarios
- Optimización de rendimiento
- UX/UI responsive y accesible

**Xisco Rossello** - IFC33 2º Curso - Enero 2026
