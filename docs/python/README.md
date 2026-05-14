# Installation

### 개발 도구 및 필수 패키지 설치
```bash
dnf groupinstall "Development Tools" -y
dnf install gcc openssl-devel bzip2-devel libffi-devel zlib-devel wget make -y
```

### Python 3.13 다운로드
```bash
cd /usr/src
wget https://www.python.org/ftp/python/3.13.3/Python-3.13.3.tgz
```

### 압축 해제
```bash
tar xzf Python-3.13.3.tgz
cd Python-3.13.3
```

### 빌드 및 설치
```bash
./configure --enable-optimizations
make -j$(nproc)
make altinstall
```