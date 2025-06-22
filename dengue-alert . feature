Feature: Reportar criaderos de zancudos

  Scenario: Reporte básico exitoso
    Given el usuario ha iniciado sesión
    When accede al botón “Reportar criadero” y completa la información requerida
    Then el sistema almacena el reporte y muestra un mensaje de confirmación

  Scenario: Captura de ubicación automática
    Given el usuario tiene activado el GPS
    When realiza un reporte
    Then la app añade automáticamente la ubicación al reporte

  Scenario: Visualización en historial
    Given el usuario ha enviado reportes previos
    When accede a la sección "Historial"
    Then puede ver una lista de sus reportes con fecha y estado

Feature: Recibir alertas sobre zonas con riesgo de dengue

  Scenario: Recepción de alerta automática
    Given el usuario está ubicado en una zona de riesgo
    When se detecta un criadero cercano
    Then recibe una notificación push con la alerta

  Scenario: Personalización del rango de alertas
    Given el usuario desea modificar la distancia de las alertas
    When accede a la configuración
    Then puede seleccionar entre 1 km, 3 km o 5 km

  Scenario: Visualización del detalle de alerta
    Given el usuario ha recibido una alerta
    When hace clic en ella
    Then visualiza el mapa con el punto exacto y recomendaciones

Feature: Visualizar mapa interactivo con zonas de riesgo

  Scenario: Carga automática del mapa
    Given el usuario ha iniciado sesión
    When entra a la pantalla de mapa
    Then se muestra el mapa centrado en su ubicación actual

  Scenario: Visualización de marcadores por nivel de riesgo
    Given que hay zonas con reportes
    When el usuario ve el mapa
    Then los puntos están marcados por colores (verde, naranja, rojo)

  Scenario: Acceso a detalle de reporte desde mapa
    Given que el usuario ve un punto en el mapa
    When toca el marcador
    Then se despliega información del criadero reportado

Feature: Tomar foto desde la cámara integrada

  Scenario: Acceso directo a la cámara
    Given el usuario accede al botón de reporte
    When selecciona "Tomar foto"
    Then se abre la cámara directamente

  Scenario: Adjuntar imagen al reporte
    Given el usuario tomó la foto
    When llena el reporte
    Then la imagen se adjunta automáticamente

  Scenario: Revisión previa a enviar
    Given la foto fue tomada
    When va a enviar el reporte
    Then puede revisar y confirmar la imagen

Feature: Reconocimiento de criaderos por imagen

  Scenario: Análisis automático de imagen
    Given el usuario sube una imagen
    When la app analiza la foto
    Then aparece un mensaje indicando si hay indicios de criadero

  Scenario: Confirmación de sospecha
    Given la app detecta un posible criadero
    When el usuario revisa el resultado
    Then puede confirmar o cancelar el reporte

  Scenario: Alerta por imagen no válida
    Given que la imagen no es clara
    When se analiza
    Then la app pide repetir la foto

Feature: Consultar historial de reportes realizados

  Scenario: Visualización de lista de reportes
    Given que el usuario tiene reportes registrados
    When accede a la sección de historial
    Then ve una lista con la fecha, ubicación y estado de cada reporte

  Scenario Outline: Reordenar lista del historial según filtro seleccionado
    Given que el usuario quiere buscar un reporte específico
    When selecciona el filtro por <criterio>
    Then la lista se ordena según <criterio>

    Examples:
      | criterio |
      | fecha    |
      | estado   |

  Scenario: Edición de reporte pendiente
    Given que el reporte está en estado pendiente
    When el usuario pulsa la opción “Editar”
    Then puede modificar la descripción o adjuntar una nueva imagen

Feature: Acceder a información educativa sobre el dengue

  Scenario: Acceso a contenidos sin conexión
    Given que el usuario descargó la información educativa
    When no tiene conexión a internet
    Then aún puede consultar el contenido desde la app

  Scenario: Navegación temática
    Given que quiere aprender sobre prevención
    When entra a la sección “Educación”
    Then puede elegir entre temas como síntomas, prevención y tratamiento

  Scenario: Interacción con contenido multimedia
    Given que hay videos y gráficos disponibles
    When el usuario toca un contenido
    Then se reproduce sin salir de la app

Feature: Consejos diarios de prevención del dengue

  Scenario: Envío automático diario
    Given que el usuario tiene notificaciones activadas
    When inicia el día
    Then recibe un consejo sobre prevención

  Scenario: Consultar histórico de tips
    Given que el usuario accede a “Consejos anteriores”
    When selecciona una fecha
    Then puede revisar el tip enviado ese día

  Scenario: Valorar el consejo
    Given que se muestra un consejo
    When pulsa “¿Te fue útil?”
    Then registra su opinión para mejorar futuros contenidos

Feature: Consulta de preguntas frecuentes en la app

  Scenario: Navegación por categorías
    Given que el usuario accede al menú principal
    When selecciona "FAQ"
    Then ve preguntas agrupadas por tema

  Scenario: Búsqueda por palabra clave
    Given que escribe una duda en el buscador
    When realiza la búsqueda
    Then se muestran preguntas relacionadas

  Scenario: Marcado de favoritos
    Given que visualiza una respuesta útil
    When pulsa "Guardar"
    Then esta se añade a su lista personal de favoritos

Feature: Descarga y compartición de infografías educativas

  Scenario: Descarga funcional
    Given que accede a la sección “Material educativo”
    When selecciona una imagen
    Then esta se descarga en su galería

  Scenario: Compartir desde app
    Given que el usuario visualiza una imagen
    When presiona "Compartir"
    Then se abre la opción de enviar por WhatsApp o redes

  Scenario: Guardado automático sin conexión
    Given que no tiene internet
    When pulsa "Descargar"
    Then la imagen se guarda para uso offline

Feature: Comunidad de usuarios y recomendaciones compartidas

  Scenario: Crear publicación comunitaria
    Given que el usuario está autenticado
    When accede a “Comunidad” y crea una publicación
    Then el sistema la muestra en la lista general

  Scenario: Reaccionar y comentar
    Given que otro usuario ha publicado contenido
    When selecciona "Me gusta" o "Comentar"
    Then se registra su reacción en la publicación

  Scenario: Filtrar publicaciones por tema
    Given que hay muchas entradas
    When usa el filtro (ej. “Prevención”)
    Then solo ve las publicaciones de esa categoría

Feature: Seguimiento de reportes por parte de autoridades

  Scenario: Actualización automática del estado
    Given que una autoridad ha procesado el reporte
    When cambia el estado a “Atendido”
    Then el usuario recibe una notificación

  Scenario: Visualización de comentarios de respuesta
    Given que el reporte fue revisado
    When el usuario accede al detalle
    Then puede ver un comentario como "criadero eliminado"

  Scenario: Opción de valoración
    Given que el reporte fue resuelto
    When el usuario lo revisa
    Then puede calificar la atención recibida

Feature: Calificación de contenido educativo

  Scenario: Opción de calificación visible
    Given que el usuario está visualizando un artículo
    When llega al final del contenido
    Then puede calificarlo con estrellas de 1 a 5

  Scenario: Mostrar promedio de puntuación
    Given que varios usuarios han calificado el contenido
    When un nuevo usuario lo consulta
    Then ve el promedio de utilidad

  Scenario: Ver calificaciones propias
    Given que ha calificado contenido antes
    When entra a su perfil
    Then puede ver su historial de calificaciones

Feature: Participación en foros geolocalizados por distrito

  Scenario: Acceso geolocalizado
    Given que el usuario accede al foro
    When permite el uso del GPS
    Then se une automáticamente al foro de su distrito

  Scenario: Crear una publicación local
    Given que está en su foro distrital
    When pulsa “Nueva publicación”
    Then puede compartir un mensaje visible solo para su distrito

  Scenario: Notificaciones personalizadas
    Given que hay nueva actividad en su foro
    When abre la app
    Then recibe una alerta destacando nuevos comentarios o publicaciones

Feature: Reporte y control de publicaciones falsas

  Scenario: Reportar contenido sospechoso
    Given que ve una publicación
    When pulsa “Reportar”
    Then puede seleccionar el motivo del reporte

  Scenario: Seguimiento del estado del reporte
    Given que ha enviado un reporte de contenido
    When accede a “Mis reportes”
    Then ve si fue aprobado, rechazado o está en revisión

  Scenario: Bloquear usuario malicioso
    Given que identificó una publicación falsa
    When pulsa “Bloquear autor”
    Then ese usuario ya no podrá interactuar con él

Feature: Uso offline de la app y sincronización posterior

  Scenario: Guardar reporte sin conexión
    Given que no tiene conexión a internet
    When intenta enviar un reporte
    Then la app lo guarda en la sección “pendientes”

  Scenario: Sincronización automática
    Given que vuelve a tener conexión
    When abre la app
    Then los reportes pendientes se envían automáticamente al servidor

  Scenario: Indicador de sincronización
    Given que tiene reportes no enviados
    When accede a la sección de reportes
    Then ve una alerta indicando que hay elementos sin sincronizar

Feature: Configuración de notificaciones y privacidad

  Scenario: Activar o desactivar tipos de alertas
    Given que el usuario entra a configuración
    When desactiva alertas de zona
    Then deja de recibir ese tipo de notificaciones

  Scenario: Elegir nivel de precisión de ubicación
    Given que el usuario valora su privacidad
    When selecciona “distrito” en lugar de “ubicación exacta”
    Then los reportes usan ese nivel de detalle

  Scenario: Eliminar cuenta y datos personales
    Given que el usuario desea darse de baja
    When accede a “Eliminar cuenta”
    Then se eliminan sus datos del sistema tras confirmación

Feature: Activación de modo oscuro en la app

  Scenario: Activación manual
    Given que el usuario accede a ajustes
    When activa el modo oscuro
    Then toda la interfaz cambia a fondo oscuro

  Scenario: Detección automática por sistema
    Given que el dispositivo está en modo oscuro
    When el usuario abre la app
    Then la interfaz se adapta automáticamente

  Scenario: Volver a modo claro
    Given que el usuario desea cambiar de nuevo
    When desactiva el modo oscuro
    Then la app vuelve a su diseño estándar

Feature: Cambio de idioma de la aplicación

  Scenario: Selección de idioma
    Given que accede a configuración
    When selecciona "Idioma"
    Then la app ofrece distintas opciones disponibles

  Scenario: Guardado automático de preferencia
    Given que elige un idioma
    When cierra la app
    Then este se mantiene activo en próximas sesiones

  Scenario: Confirmación del cambio
    Given que ha elegido otro idioma
    When pulsa "Aplicar cambios"
    Then se muestra un mensaje de confirmación

Feature: Estadísticas comunitarias de impacto

  Scenario: Visualización de estadísticas generales
    Given que el usuario está en el panel de estadísticas
    When selecciona su distrito
    Then ve reportes enviados, zonas atendidas y focos activos

  Scenario: Filtrado por fechas
    Given que desea comparar semanas
    When selecciona un rango de fechas
    Then el panel actualiza los datos mostrados

  Scenario: Comparativa con otros distritos
    Given que quiere conocer la situación en otras zonas
    When cambia de distrito en el panel
    Then se actualizan los indicadores correspondientes

Feature: Resumen semanal de actividad del usuario

  Scenario: Notificación automática
    Given que es domingo por la tarde
    When el usuario abre la app
    Then recibe un resumen con su actividad semanal

  Scenario: Comparativa con la semana anterior
    Given que accede al resumen
    When lo revisa
    Then puede ver si aumentó o disminuyó su participación

  Scenario: Recompensa simbólica por uso
    Given que cumplió con acciones clave
    When revisa el resumen
    Then recibe un badge o mensaje de reconocimiento

Feature: Visualización de evolución del riesgo de dengue

  Scenario: Visualización en gráfico
    Given que el usuario accede al mapa
    When selecciona su distrito
    Then ve un gráfico de evolución de reportes en el tiempo

  Scenario Outline: Filtro temporal aplicado al gráfico
    Given que el usuario quiere ver más detalle
    When elige el filtro por <periodo>
    Then el gráfico se actualiza con los datos correspondientes

    Examples:
      | periodo  |
      | semana   |
      | mes      |

  Scenario: Comparación entre distritos
    Given que el usuario selecciona un nuevo distrito
    When lo compara con el suyo
    Then ve una tabla comparativa entre ambos

Feature: Exportación de reportes en PDF

  Scenario: Generación del archivo
    Given que el usuario accede a "Mis contribuciones"
    When pulsa "Exportar"
    Then se genera un archivo PDF con sus reportes

  Scenario: Descarga inmediata
    Given que el archivo fue creado correctamente
    When el usuario lo descarga
    Then se guarda en su carpeta de documentos o descargas
