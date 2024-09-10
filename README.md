![](/public/images/index.png)
## E³Retail

> Un sitio web de lista de productos de comercio electrónico que demuestra la aplicación de Elasticsearch en las compras minoristas y en línea.

### Capturas de pantalla de la aplicación

#### Página de inicio

![Captura de pantalla de la página de inicio](/public/images/e3-retail_home.png)

#### Página de filtro de productos

![Captura de pantalla de la página de filtro de productos](/public/images/e3-retail_search.png)

### Características

- Adaptable a la web y a dispositivos móviles.
- Desarrollado con la filosofía de [Mejora progresiva](https://en.wikipedia.org/wiki/Progressive_enhancement).

#### Características de búsqueda

- Busque un producto escribiendo en el campo de búsqueda.
- Busque dentro de una categoría.
- Busque en varias categorías.
- Filtre por marca, precio y calificaciones.
- Ordenar por relevancia, calificaciones o precio.
- Paginar los resultados de búsqueda.
- Sugerencias de autocompletado de entradas de búsqueda (requiere que JavaScript esté habilitado).

### Requisitos

- Una computadora portátil o de escritorio.
- Navegador Chrome.
- Conectividad a Internet.

### Instrucciones para instalar

1. Requiere **[Elasticsearch](https://aws.amazon.com/opensearch-service/)**
2. Inicializar las variables del entorno. Si está ejecutando la aplicación localmente, cree un archivo `.env`:

```shell
NODE_ENV=development
ELASTICSEARCH_HOST=your-elasticsearch-domain
ELASTICSEARCH_PORT=443
ELASTICSEARCH_USER=your-elasticsearch-master-user
ELASTICSEARCH_PASSWORD=your-elasticsearch-master-password
ELASTICSEARCH_INDEX=index-to-search-on
```

3. Instale [Node.js](https://nodejs.org/)
4. Clone o bifurque este repositorio
5. Ejecute `npm install` en la raíz de su proyecto
6. Ejecute `npm start` para iniciar el servidor de aplicaciones

### Comandos comunes

#### Creación de un índice

`npm run create-index your-index-name`

#### Carga masiva de datos

Sintaxis para cargar datos en Formato `.ndjson`:

```
curl -XPOST -u 'username:password' 'your-elasticsearch-url/_bulk' --data-binary @datasets/flipkart-products-bulk.ndjson -H 'Content-Type: application/json'
```

### Problemas conocidos

- Es posible que las imágenes no se carguen si se han eliminado en la fuente.