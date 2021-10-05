# Estrategias para construir desde código fuente

## ESTRATEGIAS POSIBLES PARA EL BUILD DE CÓDIGO FUENTE

### Source

Esto utiliza Source-to-Image para producir imágenes listas para ser ejecutadas mediante la inyección del código fuente (u otros activos) en una Imagen Builder.

### Docker

Esto utiliza docker build desde un Dockerfile y los archivos fuente asociados y crear una imagen ejecutable.

### Pipeline

Esto usa Jenkins y un flujo de trabajo definido por un Jenkinsfile (version 3) para crear un pipeline para crear una imagen ejecutable. En versión 4 se usa el framework Tekton.

### Custom

Esto utiliza su propia imagen personalizada para controlar el proceso de compilación para crear la imagen ejecutable.
