# Lesson Gamifier Agent 🎮

PWA que convierte lesson plans en juegos HTML interactivos para el aula (MEDUCA · AOA · PreK–Grade 6).

## Archivos

```
lesson-gamifier/
├── index.html          ← PWA principal
├── manifest.json       ← PWA manifest (instalable)
├── sw.js               ← Service Worker (offline)
├── vercel.json         ← Configuración Vercel
├── api/
│   └── chat.js         ← Proxy DeepSeek serverless
└── README.md
```

## Deploy en Vercel

### 1. Subir a GitHub
- Crea repo nuevo: `lesson-gamifier`
- Sube todos los archivos

### 2. Conectar a Vercel
- vercel.com → New Project → importa el repo
- En **Environment Variables** agrega:
  ```
  DEEPSEEK_API_KEY = tu_api_key_aquí
  ```
- Deploy

### 3. Configurar la PWA
- Abre la URL de Vercel en tu Android
- En la PWA, ve a ⚙️ Configuración
- Pega la URL: `https://tu-app.vercel.app/api/chat`
- Guarda

### 4. Instalar como PWA
- Chrome Android → menú ⋮ → "Agregar a pantalla de inicio"
- O toca el botón "⬇ Instalar" en el header

## Iconos (opcional)
Agrega dos imágenes PNG al repo:
- `icon-192.png` (192×192 px)
- `icon-512.png` (512×512 px)

## Uso

1. **Sube el PDF** del lesson plan o pega el texto
2. **Selecciona** grado, idioma y tipo de juego
3. **Generar** → descarga automática del HTML
4. **Abre el HTML** en cualquier PC del aula (funciona offline)

## Tipos de juego
| Tipo | Descripción |
|------|-------------|
| 🎯 Quiz / Trivia | 10 preguntas múltiple opción con puntaje |
| 🎭 Scenario Roleplay | Árbol de decisiones con consecuencias |
| ⚔️ Mini-RPG | Aventura de texto en 3 escenarios |
| 🎲 Board Game | Tablero 2 jugadores con dados |
| 📝 Word Game | Match + fill-in + unscramble |
| 🃏 Flashcard Game | Tarjetas flip con seguimiento de progreso |
