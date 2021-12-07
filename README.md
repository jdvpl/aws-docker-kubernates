# aws-docker-kubernates

#### desintalar el que ya este
* `sudo apt-get remove docker docker-engine docker.io containerd runc`

### instalar paquetes
* `apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release`
### anadir clave
* ` curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg`

# repo estable
* `echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

### instalar docker
* `sudo apt-get install docker-ce docker-ce-cli containerd.io`

### Activar docker

* `usermod -a -G docker msi` <== nombre_usuario`

---
### instalar kubectl 
##### Siver para gestionar y desplegar aplicaciones en kubernates

* `https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/`

### Descargar paquete
* `curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"`

### dar permisos a la carpeta kubectl
* `chmod +x kubectl`

### ejecutar
* `./kubectl`

### Mover directorio

* `sudo mv kubectl /usr/local/bin/`
---

### Instalar minikube
* local kubernates
* `https://minikube.sigs.k8s.io/docs/start/`
* `curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64` <== descargar el binario

### mover la carpeta
* `sudo mv minikube-linux-amd64  /usr/local/bin/`

### dar permisos
* `chmod +x minikube-linux-amd64` 

### ejecutar
* `./minikube-linux-amd64`

### renombar ejecutador
* `sudo mv minikube-linux-amd64 minikube`

### instalar virtualbox

* `sudo apt install virtualbox`

---

### Instalar docker compose
* `https://docs.docker.com/compose/install/`
* ` sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose` <= binario

### dar permisos
* `sudo chmod +x /usr/local/bin/docker-compose`

### Instalacion de aws clie

* `https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html`

### descargar binario
* `curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"`

### Descomprimir
* `unzip awscliv2.zip`

### ejecutar
* `sudo ./aws/install`
