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