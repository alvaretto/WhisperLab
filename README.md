# WhisperLab
Transcendiendo Idiomas: Transcriptor y Traductor de Vídeos Automatizado

Transcriptor y Traductor de Vídeos
==================================

Este repositorio contiene un script que utiliza la API (Gratuita) de OpenAI Whisper para transcribir archivos de vídeo, y luego traduce los subtítulos generados al español utilizando la biblioteca Googletrans. Los subtítulos se guardan en formato VTT.

Requisitos
----------

*   Python 3.6 o superior
*   Google Colab

Instalación
-----------

1.  Clone este repositorio en su entorno local o en Google Colab.
2.  Asegúrese de que ha instalado todos los paquetes y bibliotecas necesarias ejecutando las siguientes líneas de código:

python

```python
!pip install googletrans==4.0.0-rc1
!pip install git+https://github.com/openai/whisper.git
!pip install ffmpeg
```

Uso
---

1.  Ejecute el script en bloques de código en Google Colab.
2.  Los archivos de vídeo en formato .mp4 deben ser almacenados en una carpeta llamada "videos" en su Google Drive.
3.  Después de ejecutar el script, los subtítulos en inglés serán guardados en una carpeta llamada "SubtítulosEN" y los subtítulos traducidos al español serán guardados en una carpeta llamada "SubtítulosES", ambas carpetas estarán ubicadas en su Google Drive.

Información adicional
--------------

(Youtube)[https://www.youtube.com/watch?v=jgSk01fWkjg]


Contribuciones
--------------

Las contribuciones son bienvenidas. Por favor, siéntase libre de enviar un Pull Request o abrir un Issue si encuentra algún problema o tiene alguna sugerencia de mejora.

Licencia
--------

Este proyecto está licenciado bajo la Licencia MIT - vea el archivo [LICENSE](LICENSE) para más detalles.

