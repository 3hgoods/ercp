
### install
1. Miniforge3 설치
 - https://openhsi.github.io/openhsi/tutorial_installing_linux.html#Installing-Pyenv
 -  https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Windows-x86_64.exe
 -  환경번수 체크하여 포함
  - ref https://gist.github.com/elejke/3437be39478c66a3efac26700cb14334
  - https://github.com/conda-forge/miniforge
  - https://yiworkdisk.netlify.app/ko/linux/install_anaconda_ubuntu.html
  - https://github.com/mamba-org/mamba
  - https://gist.github.com/elejke/3437be39478c66a3efac26700cb14334

2. 기본 정보 확인
h1@h1:~$ source .bashrc
(base) C:\Users\h7>conda -V
conda 4.14.0

(base) C:\Users\h7>conda env list
# conda environments:
#
base                  *  C:\ProgramData\miniforge3
                         C:\Users\h7\anaconda3
                         C:\Users\h7\anaconda3\envs\airsim
                         

3. prompt commander 실행
 - conda create --name <가상환경명> <패키지명>
 - ex) conda create --name ml pandas numpy matplotlib scikit-learn
 - conda create --name '이름' python='버전'
 - ex) conda create --name wgpydev python=3.7
 - conda create -n '이름' python='버전' <패키지명>
 - ex) conda create -n  makehsi python=3.8 openhsi
 - conda activate makehsi
 - conda install -y -c fastai nbdev
 - conda install -c conda-forge jupyterlab
 - conda install git
 - git clone https://github.com/openhsi/openhsi.git
 - cd openhsi
 - jupyter lab



3. import ctypes
 ``` 
 conda install -c esri pywin32-ctypes

import os
import platform
from ctypes import *

dbr = None
dbr = CDLL(os.path.join(os.path.abspath('.'), 'Crevis.VirtualFG40Library.dll'))

```

