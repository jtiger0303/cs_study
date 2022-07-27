# Singleton Pattern
___
싱글톤 패턴(singleton pattern)은 하나의 클래스에 오직 하나의 인스턴스만 가지는 패턴이다. 보통 데이터베이스 연결 모듈에 많이 사용된다. 

##### 싱글톤 패턴의 장점
1. 하나의 인스턴스를 만들어 놓고, 해당 인스턴스를 다른 모듈이 공유하며 사용하기 때문에 인스턴스를 생성할 때, 드는 비용이 줄어드는 장점이 있다.

##### 자바스크립트의 싱글톤 패턴
자바스크립트에서는 리터럴[] 또는 new Object로 객체를 생성하게 되면 다른 어떤 객체와도 같지 않기 때문에, 이 자체만으로 싱글톤 패턴을 구현할 수 있다.
```js
const obj={
    a: 27
}
const obj2={
    a: 27
}
console.log(obj===obj2)
//false
```

```js
class Singleton{
    constructor(){
        if(!Singleton.instance){
            Singleton.instance=this
        }
        return Singleton.instance
    }
    getInstance(){
        return this.instance
    }
}
const a= new Singleton()
const b= new Singleton()
console.log(a===b)
//true
```

##### 싱글톤 패턴의 단점
1. 싱글톤 패턴은 TDD(Test Driven Development)를 할 때, 걸림돌이 된다. TDD를 할 때 단위 테스트를 주로 하는데, 단위 테스트는 서로 독립적이어야 하며, 테스트를 어떤 순서로든 실행하여야 한다. 하지만 싱글톤 패턴은 미리 생성된 하나의 인스턴스를 기반으로 구현하는 패턴이므로, 각 테스트마다 독립적인 인스턴스를 만들기 쉽지 않다.
2. 모듈 간의 결합을 강하게 만들 수 있다는 단점-> **의존성 주입(DI, Dependency Injection)** 을 통해 모듈간의 결합을 조금 더 느슨히 만들어 해결 가능

- 의존성이란 종속성이라고도 하며, A가 B에 종속성이 있다는 것은 B의 변경 사항에 대해 A 또한 변해야 함을 의미