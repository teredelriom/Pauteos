🧠 Pauteo Pro v5.1

Pauteo Pro es una plataforma de estudio médico modular, diseñada para funcionar completamente en el navegador (offline-first). Combina simulacros de examen, estudio con retroalimentación inmediata y un módulo de casos clínicos con Sistema de Repetición Espaciada (SRS).
✨ Características Principales
📚 Modos de Estudio
 * Modo Estudio: Feedback inmediato. Responde y ve la justificación al instante.
 * Modo Examen: Simulación ciega. Cronómetro activado y resultados al final.
 * Modo Pauteo: Lectura rápida. Muestra la respuesta correcta marcada automáticamente para repasar conceptos.
 * Ensayo/Simulacro: Configura tiempo y cantidad de preguntas para simular un examen real.
🩺 Módulo de Casos Clínicos (SRS)
 * Sistema independiente para casos largos.
 * Algoritmo SRS (Spaced Repetition System): Clasifica casos en Difícil, Bien o Fácil para optimizar tu curva de aprendizaje.
🛠️ Herramientas de Gestión de Bancos
 * Gestión Local: Crea, guarda, fusiona y elimina bancos de preguntas directamente en el navegador.
 * Limpieza: Detección y eliminación automática de preguntas duplicadas.
 * Filtros Avanzados: Crea nuevos bancos basándote en etiquetas (tags) específicas.
 * Importación/Exportación: Soporte para archivos .json y .txt.
🤖 Inteligencia Artificial (Gemini)
 * Integración con Google Gemini API.
 * Auto-Tagging: Clasifica automáticamente tus preguntas por especialidad (Cardio, Resp, Neuro, etc.) con un solo clic.
🚀 Instalación y Uso
No requiere instalación de servidores ni bases de datos.
 * Descarga el archivo Pauteo 2.html.
 * Ábrelo en cualquier navegador web moderno (Chrome, Edge, Safari).
 * ¡Listo! La aplicación funciona localmente.
> Nota: Para una mejor experiencia en móviles, puedes usar la opción "Agregar a la pantalla de inicio" del navegador para usarla como una Web App.
> 
📥 Descargar y uso offline
Para usar Pauteo Pro sin conexión:
 * Descarga el archivo HTML y guárdalo en tu equipo (por ejemplo en Escritorio o Descargas).
 * Ábrelo con doble clic en tu navegador (no necesitas servidores).
 * Tras la primera carga, la app funciona sin internet para estudiar, guardar bancos y revisar tus estadísticas.
 * Si quieres una experiencia tipo app en móvil, usa "Agregar a pantalla de inicio" desde el navegador.

📂 Formatos de Importación
Para cargar preguntas, puedes arrastrar y soltar archivos en la zona de carga.
1. Formato JSON (Recomendado)
El formato más completo para preguntas de selección múltiple.
[
  {
    "question": "¿Cuál es el tratamiento de primera línea para...?",
    "answers": [
      "Opción A: Ibuprofeno",
      "Opción B: Paracetamol",
      "Opción C: Ketorolaco"
    ],
    "correct": 1, 
    "justification": "El paracetamol es primera línea porque...",
    "tags": ["Farmacología", "Dolor"],
    "image": "https://link-a-imagen.com/img.jpg"
  }
]

Nota: correct es el índice de la respuesta correcta (0 = A, 1 = B, etc.).
2. Formato Casos Clínicos (JSON)
Para el módulo SRS de casos.
[
  {
    "title": "Paciente con disnea súbita",
    "description": "Mujer de 35 años, antecedentes de ACO...",
    "diagnosis": "TEP. El dímero D elevado sugiere...",
    "tags": ["Respiratorio", "Urgencias"],
    "image": ""
  }
]

3. Formato TXT (Simple)
Ideal para copiar y pegar rápido. El sistema detecta automáticamente las alternativas y la respuesta si sigue este patrón:
¿Pregunta clínica aquí?
A) Alternativa 1
B) Alternativa 2
C) Alternativa 3
R: B

⚙️ Configuración de IA
Para usar el etiquetado automático:
 * Obtén tu API Key gratuita en Google AI Studio.
 * En la app, ve a Importar > Config IA.
 * Pega tu clave. (Se guarda localmente en tu navegador).
🔒 Privacidad y Datos
 * Local Storage: Todos tus bancos, progreso, notas y estadísticas se guardan en el localStorage de tu navegador.
 * Cero Nube: Nada se sube a ningún servidor externo (excepto el texto de las preguntas enviado a Gemini si usas la función de IA).
 * Advertencia: Si borras la caché del navegador, perderás tus bancos guardados. Usa el botón "Exportar JSON" regularmente para hacer copias de seguridad.
Desarrollado para facilitar el estudio médico de alto rendimiento.
