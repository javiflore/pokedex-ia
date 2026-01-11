# Instrucciones para el Agente de IA

## Reglas de Procedimiento

### 1. Registro en el Diario (DIARIO.md)
- **SIEMPRE** actualizar `DIARIO.md` antes de ejecutar cualquier tarea
- Cada entrada debe ser de 1-2 líneas máximo
- Si se ejecuta un comando, incluir el comando exacto entre paréntesis
- Formato: `N. Descripción breve (comando si aplica)`
- Agrupar por fecha

### 2. Formato de Entradas
```
## DD/MM/YYYY
1. Descripción de la tarea (`comando ejecutado`)
2. Otra tarea realizada
```

### 3. Flujo de Trabajo
1. Actualizar `DIARIO.md` con la nueva solicitud
2. Ejecutar la tarea solicitada
3. Confirmar completitud

## Buenas Prácticas de Programación

### Estructura de Proyecto
- **Organización modular**: Separar código en carpetas lógicas (`components/`, `services/`, `types/`, `utils/`, `hooks/`)
- **Naming conventions**: Usar PascalCase para componentes, camelCase para funciones/variables
- **Archivos pequeños**: Máximo 200-300 líneas por archivo

### TypeScript
- **Tipado estricto**: Evitar `any`, usar tipos e interfaces explícitas
- **Interfaces sobre types**: Preferir `interface` para objetos, `type` para uniones/intersecciones
- **Exports nombrados**: Evitar default exports excepto en páginas de Next.js

### React/Next.js
- **Server Components por defecto**: Usar "use client" solo cuando sea necesario
- **Separación de responsabilidades**: Lógica de negocio en servicios, componentes solo para UI
- **Custom hooks**: Extraer lógica reutilizable en hooks personalizados
- **Componentes puros**: Evitar efectos secundarios innecesarios

### API y Datos
- **Manejo de errores**: Implementar try-catch y validaciones
- **Loading states**: Mostrar estados de carga y error al usuario
- **Cache apropiado**: Usar estrategias de cache de Next.js
- **Variables de entorno**: Nunca hardcodear URLs o keys

### Estilos
- **Tailwind utilities**: Usar clases de utilidad en lugar de CSS custom cuando sea posible
- **Responsive first**: Mobile-first approach con breakpoints
- **Consistencia**: Definir paleta de colores y espaciados consistentes

### Performance
- **Lazy loading**: Cargar componentes bajo demanda con `dynamic()`
- **Optimización de imágenes**: Usar `next/image` siempre
- **Memoización**: Usar `useMemo` y `useCallback` cuando sea necesario

### Calidad de Código
- **DRY (Don't Repeat Yourself)**: Extraer código duplicado
- **KISS (Keep It Simple)**: Soluciones simples sobre complejas
- **Comentarios significativos**: Solo cuando el código no sea auto-explicativo
- **Nombres descriptivos**: Variables y funciones con nombres claros

## Ejemplo
```markdown
## 11/01/2026
1. Instalación de Next.js (`npx create-next-app@latest .`)
2. Creación de componente Header (`src/components/Header.tsx`)
3. Configuración de Tailwind CSS (`npm install -D tailwindcss`)
```
