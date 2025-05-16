## Install Docker Apt Repository
```
sudo apt-get update
sudo apt-get install ca-certificate curl
sudo install -m 0755 -d /etc/apt/keyrings
usdo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

## Install Docker Package
```sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin```

## Test menjalankan Docker
``` sudo docker run hello-world ```

## Install Hivemq pada Docker
```sudo docker run -p 80:8080 -p 1883:1883 hivemq/hivemq4```

## Lihat daftar container yang berada pada docker
```sudo docker container ls -a```

## Jalankan container yang mengandung Hivemq
```sudo docker container start [container id HiveMQ]```
