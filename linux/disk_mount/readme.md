### 230731
## 하드디스크 마운트 방법
### 마운트 가능한 디스크 확인
```
fdisk -l 
```
### * 아래 /dev/sdb1, /dev/sdb2 로 분리된 건 아래 명령어를 써서 n, p 옵션을 써서 분리해서 나눠진 것이다.
```
fdisk /dev/sdb
```
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/6ba3c715-689f-4d89-89f6-34aef8e4209b)
### <br/>

### 마운트
```
mkdir /data
mount /dev/sdb1 /data
```
### <br/>

### 마운트 확인
```
df -h
```
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/a4af473d-c97b-46e5-a9b8-05ed564f42c3)
### <br/><br/><br/>

