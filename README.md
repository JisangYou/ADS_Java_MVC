# ADS04 Java 

## 수업 내용
- MVC 디자인 패턴을 학습했음.

## Code Review


![MVC](http://cfile3.uf.tistory.com/image/2309334953E48F84158AD5)


- Model : 데이터의 구조

class UserBean {

private String id;

private String pw;

private int phone;

}

- Controller : Model과 View를 연결

class UserController {

public boolean registUser() {};

public boolean updateUser() {};

public boolean findUser() {};

public boolean deleteUser() {};

}

- View : 사용자에게 보여지는 화면 

class UserApplication {

public void main(String[] args) {


...어떤 Controller를 사용할 것인지 묻는 로직...


}

}



#### 출처: http://derveljunit.tistory.com/87 [IT를 보고, 듣고, 사색하고]


## 보충설명

- "책임 분담을 하자."는 의미에서 나온 개념, 결합도의 최소화를 지향

Model - 모델은 어플리케이션의 비즈니스 로직 부분을 의미함. DB에서 데이터를 가져오고, 어플리케이션에 필요한 서비스를 수행하는 부분

View - 뷰는 사용자에게 보여지는 영역, 모델에서 처리하여 보내진 정보를 보여주는 영역

Controller - 모델과 뷰 사이에서 요청의 흐름을 컨트롤하는 부분, 사용자의 요청을 받아들이면, 컨트롤러는 요청에 해당하는 비즈니스 로직을 호출하여 요청을 처리하거나 데이터를 가져오거나 처리하고 결과를 뷰로 포워딩하여 사용자가 결과를 확인하게 하는 기능을 함.


-DTO : Data Transfer Object의 약자로 데이터를 담아 움직이는 객체
사용자가 입력한 데이터나 사용자가 용청한 데이터를 담아서 흐름을 따라 움직임

-DAO : Data Access Object의 약자로 데이터를 저장하고있는 데이터베이스에 접근하는 객체입니다.
사용자가 요청한 데이터가 DTO에 담겨져서 넘어오면 DAO는 DTO에 있는 데이터들을 이용하여 DBMS에 쿼리를 날려서 데이터를 저장하거나, 가져옵니다. 

- 장점?

>> 유연하고 확장하기 쉽다

View와 Model간의 간섭을 피하고 Controller가 중간 관리를 하는 역할을 하여 간접소통을 통해 좀더 유연한 구조를 설계할 수 있는것이 MVC의 가장 큰 장점입니다.

- 단점?

>> 복잡한 구조로 보일 수있다.

>> Model과 View의 완벽한 분리가 어렵다.

기본기능 설계를 위해 클래스들이 많이 필요하기 때문에 복잡할 수 있습니다. 이것은 속도가 중요한 프로그램에서는 권장 되지 않을 수 있습니다. 또한 설계시간이 오래 걸리고 숙련된 개발자가 필요합니다. 
가장 큰 문제점은 Model과 View의 의존성이 완벽히 분리 할 수 없기 때문에 패턴이 모호해질 수 있고 변형이 올 수 있습니다.



#### 출처: http://comtk.tistory.com/22 [comtK]
#### 출처: http://blog.embian.com/49 [Embian Blog]


## TODO

- 추후에 프로그램을 짤때 MVC패턴으로 짜는 연습 필요
- 디자인패턴이란 무엇인지, 왜 이런 것을 사용하는지 찾아보기


## Retrospect

- 처음 접해서 그런지 코드가 왔다갔다 하는 듯한 느낌을 받았으나, 나중에 협업을 위해서는 필요할 것 같다라는 생각은 함.


## Output
- 생략
