### 240103
## subprocess test
### subprocess 모듈은 서브 프로세스가 끝났는지 안 끝났는지 체크해준다.
```
import subprocess

p1 = subprocess.run(args = ["ls"], shell = True, capture_output = True)
print(p1)
print(p1.stdout.decode('utf-8'))
```
#### ![image](https://github.com/Shin-jongwhan/TIL/assets/62974484/1c41d043-cd27-4cea-8b23-d46a991539f3)
