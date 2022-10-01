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
