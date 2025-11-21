# Docker
- Permite empaquetar una aplicación con todas sus dependencias en una unidad estandarizada 
- Para garantizar que aplicación corra independientemente del entorno 
# DockerFile
- Secuencia de instrucciones a ejecutar
# Imagen
Definición
	- Paquete que contiene binario, liberias, config y otras dependencias 
	- Construido a partir del Dockerfile
	- Contiene distribución del 	OS (sin el kernel)
Caracteristicas
	- Inmutable 
	- Compuesto por capa (cada capa es modificación en FS)
	- Cada capa es hasheada y cacheada (así solo se vuelve a compilar la capa que fue modificada)
	- Se usan para crear contenedores
## Docker FS Layers
- Al correr un contenedor (a partir de la imagen), se genera genera una capa adicional (de contenedor) de escritura y lectura
- Esta capa muere al eliminar el contenedor
- Si tengo varios contaniers => Capa de imagen se comparte, se crean varias capas de contenedor (apuntando a la misma capa de imagen)
![[Pasted image 20250909193113.webp]]
# Registry
- Almacena docker images (para consumir de forma distribuidas)
- (similar a repositorios git)
ejemplos:
	- Docker hub
	- AWS elastic container registry 
	- Propios (opensource)
# Docker Container 
- Instancia de docker image 
- **Efímero** (no guardar estado)
- Aislamiento
	- Namespaces -> Contenedor maneja sus propios procesos
	- cgroups
___
# Manejo de Disco
## Copy-on-Write
Cuando archivo se modifica en container
1. Busca archivo a través de las capas (de arriba a abajo)
2. **Copy-up** -> Copia, la primera copia del archivo encontrada, a la capa del container 
3. Modifica la copia recien cargada en la capa container 
Performance
	- Si archivos son grandes => aumenta mucho tamaño del container en disco

# Espacio Ocupado
- Si hay container que escribe mucho en disco (porque quiero persistir) => Crear **Data Volume** 
## Data Volume
- Es un directorio del fs
- No se elimina al eliminar el contenedor
- Tener cuidado con permisos otorgados del contenedor al fs
- Se pueden compartir entre contenedores 
- Si se escribe mucho puede tirar el host entero (no solo el contenedor)
___
# Buenas practicas 
- Deben ser efímeros 
- Reducir tamaño de imagenes lo máximo posible 
- Usar .dockerignore 
- Container con responsabilidad limitada
- Minimizar cant de capas 
- No agregar info sensible en imagen (usar data volumes)
___
# Definición 
Herramienta adicional 
Función
	- Definir y correr aplicaciones docker 
	- Automatrizar el levantado de la aplicación 
___
Kubernetes -> Orquestador 
