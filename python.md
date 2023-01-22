# Pororo 설치

\#\#\#\#\# 해당 가상환경으로 이동 후 \#\#\#\#\#
```
# konlpy 설치
pip install konlpy 
```
```
# pororo 설치
pip install git+https://github.com/kakaobrain/pororo.git
```

위에걸로 설치할 경우 numpy>=1.24가 설치된다. 이 버전에서는 np.float가 사라지므로 pororo 임포트시 에러가 난다.  
1.20.3으로 다운그레이드 시켜준다.
```
pip uninstall numpy
pip install numpy==1.20.3
```
```
# mecab-ko 설치
pip install python-mecab-ko
```

자바가 설치되어있지 않거나 환경변수로 설정되어있지 않다면
```
# 설치
sudo apt install default-jdk
```
