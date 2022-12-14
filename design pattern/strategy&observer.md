# Strategy&Observer Pattern
___
##### 전략 패턴(Strategy Pattern)
- 정책 패턴이라고도 하며, 객체의 행위를 바꾸고 싶은 경우, **'직접'** 수정하지 않고, 전략이라고 부르는 캡슐화한 알고리즘을 컨텍스트 안에서 바꿔주면서, 상호 교체가 가능하게 만드는 패턴


##### 옵저버 패턴(Observer Pattern)
- 옵저버 패턴이란, 주체가 어떤 객체(Object)의 상태 변화를 관찰하다가 상태 변화가 있을 때마다 메서드 등을 통해 옵저버 목록에 있는 옵저버들에게 변화를 알려주는 디자인 패턴이다.  
- 주체란 객체의 상태 변화를 보고 있는 관찰자이며, 옵저버들이란 이 객체의 상태 변화에 따라 전달되는 메서드 등을 기반으로 '추가 변화 사항'이 생기는 객체들을 의미한다.
- 옵저버 패턴을 활용한 서비스로는 트위터를 들 수 있으며, 어떤 사람인 주체를 팔로우 했다면, 주체가 포스팅을 올리게 되면 알림이 팔로워에게 가야하는 것과 같다.