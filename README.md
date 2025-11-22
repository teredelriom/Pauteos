**Pauteo App (PWA)**

Aplicación de simulación de exámenes médicos ("Pauteo") diseñada como una Single Page Application (SPA) auto-contenida con capacidades de Progressive Web App (PWA).

🚀 Características Técnicas

Arquitectura Monolítica: Todo el código (HTML, CSS, JS, Lógica, Iconos SVG) reside en un único archivo index.html. No requiere bases de datos ni servidores backend.

PWA & Offline First: Utiliza un ServiceWorker integrado para cachear la aplicación, permitiendo su funcionamiento total sin conexión a internet.

Persistencia de Datos: Utiliza localStorage para guardar el progreso, los bancos de preguntas importados, las marcas de dudas y favoritos.

Responsive Design: Interfaz fluida que se adapta desde monitores de escritorio hasta teléfonos móviles, con soporte para gestos táctiles.

🛠️ Instalación y Despliegue

Para que la funcionalidad PWA (instalar en inicio) y la persistencia de datos funcionen correctamente, el archivo no debe abrirse localmente (file://), sino servirse a través de HTTPS.

Opción Recomendada: GitHub Pages

Sube el archivo index.html a un repositorio de GitHub.

Activa GitHub Pages en la configuración del repositorio.

Accede a la URL proporcionada (ej: tu-usuario.github.io/pauteo).

**Instalación en Dispositivos**

Android (Chrome): Al entrar a la web, aparecerá un aviso automático para instalar. Si no, ve al menú (3 puntos) -> "Instalar aplicación".

iOS (Safari): Presiona el botón "Compartir" (cuadrado con flecha) -> "Agregar al inicio" (Add to Home Screen).

**📂 Formatos de Importación Soportados**

La app permite importar preguntas arrastrando archivos o seleccionándolos desde el menú.

1. Formato JSON (Recomendado)

Es el formato nativo y más robusto. Permite incluir imágenes, etiquetas y justificaciones detalladas.

[
  {
    "question": "Paciente de 45 años con dolor torácico...",
    "answers": [
      "Infarto Agudo al Miocardio",
      "Pericarditis",
      "Costocondritis",
      "Reflujo Gastroesofágico"
    ],
    "correct": 0,
    "justification": "La clínica es sugerente de IAM por...",
    "tags": ["Cardiología", "Urgencias"],
    "image": "[https://link-a-imagen.com/ecg.jpg](https://link-a-imagen.com/ecg.jpg)"
  }
]


Nota: El campo correct es el índice del array answers (0 es la A, 1 es la B, etc.).

2. Formato Texto Plano (.txt)

Ideal para copiar y pegar rápidamente desde documentos viejos. El parseador interno intentará identificar la estructura.

1. ¿Cuál es la capital de Francia?
a) Londres
b) París
c) Madrid
d) Berlín
Respuesta: b
Justificación: París es la capital histórica...

2. Siguiente pregunta...


⚙️ Funcionalidades Clave del Código

saveProgress(): Guarda el estado actual (índice de pregunta, respuestas marcadas) en el almacenamiento local cada vez que el usuario interactúa.

removeDuplicates(): Implementa un algoritmo de similitud de Jaccard para detectar preguntas con texto muy similar (umbral 0.85) y eliminarlas.

filtrarPorEtiqueta(): Crea sub-arrays de preguntas basados en las etiquetas (tags) detectadas automáticamente o definidas en el JSON.

handleInstallTrigger(): Gestiona el evento beforeinstallprompt para ofrecer la instalación nativa en Android y mostrar instrucciones personalizadas en iOS.

**🎨 Personalización**

El diseño utiliza variables CSS (:root) para facilitar el cambio de temas.

Color Principal: Modificar --primary y --primary-soft.

Tema Oscuro: La app detecta la preferencia del sistema o permite el cambio manual, ajustando las variables --bg y --card.

Desarrollado para facilitar el estudio médico autónomo.
