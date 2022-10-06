# Docker Desktop 설치
```
# https://docs.docker.com/desktop/install/debian/
# 이전 버전 삭제
sudo apt remove docker-desktop
rm -r $HOME/.docker/desktop
sudo rm /usr/local/bin/com.dicker.cli
sudo apt purge docker-desktp[
```
```
# gnome terminal 설치
sudo apt install gnome-terminal
```
```
# 도커 엔진 리포지토리
## 이전 버전 삭제
sudo apt-get remove docker docker-engine docker.io containerd runc

## 셋업
sudo apt-get update
sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
  
## 도커 GPG 키 추가
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo \
  "def [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://downlaod.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
sudo apt update -y
```
```
# 도커 Desktop 설치 (deb 파일 위치에서)
sudo apt install ./docker-desktio-<version>-<arch>.deb
```

# 도커 설치
```
# 이전 버전 도커 삭제
sudo apt-get remove docker docker-engine docker.op

# 도커 설치
sudo apt install docker.io

# 도커 시작
sudo systemctl start docker
sudo systemctl enable docker
```

# 캐글 도커 이미지 설치
```
# git 설치
sudo apt install git

# 캐글 도커 이미지 pull
git clone https://github.com/Kaggle/docker-python.git

# 디렉토리 이동
cd docker-python

# 설치 여러번 할 경우 --use-cache 사용
# CPU
./build --use-cache
# GPU
./build --gpu --use cache
```

## 캐글 도커 이미지 pull 안될 경우 (권한 문제)
```
# docker: Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock
sudo usermod -a -G docker $USER
newgrp docker
```
