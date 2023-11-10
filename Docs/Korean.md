# Wave
Wave는 `WDK(Wave Devlopment Kit)`에서 작동된다. `WDK`에는 `Wave RuinTime`, `Wave VM`으로 이루어져 있다. 

`Wave`의 확장자는 `.wave`이다. 다른 확장자는 없다.

# Wave Devlopment Kit (WDK)

## Wave RunTime (WRT)
`WRT`는 `WVM`과 함께 Wave 컴파일러 실행에 필요한 라이브러리를 포함한다. `WRT`는 `WVM`을 실행하기 위해 필요한 기본적인 라이브러리를 제공한다.

## Wave Virtual Machine (WVM)
`WVM`은 `Wave` 실행하는 엔진인다. `WVM`은 `Wave` 프로그램을 기계어로 번역하여 실행한다. `WVM`은 운영 체제에 종속적이지 않기 때문에 `Wave`는 모든 운영 체제에서 실행될 수 있다.

# 문법
`Wave`의 `fun`이라는 용어는 `함수 선언`을 나타낸다. 모든 코드는 `main()` 함수 내에 있어야 한다. 그렇지 않으면 실행되지 않는다. `var` 키워드는 `변수 선언`에만 사용되는 반면 `count`는 `숫자 변수`에서만 사용된다. 유형 선언 `:String`은 `:str`로 표시될 수도 있으며 문자 데이터에만 사용된다. 또한 모든 명령문을 `세미콜론`(`;`)으로 끝내는 것이 중요하다.

파일을 가져올때는 `import` 키워드를 사용해야 한다. (예시: `import hello`) 

# 예시 코드 

## Hello, World! 출력
### main.wave
```
fun main() {
    print("Hello, World!");
}
```
### 출력
```
>> Hello, World!
```

## 변수 사용
### main.wave
```
fun main() {
    var a :String = "Hello ";
    var b :str = "World";

    conut c = 10;

    print(a);
    print(b);
    print(c);

    print(a + b + c);
}
```
### 출력
```
>> Hello 
>> World
>> 10
>> Hello World 10
```

## 다른 함수 가져다쓰기
```
fun hello() {
    print("Hello, World!");
}

fun main() {
    hello();
}
```
### 출력
```
>> Hello, World!
```


## 파일 가져다쓰기
### hello.wave
```
fun hello() {
    print("Hello, World!");
}
```
### main.wave
```
import hello;

fun main() {
    hello();
}
```
### 출력
```
>> Hello, World!
```
