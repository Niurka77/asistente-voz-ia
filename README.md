# 🎙️ Asistente de Voz IA

Asistente de voz inteligente con **Flask** que transcribe audio a texto mediante **Whisper (Groq)**, genera resúmenes con **Hugging Face** y extrae tareas pendientes automáticamente. Pensado para productividad: graba, habla y el sistema ordena tu día.

## ✨ Cómo funciona

1. 🎤 El usuario graba un audio desde el frontend
2. 🔉 **Groq (whisper-large-v3)** transcribe el audio al español
3. 🧠 **Hugging Face** genera un resumen del texto
4. ✅ Extracción simple de tareas pendientes por palabras clave
5. 📦 Respuesta JSON lista para mostrar al usuario

## 🚀 Instalación

```bash
pip install -r requirements.txt
```

Configura tus claves en un archivo `.env`:

```
GROQ_API_KEY=tu_clave
HF_API_KEY=tu_clave
```

## 🧪 Ejecutar

```bash
cd backend
python app.py
```

El servidor queda en `http://localhost:5000` con el endpoint `POST /transcribe` (multipart con campo `audio`).

También hay scripts de prueba para validar las claves:

```bash
python test_groq.py   # Prueba la clave de Groq
python test_hf.py     # Prueba la clave de Hugging Face
```

## 📁 Estructura

```
├── backend/
│   └── app.py            # API Flask (transcripción, resumen, tareas)
├── frontend/
│   └── index.html        # Interfaz de grabación por voz
├── test_groq.py          # Validación de API Groq
├── test_hf.py            # Validación de API Hugging Face
├── requirements.txt      # Dependencias
└── README.md
```

## 🛠️ Stack

`Python` · `Flask` · `Groq (Whisper)` · `Hugging Face Transformers` · `SpeechRecognition` · `pyttsx3`

---

Desarrollado por **Niurka Guevara** · Ingeniería de Software con IA.