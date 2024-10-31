# Transcriptor y Traductor de Videos con Whisper y Claude

Este proyecto es una herramienta automatizada para transcribir videos y traducir sus subtítulos del inglés al español, especialmente optimizada para contenido relacionado con Inteligencia Artificial, Python y ChatBots. Utiliza OpenAI Whisper para la transcripción y Claude de Anthropic para la traducción.

## Características Principales

- Transcripción automática de videos usando Whisper
- Traducción especializada de inglés a español usando Claude
- Procesamiento por lotes de videos en Google Drive
- Generación de archivos de subtítulos en formato .srt
- Manejo automático de errores y reintentos
- Optimización de subtítulos para mejor legibilidad

## Requisitos Previos

- Google Colab (para ejecución en la nube)
- Cuenta de Google Drive
- Clave API de Anthropic (Claude)
- Python 3.x
- Bibliotecas requeridas:
  - openai-whisper
  - ffmpeg-python
  - anthropic

## Instalación

1. Abra el notebook en Google Colab
2. Monte su Google Drive
3. Instale las dependencias necesarias:
```python
!pip install git+https://github.com/openai/whisper.git
!pip install ffmpeg-python
!pip install anthropic
```

## Estructura del Proyecto

```
Videos/
├── video1.mp4
├── video1.srt        # Subtítulos originales en inglés
├── video1.es.srt     # Subtítulos traducidos al español
└── ...
```

## Uso

1. Coloque sus videos en la carpeta 'Videos' de Google Drive
2. Ejecute el notebook en Google Colab
3. Ingrese su clave API de Anthropic cuando se solicite
4. El sistema procesará automáticamente todos los videos:
   - Generará transcripciones (.srt)
   - Creará traducciones (.es.srt)

## Características Técnicas

- Manejo de sesión persistente en Colab
- División inteligente de subtítulos para traducción por lotes
- Preservación de términos técnicos durante la traducción
- Eliminación automática de muletillas
- Sistema de reintentos con espera exponencial
- Logging completo de operaciones

## Configuración Personalizable

```python
MAX_SUBTITLE_LENGTH = 48            # Longitud máxima de línea de subtítulo
MAX_SUBTITLES_PER_PART = 10        # Subtítulos por lote de traducción
RETRY_DELAY_BASE = 2               # Tiempo base para reintentos
MAX_RETRIES = 5                    # Número máximo de reintentos
PAUSE_BETWEEN_TRANSLATIONS = 3      # Pausa entre traducciones
PAUSE_BETWEEN_VIDEOS = 15          # Pausa entre videos
```

## Limitaciones

- Requiere conexión a internet estable
- El procesamiento puede ser lento para videos largos
- Depende de la disponibilidad de las APIs de Whisper y Claude
- Los videos deben estar en formato MP4

## Notas de Uso

- El sistema mantiene la estructura exacta de los subtítulos
- Preserva términos técnicos sin traducir
- Mejora la redacción para mayor claridad
- Elimina muletillas y sonidos de relleno
- Mantiene registro de errores en archivo de log

## Recomendaciones

1. Organice sus videos en carpetas para mejor gestión
2. Verifique la calidad del audio para mejores transcripciones
3. Monitoree el proceso para detectar posibles errores
4. Revise los archivos de log para diagnóstico
5. Mantenga una copia de seguridad de los videos originales
