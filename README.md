# TallerAws

1. Acceda a la consola de administración de AWS

![Cosola de administración](/images/1.png)

2. Cree una maquina virtual linux siguiendo los pasos en: https://aws.amazon.com/es/getting-started/tutorials/launch-a-virtual-machine/

![Cosola de EC2](/images/2.png)
![Seleccion de Maquina](/images/3.png)
![Seleccion de tipo de instancia](/images/4.png)
![Resumen del recurso a crear](/images/5.png)
![Creacion de credenciales ssh](/images/6.png)
![Cosola de administración instancias EC2](/images/7.png)

3. Conéctese a la máquina virtual usando ssh. Verifique que está en la máquina virtual introduciendo comandos simples como: whoami, ls, pwd.

```
ssh -i "Credentials.pem" ec2-user@ec2-18-209-23-92.compute-1.amazonaws.com
```

![Cliente ssh](/images/8.png)

4. Verifique que java está instalado. Note que el compilador de java (javac) no está instalado en la máquina virtual.

![Ejecucion de comandos java](/images/9.png)

5. Salga del ssh usando "exit".

![Cosola de salida](/images/10.png)

6. En su máquina local, usando netbeans cree un cliente que se pueda conectar a una url e imprimir la respuesta de  esa url en pantalla. Observe que el código de ejemplo recibe la url como el primer argumento en la línea de comandos.

![Captura de netbeans](/images/11.png)

7. Pruebe su cliente en la máquina local con un comando similar al siguiente:

    ```
    java URLReader https://aqueous-tor-89579.herokuapp.com
    ```
    [Repositorio del servidor en heroku](https://github.com/NicoCardenas/proyectArep)

![Pagina de consulta](/images/12.png)
![Ejecucion de la consulta](/images/13.png)

8. Suba el proyecto compilado a su máquina virtual usando sftp.

![Captura sftp](/images/14.png)
![Captura maquina virtual](/images/15.png)

9. Ejecute el cliente que instaló en su máquina virtual de AWS para conectarse a la aplicación que instaló en Heroku durante el parcial o el taller.
```
java -jar cliente-aws-1.0-SNAPSHOT.jar https://aqueous-tor-89579.herokuapp.com
```
![Captura maquina virtual](/images/16.png)
10. Borre las instancias y unidades de almacenamiento en su cuenta AWS para no generar costos.
![Captura maquina virtual](/images/17.png)