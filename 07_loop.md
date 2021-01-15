# 반복문

## while문

while문은 주어진 조건이 만족되는 동안 문장들을 반복 실행하는 문장 구조이다.

while문의 형식은 다음과 같다.

    while(repeating condition)
        statement;

while문은 조건식의 값이 참인 동안에는 주어진 문장을 반복 실행한다. 조건식의 값이 거짓이 되면 반복을 중지한다.

---

## do while문

while문과 비슷하나 반복 조건을 루프의 처음이 아니라 루프의 끝에서 검사한다는 것이 다르다,
즉, 1번은 무조건 실행한다는 뜻이다.

do while문의 형식

    do
        repeat statement;
    while(condition);

위의 방식이다.

---

## for문

for문은 문장을 정해진 횟수만큼 반복하여 실행하는 반복 구조이다. for loop라고 부른다.

for문은 초기식, 조건식, 증감식의 3부분으로 구성된다.

    for (초기식 ; 조건식 ; 증감식)
        repeat statement;

예를들어

    for(i = 0; i <= 5> i ++)
        repeat statement;

위의 방식이다.

--- 

## continue break

break문은 반복 루프를 벗어나기위하여 사용한다. 반복 루프 안에서 break문이 실행되면 반복루프를 빠져 나오게 된다.

### goto문의 사용
 goto문을 사용해서도 무한 루프를 걸어논 반복문을 빠져나올수 있다.
>p274 참고

### continue 문
현재 실행하고 있는 반복 과정의 나머지를 생략하고 다음 반복을 시작하게 만든다.