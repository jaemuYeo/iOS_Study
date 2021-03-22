## Step1

- 설계도 그리기 UML활용
  <img width="835" alt="스크린샷 2021-03-13 오후 1 20 31" src="https://user-images.githubusercontent.com/70311145/111018890-2c6a5f80-83ff-11eb-94ec-e1de4dccfcc8.png">
  <img width="828" alt="스크린샷 2021-03-13 오후 1 20 37" src="https://user-images.githubusercontent.com/70311145/111018892-2f655000-83ff-11eb-842c-d5c455a96b4f.png">

- 커밋로그 정하기

  [사이트 참조](https://doublesprogramming.tistory.com/256)

  - 예시로 코드를 추가했을 때 [#1] Feat UI화면 꾸미기

- branch 이름

  스탭 별로 develop-step1 로 만든 후

  PR에서 리뷰를 받고 코드 개선 후 main에 merge하기.

- 타입 설계

  클래스, 구조체, 열거형에 대한 선수지식 공부

  Fruit와 Juice는 열거형으로 나열.

  Stock은 구조체로 만들어서 JuiceMaker 클래스에 인스턴스 생성 후 초기재고 구현

## Step2

<img width="849" alt="스크린샷 2021-03-13 오후 2 18 08" src="https://user-images.githubusercontent.com/70311145/111020141-01840980-8407-11eb-8bd8-b4ab7999e1b8.png">

- View를 구현하기 위해 SDK에 대한 내용 공부

  타이틀 - Label

  재고수정 - Button

  과일 이미지 - Label로 구현 후 이모지 적용

  재고 현황 - Label

  주문버튼 - Button

  오토레이아웃 적용 - 스택뷰 활용.

  디바이스 가로모드만 지원

- MVC 패턴에 대해 이해하고 코드 연결 후 동작 구현

<img width="786" alt="스크린샷 2021-03-13 오후 2 24 44" src="https://user-images.githubusercontent.com/70311145/111020258-df3ebb80-8407-11eb-9691-c2f117c25daf.png">

MARK:- 를 활용하여 코드 분기처리

옵셔널 값을 어떻게 안전하게 처리할 수 있을까 고민하다가 옵셔널이 들어간 코드에 전부 guard let을 활용하여 옵셔널 바인딩 처리했음.

하나의 Outlet과 Action으로 여러 Lable과 Button을 한번에 처리할 수 없을까 고민하다가 인스턴스를 배열로 받기로 결정 후 구현.

- Alert에 대한 이해

![스크린샷 2021-03-13 오후 2 28 25](https://user-images.githubusercontent.com/70311145/111020327-668c2f00-8408-11eb-8422-22d2e1620d88.png)

UIAlertController와 UIAlertAction에 대한 공부

클래스 본문에 쓰면 코드가 길어지고 가독성이 떨어질 경우를 대비하여

Extension을 통해서 Aleart 구현.

## Step3

## 문제점 / 고민한점

- 타입 설계에 대한 공부를 더 해야겠다고 생각했다.
- 싱글턴 패턴을 활용하여 하나의 인스턴스로 앱을 구현할 수 있을까 고민했다.
- 타입 설계 후 Controller를 구현할 때 타입에 대한 문제점이 하나씩 보이고
  몇몇 수정한 부분이 있었다. 어떻게 하면 한번에 알아보기 쉽고, 불러오기 쉽게 구현할 수 있을까 고민해 보았다.
- 함수를 어떻게 최대한 한 동작만 할 수 있게 나눌 수 있을까에 대한 고민을 해보았다.

## 회고
