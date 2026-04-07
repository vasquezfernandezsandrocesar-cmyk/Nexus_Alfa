# 🤖 Nexus Prime v9.0 — Asistente Académico

Asistente académico universitario con interfaz web moderna. Usa Groq, Gemini y OpenRouter como motores de IA.

## 🚀 Deploy en Render

### 1. Sube el código a GitHub
- Crea un repo nuevo en GitHub
- Sube estos archivos: `nexus_prime.py`, `requirements.txt`

### 2. Crea el servicio en Render
- Ve a render.com → New → Web Service
- Conecta tu repo de GitHub
- Configura así:
  - Runtime: Python 3
  - Build Command: pip install -r requirements.txt
  - Start Command: python nexus_prime.py

### 3. Agrega las variables de entorno
En Render → tu servicio → Environment → agrega:

  GROQ_API_KEY      → tu clave de console.groq.com
  GEMINI_API_KEY    → tu clave de aistudio.google.com
  OPENROUTER_API_KEY→ tu clave de openrouter.ai
  PORT              → 8080

Con solo una clave ya funciona. Las demás son respaldo automático.

### 4. Deploy
Haz clic en Deploy y espera ~2 minutos. Render te dará una URL tipo https://nexus-prime.onrender.com

---

## Ejecutar en local

  pip install -r requirements.txt
  set GROQ_API_KEY=tu_clave        (Windows)
  export GROQ_API_KEY=tu_clave     (Linux/Mac)
  python nexus_prime.py

Luego abre: http://localhost:8080

---

## Motores de IA
- Groq (llama-3.3-70b)   → Principal, más rápido
- Gemini (2.0 flash)     → Respaldo
- OpenRouter (mistral-7b) → Respaldo extra

## Modos
Chat Libre, Académico, Código, Creativo, Tutor, Clínico

## Comandos
/informe, /ensayo, /resumen, /apa, /tesis, /flashcards, /plan, /noticias, /imagen y más.
