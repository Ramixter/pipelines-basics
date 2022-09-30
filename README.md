# ESTO PRETENDE SER UNA GUÍA DEL MANEJO E IMPLEMENTACIÓN DE PIPELINES CON *PRISM*

Prism es un software que ayuda a la gestión de las pipelines de los estudios de producción asignando tareas, comentarios y muchas más cosas que podemos encontrarnos en el mundo de los estudios de VFX.

**ESTA GUÍA SE IRÁ ACTUALIZANDO A MEDIDA QUE SE VAYAN CORRIGIENDO ERRORES Y SE IRÁ ACTUALIZANDO CONSTANTENTE**




# Crear un proyecto

La primera vez que iniciamos Prism nos aparece un cuadro de diálogo que nos pide que abra un proyecto existente o que cree uno nuevo.

![](/CAHAPTER-1/sources/noProject.webp)

Haremos clic en `Crear nuevo proyecto` para abrir el cuadro de diálogo `Crear proyecto`. Establezca un nombre y una ruta para su nuevo proyecto.

>Cada opción tiene una información sobre herramientas para brindarle información detallada sobre su funcionalidad.

![](/CAHAPTER-1/sources/CreateProject.webp)

Haremos clic en `Crear proyecto` para finalizar la configuración del proyecto y crear su primer proyecto.

# Crear escenas

El siguiente paso es crear archivos de escena, donde puede guardar su trabajo. Para esto, debe abrir Prism `ProjectBrowser`. Puede abrirlo haciendo clic en el icono de la bandeja Prism, escribiendo `PrismProjectBrowser` en la búsqueda del menú de inicio o abriendo una aplicación DCC (por ejemplo, Maya, Houdini). El ProjectBrowser se abre automáticamente durante el inicio del programa.

>Si es la primera vez que usa Prism, aparecerá un cuadro de diálogo y le pedirá su nombre. El nombre se utiliza para identificar qué usuario creó qué archivos de escena. ~~Más información~~.

En `ProjectBrowser` puede crear archivos de escena en la pestaña `Activos` y `Tomas`. Antes de que pueda crear un archivo de escena, debe crear un recurso/toma. Puede hacerlo a través del menú contextual (clic derecho) o haciendo doble clic en un área vacía de la lista de activos/disparos. También debe crear un paso de canalización en la lista `Pasos`. Puede hacerlo seleccionando un recurso/disparo y haciendo doble clic en la lista de pasos.

Cuando haya seleccionado un paso (en la pestaña `Tomas` debe seleccionar una categoría) puede crear un nuevo archivo de escena en la lista `Archivos`. Abra el menú contextual (haga clic con el botón derecho en la lista de archivos) y elija `Crear archivo vacío` o `Crear nueva versión a partir de la actuaL` (solo disponible si está dentro de una aplicación DCC).

![](/CAHAPTER-1/sources/sceneCreated.webp)

Si está en una aplicación DCC, el nuevo archivo de escena se abre inmediatamente. De lo contrario, puede hacer doble clic en la versión en ProjectBrowser para abrirla.

Para crear nuevas versiones de su archivo de escena, puede usar la opción `guardar` en el estante/menú Prism de su aplicación DCC o las diferentes opciones en el menú contextual del `ProjectBrowser`.

# Exportar objetos

Para intercambiar datos entre diferentes archivos de escena, los datos (u objetos) deben exportarse. Solo los datos que se exportaron desde una escena se pueden importar a otra escena. Esto es útil, por ejemplo, cuando se debe importar un activo de personaje a diferentes escenas. Además, cuando desea cambiar a otro paso de canalización y desea llevar los objetos a otro software, debe exportar los objetos.

Para exportar objetos con Prism tienes que usar la herramienta `StateManager`. Esta herramienta se puede encontrar en el estante/menú Prism de su aplicación DCC.

![](/CAHAPTER-1/sources/mayaShelf.webp)

La segunda lista en el lado izquierdo de `StateManager` es la lista de estados de exportación. Para exportar objetos, debe crear un estado de exportación. Puede hacerlo haciendo clic en el botón `Exportar` o a través del menú contextual de la lista de exportación. Cuando creó un estado de exportación, seleccione el estado para ver sus propiedades en el lado derecho del `StateManager`.

![](/CAHAPTER-1/sources/statemanager.webp)

Si la opción `Exportar toda la escena` no está seleccionada, solo se exportarán los objetos de la lista de `objetos`. Seleccione los objetos que desea exportar en la escena y presione el botón "Agregar seleccionados" para agregarlos a la lista. Puede eliminar objetos de la lista a través del menú contextual.

Es una buena práctica establecer un nombre de tarea significativo para cada exportación. Por ejemplo: `CharacterAnim` o `EnvironmentGeo`.

Ahora necesita ejecutar el estado de exportación para exportar los objetos en su lista. Para ello, publique su escena: establezca un comentario (por ejemplo, "Animación más rápida") en el campo de comentarios en la parte inferior izquierda del StateManager y presione el botón `Publicar` para ejecutar todos los estados en la lista de exportación. Aparece una ventana emergente cuando finaliza la exportación.

![](/CAHAPTER-1/sources/publishExport.webp)

Durante la publicación, su escena se guardó como una nueva versión. Ahora puede cerrar `StateManager` y su archivo de escena si lo desea.

# Importar objetos

Después de haber exportado objetos de una escena, normalmente desea importarlos a otra escena. Crea una nueva escena a través de ProjectBrowser en la que quieras importar tus objetos. En Prism, las importaciones se gestionan a través de `StateManager` como las exportaciones. Abra StateManager desde el estante/menú de Prism y haga clic en el botón `Importar` encima de la lista de importación. Se abre el cuadro de diálogo "Seleccionar tarea" y le muestra todas las exportaciones de todas las diferentes aplicaciones DCC en su proyecto actual.

![](/CAHAPTER-1/sources/selectTask.webp)

Seleccione un aSSET/SHOT y un nombre de tarea para mostrar todas las versiones de esta tarea en el lado derecho. Para importar una versión, haga doble clic en ella. Se cierra el cuadro de diálogo `Seleccionar tarea` y se crea un nuevo estado de importación en `StateManager`. La versión ahora está importada a su escena y puede cerrar el StateManager.

# Crear una explosión(playblast) de una escena

Una explosión de reproducción es una vista previa de ventana gráfica de su archivo de escena actual. Cuando trabaje en un proyecto, puede usar playblasts para obtener una vista previa de una animación o simulación sin esperar las representaciones.

La creación de playblasts se realiza a través de `StateManager`, similar a la exportación de objetos. Abra `StateManager` desde el estante/menú de Prism y cree un estado de playblast en la lista de exportación haciendo clic en el botón `Playblast` o a través del menú contextual.

![](/CAHAPTER-1/sources/playblast.webp)

Establezca un nombre de tarea para el estado de reproducción y agregue un comentario en el campo de comentarios en la parte inferior izquierda de StateManager. Presione el botón `Publicar` para ejecutar el estado de reproducción y las imágenes se guardarán en el disco.

Una vez finalizada la publicación, puede reproducir su playblast. Esto se hace a través del `ProjectBrowser`. Abra `ProjectBrowser` desde el estante/menú de Prism y seleccione el recurso/toma en el que está trabajando actualmente. En la mitad inferior del `ProjectBrowser`, puede seleccionar su tarea de playblast y una versión de esta tarea. Ahora se mostrará una pequeña vista previa en la esquina inferior derecha del `ProjectBrowser`. Haga doble clic cuando tenga instalado RV o DJV para reproducir la secuencia de imágenes. También puede abrir la carpeta en el explorador de archivos seleccionando `Abrir en el explorador` en el menú contextual de la imagen de vista previa.

![](/CAHAPTER-1/sources/pbreview.webp)

# Renderiza tu escena

Renderizar una escena en Prism es muy parecido a crear un playblast solo que con un tipo de estado diferente.

Debe abrir `StateManager` y crear un estado de `ImageRender` en la lista de exportación. Ahora solo necesita establecer un nombre de tarea y un comentario de publicación antes de poder publicar la escena. Durante la publicación, se renderizará tu escena. Para revisar su renderizado, puede abrir ProjectBrowser y navegar a la versión y reproducir la secuencia como se describe en el capítulo Crear un playblast.

# Crear un video a partir de representaciones

Después de renderizar su escena, puede crear un archivo de video a partir de la secuencia de imágenes. Alternativamente, puede llevar las imágenes a Nuke para una composición adicional, pero para esta descripción general solo convertiremos las representaciones sin procesar.

Las representaciones producidas por Prism generalmente están en formato OpenEXR, lo cual es bueno para la composición, pero no muy útil cuando desea enviarlo a personas externas, que pueden no tener un reproductor multimedia que admita secuencias .exr.

Con Prism puede crear un archivo de video a partir de sus representaciones (y también reproducciones) con solo unos pocos clics.

Abra `ProjectBrowser`, navegue hasta el recurso/toma y el renderizado/playblast que desea convertir. Luego haga clic con el botón derecho en la imagen de vista previa y elija `Convertir->mp4`.

![](/CAHAPTER-1/sources/convert.webp)

Se crea un archivo de video y en la lista de versiones aparece una nueva versión con una terminación `(mp4)`. La ruta al archivo de video se copia en su portapapeles y puede seleccionar `Abrir en el explorador` en el menú contextual de la versión para abrir la ubicación del archivo de video en el explorador de Windows.