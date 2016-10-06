# docker-puppet3server
Proyecto vinculado de Docker Hub para servidor Puppet 3

## Puppet 3 Server

Esta imagen contiene el servidor de Puppet 3 en una plantilla de Debian Jessie. Para establecer correctamente tanto los certificados del servicio de Puppet como la configuración de los certificados en Apache es necesario establecer en el **docker run** la opción de **--hostname** y agregar una variable de entorno llamada **FQDN**, quedando una ejecución como en el siguiente ejemplo:

```bash
docker run -dt --hostname puppet.example -e FQDN=puppet.example ignoto/puppet3server
```
