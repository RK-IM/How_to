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
# Matplotlib 한글
### bash에서
```
# ubuntu에 나눔 폰트 설치
sudo apt-get install fonts-nanum

# 캐시 삭제
sudo fc-cache -fv

# 설치한 폰트 프로젝트 내 matplotlib 폰트 경로로 복사
# 아나콘다 사용할 경우
cp /usr/share/fonts/truetype/nanum/Nanum* /home/{user_id}/.conda/envs/{env_name}/lib/python{version}/site-packages/matplotlib/mpl-data/fonts/ttf

# matplotlib 폰트 업데이트를 위해 캐시 삭제
rm -rf ~/.cache/matplotlib/*
```
### matplotlib 폰트 변경
```
# 사용 가능한 나눔 폰트 확인
import matplotlib.font_manager
font_list = matplotlib.font_manager.findSystemFonts(fontpaths=None, fontext='ttf')
[matplotlib.font_manager.FontProperties(fname=font).get_name() for font in font_list if 'Nanum' in font]

# 폰트 변경
import matplotlib.pyplot as plt
plt.rc('font', family='NanumGothicCoding')

# 마이너스 깨질 경우
import matplotlib as mpl
mpl.rcParams['axes.unicode_minus'] = False
```
### 그래도 안된다면!
위 가상환경 내 mpl-data 경로 중 matplotlibrc 파일 수정
```
gedit /path/to/matplotlib/matplotlibrc
```
font.family: NanumGothic # 변경하려는 폰트로  
편집 후 재시작

# Tensorflow 
## `libdevice not found at ./libdevice.10.bc` 에러 발생
설치된 쿠다에 libdevice.10.bc가 설치되어있는지 확인 후  
환경변수에 XLA_FLAGS 추가
```
export XLA_FLAGS=--xla_gpu_cuda_data_dir=/path/to/cuda
```

