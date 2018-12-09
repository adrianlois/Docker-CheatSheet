# Comandos-Docker
Guía Referencia: Comandos Docker

## ▶ Instalación Docker en Ubuntu 18.04
### ● Instalación Docker
Actualizar los repositorios existentes.
```
sudo apt update
```

Instalar paquetes previos que permitan a apt usar paquetes a través de HTTPS. 
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

Agregar la clave GPG del repositorio oficial de Docker. 
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Agregar el repositorio de Docker en las fuentes de APT. 
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```

Finalmente, se instala Docker. 
```
sudo apt install docker-ce
```

Se comprueba que el daemon de Docker está iniciado y el proceso está habilita para iniciarse en el arranque. 
```
sudo systemctl status docker
```

Si no estuviese iniciado y/o habilitado para el arranque del sistema. 
```
sudo systemctl start docker
sudo systemctl enable docker
```

### ● Ejecutar el comando Docker sin sudo o desde otro usuario
De forma predeterminada el comando Docker solo puede ser ejecutado por el usuario root o por un usuario del grupo docker. Donde “username” sería el nombre del usuario. 
```
sudo usermod -aG docker username
```

Para comprobar que el usuario forma parte del grupo docker se pude ejecutar. 
```
id -nG
```
