### 230824
## SGE (Sun Grid Engine / Oracle Grid Engine)
### <br/><br/><br/>

## qsub 
### 메뉴얼 참고
### https://gridscheduler.sourceforge.net/htmlman/htmlman1/qsub.html
### <br/>

### qsub 제출 예시
```
qsub -q wgs.q -V -e /TBI/People/tbi/jhshin/script/test/qsub/log -o /TBI/People/tbi/jhshin/script/test/qsub/log -pe smp 10 -S /bin/bash /TBI/People/tbi/jhshin/script/test/qsub/test.sh
```
### <br/>

### 만약 어느 queue 에 특정한 host (서버)만 사용하고 싶다면 -q 옵션에 명시한다.
```
# host 를 명시하고 싶을 때
-q "wgs.q@host1|host2"

# 특정 string 을 포함하는 hostname 들을 가져오고 싶을 때(wildcard)
-q "wgs.q@host*"
```


-------------------------------------------
