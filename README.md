# recuhttp
## EJ1
1.He creado primero las carpetas de web1 y web2 en la ubi /var/www/
Dentro de esas carpetas he creados sus index ya en su carpeta ej: /var/www/web1/index.html

2. Después he copiado de la carpeta /etc/nging/sites-available/default ese archivo por defecto y he creado uno tanto para web1 como web2 llamados web1.conf y web2.conf en los que he comentado todo el contendio y solo he dejado las líneas necesarias como el puerto , el nombre del servidor , donde está ubicada la carpeta root y el nombre del archivo index.

3.Posteriormente después de hacerlo , activé digamos los sitios que habíamos creado en  /etc/nging/sites-available/ y con el comando se activó y pasó a ubicarse en /etc/nging/sites-enable , con el comando ln -s /etc/nging/sites-available/web1.conf /etc/nging/sites-enable/

4.Tras los cambios lo siguiente era hacer un reload del servicio y comprobar en un cliente en el que hemos tenido que editar el archivo /etc/hosts/ y especificar la ip en la que se encuentra esa dirección http,y en el buscador deberíamos de poner su url como podría ser http://web1.org , también comprobaremos el de la web2

5.Una vez hecho y comprobado hemos pasadado a crear la web de mantenimiento en el que hemos hecho los dos primeros pasos que hemos hecho para las otras webs solo que teniendo en cuenta que su carpeta sería /var/www/mantenimiento, y su conf web1.mantenimiento.conf . Su url es http://web1.mantenimiento.org. En su index pusimos la información que queríamos que nos mostrara como es "En mantenimiento".

Una vez accedido y comprobado que también podemos acceder pasamos a configurar redirecciones en el .conf de nuestra página de mantenimiento.

## EJ2 

Páginas de error personalizadas 
creamos en /var/www/ una carpeta llamada errores con unos index en el que escribiremos este es el error 403 o 404 que son los dos que tenemos que crear . Una vez creados deberemos de ir al sitio de configuración como puede ser /etc/nginx/sites-available/web1.conf y ahí asociar el error a la página.

Tener los logs separados por sitios sirve para ver de manera más clara e individual los eventos que están ocurriendo de algo en concreto dentro de nginx, puede ayudar ya que localizariamos más rápidamente donde puede haber un problema ya que los tenemos ubicados en distintos sitios . 


