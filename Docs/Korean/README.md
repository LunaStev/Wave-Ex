# Wave
`Wave`는 컴파일 언어이다. 

`Wave`의 확장자는 `.wave`이다. 다른 확장자는 없다.

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

## if문
### main.wave
```
fun main() {
    count num1 = 30;
    
    if (num1 == 10) {
        printf("10 입니다.");
    } else if (num1 == 20) {
        printf("20 입니다.");
    } else {
        printf("10도 20도 아닙니다.");
    }
}
```
### 출력
#### count num1 = 10; 
```
>> 10 입니다
```
#### count num1 = 20;
```
>> 20 입니다.
```
#### count num1 = 30;
```
>> 10도 20도 아닙니다.
```
