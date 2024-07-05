


	

MINISTERIO DE AGRICULTURA Y GANADERÍA
DIRECCIÓN GENERAL DE DESARROLLO RURAL (DGDR)
Programa de Fortalecimiento de la Resiliencia Climática de los Bosques Cafetaleros El Salvador

Cesar Romero 
Proyecto: Exportación QGIS con el plugin qgis2web (pruebas )
Descripción del Proyecto
Este proyecto tiene como objetivo guiar en la exportación de datos de QGIS a una aplicación web utilizando el plugin qgis2web. Se explicará cómo agregar datos tabulares a QGIS, reproyectar datos para que coincidan con la proyección de OpenStreetMap, editar datos, estilizar el mapa y finalmente exportar y personalizar el código Leaflet generado.
Pasos del Proyecto
    1. Añadir Datos Tabulares a QGIS
        ◦ Desde el menú superior, haga clic en Capa > Añadir capa > Añadir capa de texto delimitado.
        ◦ Seleccione el archivo wf12.geojson.gpkg ubicado en C:\Users\R\Documents\ENCAFE\SEGMENTOS MARCO CENSAL.
        ◦ Bajo Definiciones de geometría, asegúrese de que Coordenadas de punto esté seleccionado.
        ◦ Haga clic en el botón del globo a la derecha de CRS de geometría.
        ◦ En la barra de búsqueda del filtro, escriba EPSG:4326 y selecciónelo.
        ◦ Haga clic en Aceptar y luego en Añadir.
        ◦ Cierre la ventana y los puntos deberían aparecer en el área principal de trabajo, y el CSV en el panel de capas.
    2. Crear GeoJSON Proyectado
        ◦ Abra el panel de la caja de herramientas de procesamiento (Ver > Paneles > Caja de herramientas de procesamiento).
        ◦ Busque reproyectar y haga doble clic en Reproyectar capa.
        ◦ Configure los parámetros:
            ▪ Capa de entrada: el CSV.
            ▪ CRS de destino: EPSG:3857.
            ▪ Haga clic en los tres puntos junto a Reproyectado y elija Guardar en archivo.
            ▪ Guarde el archivo en el repositorio Git y asegúrese de que el tipo de archivo sea .geojson.
        ◦ Haga clic en Ejecutar y luego cierre la ventana cuando el registro muestre que la capa se reproyectó correctamente.
    3. Eliminar Capas y Agregar Capa Reproyectada
        ◦ Elimine todas las capas del panel de capas.
        ◦ Agregue la capa reproyectada arrastrándola al panel de capas.
        ◦ Asegúrese de que el CRS del proyecto sea EPSG:3857.
    4. Añadir Base de Mapa de OpenStreetMap
        ◦ Desde la barra de herramientas superior, haga clic en Web > QuickMapServices > OpenStreetMap > OSMStandard.
        ◦ Verifique que los lugares se vean correctamente sobre el mapa base de OpenStreetMap.
    5. Editar Datos
        ◦ Abra la tabla de atributos de la capa reproyectada.
        ◦ Haga clic en el ícono del lápiz para editar y elimine las columnas de latitud y longitud.
        ◦ Guarde las ediciones y cierre la tabla de atributos.
    6. Estilizar el Mapa
        ◦ Haga doble clic en la capa de puntos para abrir la ventana de propiedades de la capa.
        ◦ En la pestaña Simbología, elija Categorizado y seleccione una característica categórica para estilizar los puntos.
        ◦ Clasifique los puntos y ajuste los símbolos y colores según sea necesario.
    7. Usar qgis2web para Exportar Código Leaflet
        ◦ Desde la barra de herramientas superior, haga clic en Web > qgis2web > Crear mapa web.
        ◦ Seleccione Leaflet y actualice la vista previa si es necesario.
        ◦ En la pestaña Apariencia, configure los campos de las ventanas emergentes y otras opciones de apariencia.
        ◦ Exporte el mapa web al repositorio Git.
    8. Editar el Archivo index.html de qgis2web
        ◦ Navegue a la carpeta qgis2web en el repositorio Git y renómbrela a webapp.
        ◦ Abra el archivo index.html con un editor de texto (por ejemplo, Atom).
        ◦ Realice los siguientes cambios:
            ▪ Añada meta etiquetas para móviles en la sección <head>.
            ▪ Establezca un ancho y alto mínimo para las ventanas emergentes en la sección <style>.
            ▪ Opcionalmente, cambie los marcadores a los predeterminados de Leaflet.
            ▪ Cambie el mapa base a Google Hybrid si es necesario.
            ▪ Asegúrese de que todas las direcciones web sean seguras (https).
            ▪ Actualice la leyenda y otros elementos según sea necesario.
        ◦ Guarde los cambios y verifique que el mapa se visualice correctamente en el navegador.
    9. Subir Cambios a GitHub
        ◦ Abra GitHub Desktop y asegúrese de que el repositorio actual sea el correcto.
        ◦ Proporcione un resumen de los cambios y haga clic en Commit to master.
        ◦ Haga clic en Push origin para subir los cambios a GitHub.
    10. Integrar con un Sitio Web
    • La forma más sencilla de integrar el mapa Leaflet en un sitio web es mediante un iframe.
    • Si no tiene un sitio web, considere crear un blog con Jekyll que se integre con GitHub Pages.
    • La cuenta de GitHub utilizada es 
Conclusión
Este proyecto guía a través de la exportación y personalización de datos de QGIS a una aplicación web utilizando qgis2web, permitiendo la creación de mapas interactivos sin necesidad de conocimientos avanzados de programación

La prueba del mapa se puede acceder 
https://xcero.github.io/encafe.gihub.io/#11/13.8177/-89.1389	
	


