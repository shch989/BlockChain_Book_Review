# 제 1장 처음 접하는 블록체인
## 비트코인 개발환경 세팅
### 비트코인 클라이언트 설치
```
wget https://bitcoincore.org/bin/bitcoin-core-0.15.2/bitcoin-0.15.2-x86_64-linux-gnu.tar.gz
```
```
tar xzf bitcoin-0.15.2-x86_64-linux-gnu.tar.gz*
```
```
sudo install -m 0755 -o root -g root -t /usr/local/bin bitcoin-0.15.2/bin/*
```

### 비트코인 클라이언트 설치(최신버전)
```
sudo apt-add-repository ppa:bitcoin/bitcoin
```
```
sudo apt-get update
```
```
sudo apt-get install bitcoin-qt bitcoind
```

### 일렉트럼(경량 지갑) 설치
```
wget https://download.electrum.org/3.3.4/Electrum-3.3.4.tar.gz
```
```
sudo apt-get install python3-setuptools python3-pyqt5 python3-pip
```
```
sudo pip3 install Electrum-3.3.4.tar.gz
```

## 비트코인 코어 실행
### bitcoin.conf 파일 생성
```
mkdir ~/.bitcoin
```
```
nano ~/.bitcoin/bitcoin.conf
```
### bitcoin.conf 파일에 아래의 내용 작성
```
rpcuser=user_name           #JSON-RPC 연결에 사용할 사용자 이름
rpcpassword=your_password   #JSON-RPC 연결에 사용할 패스워드
server=1                    #JSON-RPC 명령 실행을 위한 서버 활성화
testnet=1                   #실제 비트코인 네트워크 대신 시험용 네트워크에서 실행
prune=550                   #가지치기 모드 활성화
```
### 비트코인 코어의 GUI 버전 실행
```
bitcoin-qt
```