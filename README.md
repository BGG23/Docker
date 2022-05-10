# Docker

## Instalacion
1. Eliminar otras versiones

· "sudo apt-get remove docker docker-engine docker.io containerd runc"

2. Instalar mediante el repositorio

· "sudo apt-get update"
· "sudo apt-get install \ ca-certificates \ curl \ gnupg \ lsb-release"

  2.1 Agregue la clave GPG oficial de Docker

· "curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg"

  2.2 Utilice el siguiente comando para configurar el repositorio estable. Para agregar el repositorio nightly o test, agregue la palabra nightly o test (o ambas) después de la palabra estable en los comandos a continuación. Más información sobre los canales nocturnos y de prueba.

· "echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null"
 
 3. Instalar el motor Docker
    
    3.1 Actualice el índice del paquete apt e instale la última versión de Docker Engine, containerd y Docker Compose, o vaya al siguiente paso para instalar una versión específica:

· "sudo apt-get update"
· "sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin apt-cache madison docker-ce"

3.2 Para instalar una versión específica de Docker Engine, enumere las versiones disponibles en el repositorio, luego seleccione e instale:

· "apt-cache madison docker-ce"

## Resultado

4. Verifique que Docker Engine esté instalado correctamente ejecutando la imagen hello-world.

· "sudo docker run hello-world"

![image](https://user-images.githubusercontent.com/91567318/167696798-540c4b3d-babb-4e7a-b907-b6d4e6003da8.png)
