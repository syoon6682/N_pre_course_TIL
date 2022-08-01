# Python data handling



## CSV

: Comma Separate Values

: 필드를 쉼표(,)로 구분한 텍스트 파일

: 엑셀 양식의 데이터를 프로그램에 상관없이 쓰기 위한 데이터 형식

: Text 파일 형태로 데이터 처리 예제



### csv 객체 활용

```python
import csv
reader = csv.reader(f, delimiter=',', quotechar='"', quoting = csv.QUOTE_ALL)
```

window는 encoding을 cp949

다른 경우 utf-8



## Web

: World Wide Web

: HTTP 프로토콜 & HTML 형식을 활용한 데이터 표시



### HTML

: 웹 상의 정보를 구조적으로 표현하기 위한 언어



정규식 문법 (regular expression)

: 교재 확인 및 실제로 사이트에서 실습해보기

```python
import re # re 모듈이 정규식임

# 정규식을 활용하여 조건을 설정하고 re.findall() 안에 조건 적용 후 찾기
```



## XML

: 데이터의 구조와 의미를 설명하는 TAG(MarkUp)을 사용하여 표시하는 언어

: 주로 beatifulsoup을 활용하여 파싱



``` python
# 모듈 호출
from bs4 import BeautifulSoup

# 객체 생성
soup = BeautifulSoup("열고 싶은 파일", "lxml") # lxml은 parser 종류

# Tag 찾는 함수 find_all 생성
soup.find_all("author")
```



XML을 parser로 나눠서 CSV로 하는 실습 한번 살펴보기



## JSON

: JavaScript Object Notation

: 간결성..!, python의 DIct Type과 유사

: API는 대부분 정보 교환 시 JSON 활용



### 처리

: JSON 파일의 구조 확인 -> 읽어온 후 -> DIct Type처럼 처리



