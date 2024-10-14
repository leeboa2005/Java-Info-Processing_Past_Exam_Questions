## 정보처리기사 자바 기출 문제 모음 


### 목차 
- [20년 기출](#year20)
- [21년 기출](#year21)
- [22년 기출](#year22)
- [23년 기출](#year23)
- [24년 기출](#year24)
  
### <h3 id="year20">📋20년 기출</h3>

**20년 1회**

```java
class Main {  
  static int[] arr() { 
    int a[]=new int[4];
    int b = a.length;
    for(int i =0; i<b;i++)
      a[i]=i;
    return a;
  } 
 
  public static void main(String args[]) { 
  int a[]=arr();
  for(int i =0; i< a.length; i++)
    System.out.print(a[i]+" ");
  } 
}
``` 

<details>
<summary>✅ 정답</summary>
0 1 2 3
</details>
<br>

🖋 **문제 풀이** <br>

1. 메서드 arr()<br>
- 정수형 배열 a를 길이 4로 생성.<br>
- for 루프를 통해 배열에 인덱스 값을 할당 (0부터 3까지).<br>

2. main 메서드<br>
- arr() 메서드를 호출하여 배열 a를 받음.<br>
- for 루프를 통해 배열의 요소를 출력.

<hr>

**20년 2회**<br>
 (가)에 들어갈 알맞은 답을 쓰시오

```java
	class Parent{
  void show(){System.out.println("parent");}  
}
class Child extends Parent{
  void show() {System.out.println("child");}
}
 
class Main {  
  public static void main(String args[]) { 
    Parent pa=(가) Child();
    pa.show();
  } 
}
``` 

<details>
<summary>✅ 정답</summary>
new
</details>
<br>

🖋 **문제 풀이** <br>
1. 클래스 구조<br>
- Parent 클래스: show() 메서드를 정의.<br>
- Child 클래스: Parent를 상속하며 show() 메서드를 오버라이드.<br>

2. main 메서드<br>
- (가)에 들어갈 부분은 Child 객체를 Parent 타입으로 캐스팅하는 것.<br>
- Child 객체를 생성하기 위해 new 키워드가 필요.<br>

3. 결과<br>
- pa.show()를 호출하면 Child 클래스의 show() 메서드가 실행되어 "child"가 출력.<br><br>


**자바 키워드 및 개념**

| 키워드          | 설명                                      |
|------------------|-------------------------------------------|
| `new`            | 객체를 생성할 때 사용.                   |
| `class`          | 클래스를 정의할 때 사용.                 |
| `extends`        | 클래스를 상속할 때 사용.                 |
| `void`           | 반환값이 없는 메서드를 정의할 때 사용.   |
| `static`         | 클래스에 속하는 메서드나 변수를 정의할 때 사용. |
| `public`         | 접근 제어자로, 모든 클래스에서 접근 가능. |
| `private`        | 접근 제어자로, 같은 클래스 내에서만 접근 가능. |
| `protected`      | 접근 제어자로, 같은 패키지와 상속받은 클래스에서 접근 가능. |
| `abstract`       | 추상 클래스를 정의할 때 사용.            |
| `interface`      | 인터페이스를 정의할 때 사용.            |
| `implements`     | 인터페이스를 구현할 때 사용.            |
| `this`           | 현재 객체를 참조할 때 사용.              |
| `super`          | 부모 클래스의 메서드나 생성자를 호출할 때 사용. |


<hr>

**20년 2회😿**<br>
출력 결과는?

```java
class A{
	private int a;
    public A(int a){
    	this.a = a;
    }
    public void display(){
    	System.out.println("a=" + a);
    }
}
 
class B extends A {
	public B(int a){
    	super(a);
        super.display();
    }
}
 
 
public class Main {
	public static void main(String[] args){
    	B obj = new B(10);
    }
}

``` 

<details>
<summary>✅ 정답</summary>

</details>
<br>

🖋 **문제 풀이** <br>
1. B 객체 생성: B obj = new B(10);에서 B의 객체를 만들고 매개변수로 10을 전달.<br>
  ```java
   B obj = new B(10);
   ```
<br>

2. 부모 클래스 호출: 이 10은 super(a)를 통해 A 클래스의 생성자에 전달.<br>
 ```java
   public B(int a) {
      super(a); // A 클래스의 생성자를 호출
  }
   ```
<br>

3. 값 저장: A 클래스의 생성자가 실행되어 a에 10이 저장.<br>
 ```java
 public A(int a) {
    this.a = a; // a에 10을 저장
}
   ```
<br>

4. 출력: super.display()가 호출되어 A의 display() 메서드가 실행되고, a의 값이 출력되어 a=10.<br>
 ```java
public void display() {
    System.out.println("a=" + a); // a의 값을 출력
}
   ```
<hr>

**20년 2회**<br>
출력 결과는?

```java
public class Main{
	public static void main(String[] args){
    	int i=0, c=0;
        while (i<10){
         i++;
         c*=i;
        }
        System.out.println(c);
   }
  }
``` 

<details>
<summary>✅ 정답</summary>
0 
</details>
<br>

🖋 **문제 풀이** <br>
- i가 10보다 작을 동안 반복합니다.<br>
- i를 1씩 증가시킵니다.<br>
- c *= i;는 c = c * i;임으로<br>
  
```java
while (i < 10) {
    i++;
    c *= i; // c는 항상 0
}
```

<hr>

**20년 3회😿**<br>
출력 결과는? 

```java
	abstract class Vehicle{
	String name;
    abstract public String getName(String val);
    public String getName(){
    	return "Vehicle name:" + name;
    }
}
 
class Car extends Vehicle{
  private String name;
	public Car(String val){
    	name=super.name=val;
   }
public String getName(String val){
	return "Car name : " + val;
   }
public String getName(byte val[]){
	return "Car name : " + val;
   }
}
 
public class Main {
	public static void main(String[] args){
    Vehicle obj = new Car("Spark");
    System.out.print(obj.getName());
    }
}
``` 

<details>
<summary>✅ 정답</summary>

</details>
<br>

🖋 **문제 풀이** <br><br>

1. **추상 클래스 `Vehicle`**<br>
 - `String name;`: 이름을 저장하는 변수.<br>
 - `abstract public String getName(String val);`: 추상 메서드 선언.<br>
 - `public String getName()`: `name`을 반환하는 메서드.<br>

2. **`Car` 클래스**<br>
 - `Car`는 `Vehicle`을 상속받습니다.<br>
 - 생성자 `Car(String val)`에서 `super.name = val;`로 부모 클래스의 `name`을 초기화.<br>
 - `public String getName(String val)`: 매개변수 `val`을 사용하여 "Car name :"을 반환.<br>

3. **`Main` 클래스**<br>

   ```java
   Vehicle obj = new Car("Spark");
   System.out.print(obj.getName());
   ```
- Vehicle 타입의 obj를 Car 객체로 생성.<br>
- obj.getName() 호출 시, Vehicle 클래스의 getName()이 실행됨.

<hr>

**20년 3회😿**<br>
출력 결과는? 

```java
	public class Main {
	public static void main(String[] args){
    int i=0, sum=0;
    while (i<10){
    	i++;
        if(i%2 ==1)
        	continue;
        sum += i;
     }
     System.out.println(sum);
   }
}
``` 

<details>
<summary>✅ 정답</summary>
30
</details>
<br>

🖋 **문제 풀이** <br><br>

1. **변수 초기화**<br>
 - `int i = 0, sum = 0;`<br>
 - `i`는 루프 카운터, `sum`은 짝수의 합을 저장할 변수.<br>

2. **while 루프**<br>

   ```java
     while (i < 10) {
         i++; // i를 1 증가시킵니다.
         if (i % 2 == 1) // i가 홀수인 경우
             continue; // 다음 반복으로 건너뜀.
         sum += i; // i가 짝수인 경우 sum에 더함
     }
   ```
<hr>

**20년 4회**<br>
다음은 변수 n에 저장된 10진수를 2진수로 변환하여 출력하는 java프로그램이다. 프로그램을 분석하여 ( 1번 )( 2번 )빈칸에 알맞은 답을 쓰시오.

```java

class Main {
	public static void main (String[] args) {
    	int[]a = new int[8];
        int i=0; int n=10;
        while (  1번 ) {
        	a[i++] = ( 2번 );
            n /= 2;
        }
        for(i=7; i>=0; i--){
         System.out.print(a[i]);
        }
     }
  }
``` 

<details>
<summary>✅ 정답</summary>
(1번) : n>0
(2번) : n%2
</details>
<br>

🖋 **문제 풀이** <br><br>
1. n이 0보다 크면 반복하여 2로 나눈 나머지를 배열에 저장.<br>
2. 배열의 요소를 역순으로 출력하면 n의 2진수 표현.<br>
3. 
while 루프
   ```java
   while (n > 0) { // 1번 답: n > 0
       a[i++] = n % 2; // 2번 답: n % 2
       n /= 2; // n을 2로 나누어 몫을 저장
   }
```
<br>
- n이 0보다 크면 반복.<br>
- n을 2로 나눈 나머지를 배열 a에 저장.<br>
- n을 2로 나눈 몫을 n에 다시 저장.<br>

<hr>

**20년 4회**<br>

출력 결과는? 

```java
	class Parent{
	public int compute(int num){
    	if(num <=1) return num;
        return compute(num-1) + compute(num-2);
    }
 }
 
 class Child extends parent {
 	public int compute(int num){
    	if(num<=1) return num;
        	return compute(num-1) + compute(num-3);
        }
   }
   
  class Main{
  	public static void main (String[] args){
    Parent obj = new Child();
    System.out.print(obj.compute(4));
   }
 }
``` 

<details>
<summary>✅ 정답</summary>
1
</details>
<br>

🖋 **문제 풀이** <br><br>

1. **클래스 구조**<br>
 - `Parent`: Fibonacci 수열 계산.<br>
 - `Child`: `compute(num-3)`을 사용하여 계산.<br>

2. **`Main` 클래스**<br>
   
   ```java
   Parent obj = new Child();<br>
   System.out.print(obj.compute(4)); // Child의 compute(4) 호출
   ```

4. **compute(4) 계산**<br>
- compute(4) = compute(3) + compute(1)<br>
- compute(3) = compute(2) + compute(0)<br>
- compute(2) = compute(1) + compute(-1)<br>

4. **결과**<br>
- compute(1) = 1<br>
- compute(0) = 0<br>
- compute(-1) = -1   <br>
- compute(4) = 0 + 1 = 1<br>
- compute(3) = 0 + 0 = 0<br>
- compute(2) = 1 + -1 = 0<br>
정답은 compute(4) = 0 + 1 = 1


<hr>

### <h3 id="year21">📋21년 기출</h3>

**21년 1회**<br>
출력 결과는?

```java
public class Main{
	public static void main(String[] args){
    	int arr[][] = new int[][]{{45,50,75},{89}};
        System.out.println(arr[0].length);
        System.out.println(arr[1].length);
        System.out.println(arr[0][0]);
        System.out.println(arr[0][1]);
        System.out.println(arr[1][0]);
  }
}
``` 

<details>
<summary>✅ 정답</summary>
3
1
45
50
89


</details>
<br>

🖋 **문제 풀이** <br><br>
2차원 배열 초기화 <br>

```java
   int arr[][] = new int[][]{{45, 50, 75}, {89}};
```

- arr은 2개의 행을 가진 2차원 배열.<br>
- 첫 번째 행: {45, 50, 75} (길이 3)<br>
- 두 번째 행: {89} (길이 1)

```text
arr
┌───────────────┐
│   {45, 50, 75}│  → arr[0]
├───────────────┤
│      {89}     │  → arr[1]
└───────────────┘
```
<hr>

**21년 1회**<br>
출력 결과는? 

```java
	public class Main {
	public static void main(String[] args){
    int i, j;
    for(j=0, i=0; i<=5; i++){
     j+=i;
     System.out.print(i);
     if(i==5){
     System.out.print("=");
     System.out.print(j);
   } else{
   	System.out.print("+");
	}
   }
  }
 }

``` 

<details>
<summary>✅ 정답</summary>
0+1+2+3+4+5=15
</details>
<br>

🖋 **문제 풀이** <br><br>
1. **변수 초기화**
   
```java
   int i, j;
```
- i: 반복 카운터<br>
- j: 합계 저장 변수 (초기값 0)<br>

2. **for 루프**

```java
for(j=0, i=0; i<=5; i++) {
    j += i; // i 값을 j에 더함
    System.out.print(i); // 현재 i 출력
```
- i가 5 이하일 때까지 반복.<br>
- 각 반복에서 j에 현재 i 값을 더하고, i 값을 출력.<br>

3. **출력 형식** 

```java 
if(i==5) {
    System.out.print("="); // i가 5일 때 '=' 출력
    System.out.print(j); // 총합 출력
} else {
    System.out.print("+"); // 그 외에는 '+' 출력
}
```
출력 결과: 0+1+2+3+4+5=15

<hr>

**21년 1회**<br>

```java

``` 

<details>
<summary>✅ 정답</summary>

</details>
<br>

🖋 **문제 풀이** <br><br>



**21년 1회**<br>

```java

``` 

<details>
<summary>✅ 정답</summary>

</details>
<br>

🖋 **문제 풀이** <br><br>


