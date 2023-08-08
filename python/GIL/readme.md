# GIL (Global Interpreter Lock)
## [python 공식 홈페이지 GIL](https://wiki.python.org/moin/GlobalInterpreterLock)
### In CPython, the global interpreter lock, or GIL, is a mutex that protects access to Python objects, preventing multiple threads from executing Python bytecodes at once.
### 키워드
- 파이썬 인터프리터
  - cpython
- GC (garbage collection)
- reference counting
- Race Condition
- prevent to access multi threading that goes wrong
- 1 thread, 1 execute
- to manage memory access
### <br/>

### 참고 블로그
- https://bloofer.net/114
- https://it-eldorado.tistory.com/160
- https://ssungkang.tistory.com/entry/python-GIL-Global-interpreter-Lock%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C
### <br/><br/><br/>

## 내용 정리
### GIL 은 멀티 쓰레드로 접근 시 변수 참조를 한 번에 한 번씩만 접근할 수 있게 하게 하는 장치이다.
### GIL 이 탄생한 이유는 race condition 때문이다.
### race condition 은 여러 쓰레드가 동시 접근 시 잘못 읽거나 쓰기가 되는 경우를 말한다.
### 그래서 한 번에 한 쓰레드만 접근할 수 있게 막아두는 장치로 GIL 이 탄생하였다.
### <br/>

### 파이썬은 '객체를 저장하는 메모리'가 '몇 번 참조되었는지 저장하는 refernece count' 라는 것으로 객체가 관리된다. reference count 가 0 이 되면 객체는 GC (garbage collection) 에 의해 삭제된다.
### 만약 여러 쓰레드가 동시에 객체에 접근하게 한다면 reference count 를 잘못 조정할 수 있다. 그럼 코드가 다 끝나지도 않았는데 객체가 이미 삭제되거나 하는 상황이 벌어진다
### 이런 상황을 막기 위해 GIL 이 존재하는 것이다. 
### <br/><br/><br/>

## 한 줄로 GIL 을 요약해보자.
### GIL 은 멀티쓰레드로 파이썬 객체에 접근할 때 잘못된 순서(로직)로 읽거나 쓰기, 또는 동시 접근을 막기 위한 장치(mutex, 멀티 쓰레드로 실행 시 자원 접근에 대해 강제하기 위한 동기화 매커니즘)이다.
