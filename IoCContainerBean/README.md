# IoC Container and Bean

Inversion of Control: 의존 관계 주입(Dependency)이라고도 하며, 어떤 객체가 사용하는 **의존 객체를 직접 만들어 사용하는게 아니라, 주입 받아 사용하는 방법**을 말한다.

## 스프링 IoC 컨테이너

+ BeanFactory: 빈의 생성과 관계 설정 제어를 담당하는 IoC오브젝트 
+ 애플리케이션 컴포넌트 중앙 저장소
+ **빈 설정 소스**로 부터 **빈 정의**를 읽어들이고, **빈을 구성하고 제공**한다.

## Bean
+ 스프링 IoC 컨테이너가 관리 하는 객체
+ 장점
    + 의존성 관리
    + 스코프
        + 싱글톤: 하나
        + 프로토타입: 매번 다른 객체
    + 라이프사이클 인터페이스

## ApplicationContext
+ BeanFactory
+ 메시지 소스 처리 기능(i18n)
+ 이벤트 발행 기능
+ 리소스 로딩 기능
+ ...

## 스프링 IoC 컨테이너 역할
+ 빈 인스턴스 생성
+ 의존 관계 설정
+ 빈 제공

## ApplicationContext
+ ClassPathXmlApplicationContext(XML)
+ AnnotationConfigApplicationContext(Java)

## 빈 설정
+ 빈 명세서
+ 빈에 대한정의를 담고 있다.
    + 이름
    + 클래스
    + 스코프
    + 생성자 아규먼트(constructor)
    + 프로퍼티(setter)
    + ...
    
    
## ResourceLoader

리소스를 읽어오는 기능을 제공하는 인터페이스

ApplicationContext extends ResourceLoader

리소스 읽어오기
+ 파일 시스템에서 읽어오기
+ classpath에서 읽어오기
+ URL로 읽어오기
+ 상대/절대 경로를 읽어오기