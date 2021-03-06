# 조건문

## 제어문

프로그램에서는 기본적으로 각 문장들이 순차적으로 실행된다.
문장들이 실행되는 순서에 영향을 주는 문장을 __제어문__ 이라고 한다.
제어문은 크게 2가지로 나뉜다.

### 조건문
if 문장과 switch 문장이 조건문에 속한다.

### 반복문
for 문장과 while 문장이 반복문에 속한다.

---

## if 문

조건이 참일 경우에만 뒤의 문장이 실행되는 문장이다.

영어에서 if문을 만약 ~하면 ~한다로 해석되는 것처럼 똑같다.

if문의 형식

    if(조건)
        {문장}

이렇다.

---

## if else 문

if문은 조건이 참일경우에만 해당 문장이 실행되는데 if else문은 조건이 참이 아니더라도 실행가능한 문장을 입력가능하다.

if else 문의 형식

    if(조건)
        {문장}
    else(조건)
        {문장}

이렇다.

if else문을 응용하여 여러개의 조건을 집어넣을수도 있다.

if else문은 삼항연산자 ?를 표현할 수 있다.

---

## 다중 if 문

if문도 하나의 문장이므로, if문을 여러개 나열해서 조건을 여러개 줄수도 있고, if문 안에 if문을 넣어서
추가적으로 조건을 부여할 수도 있다.

예를들어

    if(condition)
    else if(condition)
    else if(condition)
    else

이런것도 가능하고

    if(condition)
        {
            statement
            if(condition)
        }

이런것도 충분히 가능하다.

---

## switch 문

if문에서는 조건의 가짓수가 1개의 if문에서 2개밖에 안되는데, 실행가능한 경로가 여러개인 경우에는 switch문을 사용하는것이 좋다.

switch문 예시

    switch(제어식)
    {
        case1 condition1 : //condition1에 부합할 때
            statement
            break;

        case2 condition2 :
            statement;
            break;  

        defalut :  //일치하는 값이 없을 때
            statement;
            break;
    }

### 주의할 점
> break문이 없으면 선택된 case절 안의 문장들을 실행한 다음, 계속해서 다음 case절의 문장들을 실행하게 된다. 연속되는 오류가 발생하게된다.

> case절에 있는 수식은 반드시 __정수 상수__ 이어야 한다. 다음과 같이 case절에 실수나 변수, 수식, 문자열을 사용하는 것은 컴파일 오류이다. 따라서 case절의 condition문은 정수 상수 만을 사용해야한다. 


switch 문이 편할때도 있지만, if else문이 훨씬 편할때도 존재하므로 그때그때 비교하며 선택하여야한다.

---

## goto문

goto문은 조건없이 어떤 위치(원하는 위치)로 점프하게 만드는 문장이다.
goto문의 사용은 잘 권장되지는 않는데 프로그램을 아주 복잡하게 만들기 때문이다.

goto문의 형식은 goto와 레이블의 두 부분으로 구성된다. 레이블은 점프를 원하는 위치에 이름을 붙인 것이다. 식별자를 만들 때 적용했던 규칙들을 이용하여 레이블을 만들고 원하는 위치에 적은 후 콜론을 붙이면 된다.
레이블이 붙어 있는 위치로 실행 위치를 변경하려면 다음과 같이 goto다음에 레이블의 이름을 적어주고 세미콜론을 붙이면 된다. goto문은 함수 안에서만 점프할 수 있다. 함수 사이의 점프는 불가능하다.

    goto error;


    error: 
        printf("오류발생");

이런 형식으로 goto문을 사용하면 된다.

