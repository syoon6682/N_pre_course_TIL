# Module and Project

: project > module > 객체



### 모듈과 패키지

: 모듈은 패키지 안에 들어있음



### Module

: python의 module == py 파일

 

- Module namespace example

  ```python
  # Ailas 
  import fah_converter as fah
  
  # 특정 함수 또는 클래스만 호출
  from fah_converter import convert_c_to_f
  
  # 모듈에서 모든 함수 또는 클래스를 호출하기
  from fah_converter import *
  
  ```

- built-in-module

  : python에서 기본적으로 제공하는 모듈



### package 만들기

각 package 안에는 \__init__.py 파일이 꼭 있어야함!  (있어야  package로 간주, 그러나 현 버전은 없어도 되긴 함)



### 상대참조 vs 절대참조

: from import 시 경로 설정의 차이



### 가상환경

: 프로젝트 진행 시 필요한 패키지만 설치하는 환경 

: conda를 활용한 가상환경 설정! (windows에서는 conda! 근데 mac에서도 잘씀)

