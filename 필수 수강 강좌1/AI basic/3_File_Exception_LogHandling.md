# Exception/File/Log Handling

- Exception

  1) 예상 가능한 예외
     - 발생 여부를 사전에 인지할 수 있는 예외ㄸ
     - 사용자의 잘못된 입력, 파일 호출 시 파일 없음
     - 개발자가 반드시 명시적으로 정의해야함
  2) 예상이 불가능한 예외
     - 인터프리터 과정에서 발생하는 예외, 개발자 실수...

  

  -> Exception Handling을 통해 해결!



### Except 문법

- `try ~ except` 문법

```python
# 모든 예외 혹은 남은 나머지 예외를 범위로 잡을 때
# 이때 어떤 error가 찍히는지 디테일하게 print됨
except Exception as e:
    print(e)
```

- `raise` 문법

  : 필요에 따라 강제로 Exception 발생

- `assert` 문법

  : 특정 조건에 만족하지 않을 경우 예외 발생



### File Handling

: FIle system = OS에서 파일을 저장하는 트리구조 저장체계



파일의 종류: text 파일, binary 파일

text 파일: 인간도 이해할 수 있는 형태인 문자열 형식으로 저장된 파일

bin 파일: 컴퓨터만 이해할 수 있는 형태인 이진(법)형식으로 저장된 파일



### Python File I/O

```python
f = open("<파일이름>", "접근 모드")
f.close()

# r = 읽기 모드, 대상파일이 같은 폴더에 있어야함
# w = 쓰기 모드
# a = 추가 모드


```



강의 30분대에 log 기록하는 거 확인



### Pickle

: 객체는 메모리에 저장되어 있어야함

: 이때 pickle은 객체를 따로 저장하는 방법

: python을 위한 binary  파일

: 영속을 위한 도구

```python
import pickle

f = open("list.pickle", "wb") # write binary
test = [1, 2, 3, 4, 5]
pickle.dump(test, f)
f.close()

f = open("list.pickle", "rb") # read binary
test_pickle = pickle.load(f)
print(test_pickle)
f.close()
```



### Logging

```python
import logging

logging.debug("")
logging.info("확인해")
....

```

 logging에 따라 레벨이 다름 -> 그 레벨 설정도 따로 해줌

로그 파일, 레벨 설정 필요!



설정 방법은 크게 2가지

1. configparser - 파일에
2. argparser - 실행시점에



```python
import configparser
import argparser
```

