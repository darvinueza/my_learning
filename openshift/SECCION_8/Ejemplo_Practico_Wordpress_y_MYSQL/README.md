# Ejemplo Práctico: Wordpress y MYSQL

## COMANDOS

- Crear un proyecto

        # oc new-project wordpress

- Recordemos activar los permisos necesarios para poder desplegar imágenes que trabajen como ROOT o que activen determinados puertos

        # oc adm policy add-scc-to-user anyuid -z default

- Crear una nueva aplicación con Mysql

        # oc new-app mysql:5.7 --name=mysql1 -e MYSQL_ROOT_PASSWORD=secret -e MYSQL_USER=usu1 -e MYSQL_PASSWORD=secret MYSQL_DATABASE=wordpress

- Crear una nueva aplicación de tipo Wordpress y enlazarla con la anterior

        # oc new-app wordpress --name=wordpress1 -e WORDPRESS_DB_HOST=mysql1 -e WORDPRESS_DB_USER=usu1 -e WORDPRESS_DB_PASSWORD=secret -e WORDPRESS_DB_NAME=wordpress

- Crear un route para poder acceder a Wordpress

        # oc expose svc wordpress1

- Comprobamos que tenemos todos los componentes

        # oc get deployment
        # oc get pod oc get svc
        # oc get is
        # oc get route
