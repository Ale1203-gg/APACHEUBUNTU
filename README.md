# APACHE UBUNTU
## Pasos para Instalar Apache en Ubuntu en Oracle Cloud
1. Conectarse al Servidor Ubuntu en Oracle Cloud
Inicia sesión en Oracle Cloud Console:

Ve a Oracle Cloud y accede a tu cuenta.

Dirígete a Compute Instances y selecciona tu instancia de Ubuntu.

Conéctate al servidor mediante SSH:

En la terminal, usa el siguiente comando para conectarte (reemplaza your_public_ip con la IP pública de tu servidor):

``` ssh -i ~/.ssh/your-key.pem ubuntu@your_public_ip```

Si es la primera vez, confirma la conexión escribiendo yes.

2. Actualizar el Sistema
Antes de instalar Apache, es recomendable actualizar los paquetes:

``` sudo apt update && sudo apt upgrade -y```
3. Instalar Apache
Ejecuta el siguiente comando para instalar Apache2 en Ubuntu:

``` sudo apt install apache2 -y```
Una vez instalado, verifica el estado del servicio Apache con:

```sudo systemctl status apache2```
Si aparece "active (running)", significa que Apache se está ejecutando correctamente.

5. Verificar que Apache Funciona
Abre tu navegador web y accede a la IP pública de tu servidor:

http://your_public_ip


Deberías ver la página de inicio de Apache con el mensaje "It works!".


6. Configurar Apache (Opcional)
   
Si deseas configurar un sitio web personalizado, puedes modificar el archivo principal de Apache:

```sudo nano /var/www/html/index.html```


Escribe el contenido HTML que deseas y guarda los cambios (CTRL + X, luego Y y Enter).
