# Docker-laravel

En este proyecto, seguiré usando [Docker](https://www.docker.com/), pero esta vez tratarée de poner en ejecución algo más complejo. Una aplicación [Laravel](http://laravel.com/), conectada a una base de datos [Mysql](https://www.mysql.com/) y...

<!-- para ejecutarse en el back y exponer un API. Así también conectarse con otra aplicación cuyo fin principal será exponer otro API (solo para búsquedas), una aplicación en AngularJs para consumir el API y finalmente un Website que también tenga acceso al API de búsqueda. Todas las aplicaciones deberan tener acceso a la misma base de datos. Y todos deberán funcionar en contenedores separados, pero conectados entre sí. -->

## ¿Que es Docker?

>Docker es un proyecto de código abierto que automatiza el despliegue de aplicaciones dentro de contenedores de software, proporcionando una capa adicional de abstracción y automatización de virtualización de aplicaciones en múltiples sistemas operativos.2​ Docker utiliza características de aislamiento de recursos del kernel Linux, tales como cgroups y espacios de nombres (namespaces) para permitir que "contenedores" independientes se ejecuten dentro de una sola instancia de Linux, evitando la sobrecarga de iniciar y mantener máquinas virtuales.3​. 

Cita tomada de [Wikipedia](https://es.wikipedia.org/wiki/Docker_(software))

## Screenshots / Capturas de Pantalla


## Tech-framework used / Tecnologías Usadas
- Docker  17.05.0-ce 
	- Para [Linux](https://docs.docker.com/install/linux/docker-ce/debian/)
	- Para [Windows](https://docs.docker.com/docker-for-windows/) 
	- Para [Mac](https://docs.docker.com/docker-for-mac/)
- Docker-compose 1.22.0
- Laravel [Instalación](https://laravel.com/docs/5.7/installation). En Github: [Releases](https://github.com/laravel/laravel/releases)
- Imagenes descargadas desde el repositorio de [docker](https://hub.docker.com):
	- php:7-apache
	- mysql:5.7
	- phpmyadmin/phpmyadmin

## Install / Instalación
#### OS X, Linux y Windows
*Abra un terminal y ejecute:*
```Shell
git clone http://github.com/pulidovpe/docker-laravel.git

cd docker-laravel
```
Para iniciar los contenedores:
```Shell
docker-compose up -d --build
```
Para detenerlos:
```Shell
docker-compose down
```

Una vez ejecutándose, puede abrirse un navegador y dirigirse a la dirección http://localhost:8080 para ver la aplicación web.

Para ingresar en las respectivas aplicaciones se debera contar con las credenciales correspondientes.

En caso de que se quisiera entrar a un contenedor sin usar el docker-compose, puede hacerse ejecutándolo de manera individual:
```Shell
docker run -it  mysql bash
```
Al usarse las banderas -it esto nos permitira iniciar el contenedor (basandose en la imagen elegida) en modo interactivo en el terminal por defecto. Y en este caso, en un consola.

## Tasks / Lista de Tareas
- [x] Inicialización de repositorio
- [x] Instalación de Docker
- [x] Instalación de Docker-compose
- [x] Configuración de Laravel
- [x] Pruebas en local
- [ ] Actualización de repositorio
- [ ] Despliegue en ...


## Contribute / Para contribuir
1. Has un [Fork](https://github.com/pulidovpe/docker-laravel/fork)
2. Crea tu propia rama (git checkout -b feature/fooBar)
3. Sube tus cambios (git commit -am 'Add some fooBar')
4. Actualiza tu rama (git push origin feature/fooBar)
5. Has un "Pull Request"

## Credits / Créditos
En este proyecto, me he guiado de la documentacion oficial de [Docker](https://docs.docker.com/compose/) y de diversos blogs de tecnología.

## License / Licencia
Pulido V.P.E. – @github/pulidovpe – pulidovpe.dev@gmail.com
Distributed under the MIT license. See [LICENSE](LICENSE) for more information.
