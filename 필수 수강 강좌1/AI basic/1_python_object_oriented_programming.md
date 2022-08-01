# Python Object Oriented Programming

: python  객체지향 프로그래밍

: 만들어 놓은 코드를 재사용하기 위한 방법



 ### 객체지향 프로그래밍 개요

: OOP (Object-Oriented-Programming)

객체: 실생활의 일종의 물건 (속성(Attribute)와 행동(Action)을 가짐)

: OOP 는 설계도에 해당하는 클래스(class)와 실제 구현체인 인스턴스(instance)로 나눔



### Objects in Python 



- 예시

```python
class SoccerPlayer(object): # CamelCase # Snake_case는 함수 명에 사용
    
    # 객체 초기화 예약 함수
    def __init__(self, name, position, back_number):
        self.name = name
        self.position = position
        self.back_number = back_number
        
    def change_back_number(self, new_number):
        print("선수의 등번호를 변경합니다 : From %d to %d" % (self.back_number, new_number))
        self.back_number = new_number
        
             
```



- __ 는 특수한 예약 함수나 변수, 그리고 함수명 변경(맨글링)으로 사용 (magic method)

  예) \__str__은 선언된 객체를 print할 때 반환값 설정



### OOP Implementation

- 강의 예시 참고



### OOP Characteristics

: 실제 세상을 모델링

필요한 것들: Inheritance(상속성), Polymorphism(다형성), Visibility(가시성, 히든 클래스)



- 상속성

  : 부모 클래스로부터 속성과 Method를 물려받은 자식 클래스를 생성하는 것

  : 초기 상속은 Object로 해주기!

  : super()를 사용하여 부모 클래스의 값들, 객체 등을 가져올 수 있음

- 다형성

  : 같은 이름 메소드의 내부 로직을 다르게 작성

```python
class Animal:
    def __init(self, name):
        self.name = name
        
    def talk(self): # Abstract method, defined by convention only
        raise NotImplementedError("Subclass nust implement abstract method")
        
class Cat(Animal):
    def talk(self):
        return 'Meow!'
    
class Dog(Animal):
    def talk(self):
        return 'Woof! Woof!'
```

- 가시성

  : 객체의 정보를 볼 수 있는 레벨을 조절하는 것

  : 누구나 객체 안에 모든 변수를 볼 필요가 없음

  : = Encapsulation(캡슐화)

``` python
class Product(object):
    pass

class Inventory(object):
    def __init__(self):
        self.__items = [] # private 변수로 선언 타객체가 접근 못함
        
    def add_new_item(self, product):
        if type(product) == Product:
            self.__items.append(product)
            print("new item added")
            
        else: 
            raise ValueError("Invalid Item")
    
    @property # property decorator: 숨겨진 변수를 반환하게 해줌
    def items(self):
        return self.__items
    
    def get_number_of_items(self):
        return len(self.__items)
    
```



### Decorate

- first-class objects

  : 일급 객체

  : 변수나 데이터 구조에 할당이 가능한 객체

  : python의 함수는 일급 함수

- Innerfunction

- Closure function

-> decorator도 closure 함수로 이루어져 있음!



