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

**21년 2회**<br>
 (가)에 알맞은 예약어를 쓰시오.

```java
	public class Main {
   public static void main(String[] args){
      System.out.print(Main.check(1));
   }
   
  (가) String check (int num) {
      return (num >= 0) ? "positive" : "negative";
   }
}
``` 

<details>
<summary>✅ 정답</summary>
static
</details>
<br>

🖋 **문제 풀이** <br><br>
- check 메서드를 static으로 선언해야 main 메서드에서 클래스 이름으로 직접 호출할 수 있다.<br>
- 이를 통해 Main 클래스의 check 메서드를 사용할 수 있다.<br>

<hr> 

**21년 2회**<br>
출력 결과는? 
```java
	public class ovr1 {
	public static void main(String[] args){
    	ovr1 a1 = new ovr1();
        ovr2 a2 = new ovr2();
        System.out.println(a1.sun(3,2) + a2.sun(3,2));
    }
    
    int sun(int x, int y){
    	return x + y;
    }
}
class ovr2 extends ovr1 {
 
	int sun(int x, int y){
    	return x - y + super.sun(x,y);
    }
 
}
``` 

<details>
<summary>✅ 정답</summary>
11
</details>
<br>

🖋 **문제 풀이** <br><br>
- `ovr1` 클래스의 `sun` 메서드는 `x + y`를 반환.
- `ovr2` 클래스는 `ovr1`을 상속받고, `sun` 메서드를 오버라이드하여 `x - y + super.sun(x, y)`를 반환.
- 따라서 `a1.sun(3, 2)` 결과는 5이고, `a2.sun(3, 2)` 결과는 6이므로, 최종 출력은 5 + 6(a1.sun(3,2) + a2.sun(3,2)) = 11.

<hr> 

**21년 3회😿**<br>
출력 결과는? 
```java
class Connection {
  private static Connection _inst = null;
  private int count = 0;
     public static Connection get() {
      if(_inst == null) {
      _inst = new Connection();
      return _inst; 
      }
    return _inst;
    }
  public void count() { count ++; }
  public int getCount() { return count; }
}
 
public class Main {
  public static void main(String[] args) {
    Connection conn1 = Connection.get();
    conn1.count();
    Connection conn2 = Connection.get();
    conn2.count();
    Connection conn3 = Connection.get();
    conn3.count();
    
    System.out.print(conn1.getCount());
  }
}
``` 

<details>
<summary>✅ 정답</summary>
3
</details>
<br>

🖋 **문제 풀이** <br><br>
1. **Singleton 패턴**<br>
- `Connection` 클래스는 오직 하나의 인스턴스만 생성되도록 설계되었습니다.<br>

2. **`get()` 메서드**<br>
- `_inst`가 `null`이면 새로운 `Connection` 객체를 생성하고, 그렇지 않으면 이미 생성된 객체를 반환합니다.<br>

3. **`count()` 메서드**<br>
- `count` 변수를 1 증가시킵니다.<br>

실행과정 <br>

```java
Connection conn1 = Connection.get(); // 인스턴스 생성 (count: 0 → 1)
conn1.count(); // count: 1  // count: 1 (첫 번째 호출)
Connection conn2 = Connection.get();  // 이미 생성된 인스턴스 반환
conn2.count(); // count: 2 // count: 2 (두 번째 호출)
Connection conn3 = Connection.get(); // 같은 인스턴스 반환
conn3.count(); // count: 3 count: 3 (세 번째 호출)

System.out.print(conn1.getCount()); // 출력: 3

```
- 모든 count() 호출이 같은 인스턴스에서 이루어지므로, 최종 count 값은 3.

<hr>

**21년 3회**<br>
출력 결과는? 

```java
	public class Main{
 public static void main(String[] args) {
  int a = 3, b = 4, c = 3, d = 5;
  if((a == 2 | a == c) & !(c > d) & (1 == b ^ c != d)) {
   a = b + c;
    if(7 == b ^ c != a) {
     System.out.println(a);
    } else {
    System.out.println(b);
    }
  } else {
    a = c + d;
    if(7 == c ^ d != a) {
    System.out.println(a);
    } else {
    System.out.println(d);
    }
  }
 }
}
``` 

<details>
<summary>✅ 정답</summary>
7 
</details>
<br>

🖋 **문제 풀이** <br><br>
**1. 조건문 해석** 

```java
if((a == 2 | a == c) & !(c > d) & (1 == b ^ c != d)) {
```
- a == 2: false (3이 2와 같지 않음)<br>
- a == c: true (3이 3과 같음)<br>
- (a == 2 | a == c) )<br>
- 조건식 확인: false | true → true (OR 연산자))<br><br>
- !(c > d): true (3이 5보다 크지 않음)<br>
- 1 == b: false (1이 4와 같지 않음)<br>
- c != d: true (3이 5와 같지 않음)<br>
- 1 == b ^ c != d<br>
- 조건식 확인: false ^ true → true (XOR 연산자)<br><br>
- 1 == b ^ c != d: true (false ^ true는 true)<br>
- 전체 조건식 확인: true & true & true → true.

**2. 최종 결론**

```java
a = b + c; // a = 4 + 3 = 7
```

**3. 다음 조건문**
```java
if(7 == b ^ c != a) {
```
- 7 == b: 7 == 4 → false
- c != a: 3 != 7 → true
- 7 == b ^ c != a: false ^ true → true
- 따라서 System.out.println(a);가 실행되고, 최종적으로 7이 출력.

<hr> 

### <h3 id="year22">📋22년 기출</h3>

**22년 1회**<br>
출력 결과는? 

```java
	class A {
  int a;
  int b;
}
  
  public class Main {
  
  static void func1(A m){
   m.a *= 10;
  }
  
  static void func2(A m){
    m.a += m.b;
  }
  
  public static void main(String args[]){
  
  A m = new A();
  
  m.a = 100;
  func1(m);
  m.b = m.a;
  func2(m);
  
  System.out.printf("%d", m.a);
  
  }
}
``` 

<details>
<summary>✅ 정답</summary>
2000 
</details>
<br>

🖋 **문제 풀이** <br><br>
1. 클래스 A<br>
- 두 개의 정수 a와 b를 가진 클래스.
2. 메인 메서드<br>
- A 타입의 객체 m을 생성하고, m.a를 100으로 초기화.
- func1(m) 호출: m.a에 10을 곱해. 따라서 m.a는 1000.
- m.b에 m.a의 값을 할당.m.b는 1000.
- func2(m) 호출: m.a에 m.b의 값을 더함. 즉, m.a = 1000 + 1000이 되어 m.a는 2000.

**22년 1회**<br>
(가)에 들어갈 알맞은 답을 쓰시오.

```java
	class Car implements Runnable{
  int a;
  
  public void run(){
    try{
      while(++a<100){
        System.out.println("miles traveled :" +a);
        Thread.sleep(100);
      }
    }
     catch(Exception E){}
  }
}
  
public class Main{
  public static void main(String args[]){
    Thread t1 = new Thread(new (가)());
    t1.start();
  }
}
``` 

<details>
<summary>✅ 정답</summary>
(가 ) : Car
</details>
<br>

🖋 **문제 풀이** <br><br>
1. Car 클래스 <br>
- Runnable을 구현해서 스레드처럼 동작. <br>
- int a는 이동한 마일 수를 저장. <br>
- run() 메서드 <br>
	- a를 1씩 늘리면서 100 미만일 때까지 반복. <br>
	- 매 반복마다 현재 a 값을 출력하고, 0.1초(100ms) 기다림. <br>

2. Main 클래스 <br>
- main 메서드에서 Thread 객체를 만들고, Car 객체를 생성해서 전달. <br>
- t1.start()로 스레드를 시작.

3. 결론 <br>
(가)에는 Car를 넣어야함. 그러면 Car의 run() 메서드가 실행되고, 마일 수가 출력됨

<hr>

**22년 2회**<br>
출력 결과는?

```java
	class Main {  
  public static void main(String args[]) { 
    int i=3, k=1;
  switch(i){
    case 1:k+=1;
    case 2:k++;
    case 3:k=0;
    case 4:k+=3;
    case 5:k-=10;
    default : k--;
  }
System.out.print(k);
  } 
}
``` 

<details>
<summary>✅ 정답</summary>
(가 ) : Car
</details>
<br>

🖋 **문제 풀이** <br><br>
1. i 3부터 시작 <br>
2. k = 0 0 + 3 -10 = -7 - 1 = -8

<hr>

**22년 2회😿**<br>
출력 결과는?

```java
	class Conv{
  public Conv(int a){
    this.a=a;
  }
  int func(){
    int b=1;
    for(int i =1;i<a;i++){
      b=a*i+b;
    }
    return a+b;
  }
}
 
public class Main {  
  public static void main(String args[]) { 
    Conv obj=new Conv(3);
    obj.a=5;
    int b=obj.func();
    System.out.print(obj.a+b);
  } 
}
``` 

<details>
<summary>✅ 정답</summary>
61
</details>
<br>

🖋 **문제 풀이** <br><br>
Conv(3)을 통해서 a=3 이 되었지만, 바로 뒤에 obj.a=5 를 통해 a=5.<br>
그래서 메소드 func()를 풀어보면 for( int i=0; i<5 ; i++)는 아래와 같이 계산됨<br><br>

b= 5*1 + 1 = 6<br>
b= 5*2 + 6 = 16<br>
b=5*3 + 16 = 31<br>
b= 5*4 + 31 = 51<br>

반복문을 마친후, a+ b 값을 return 하라고 했으니, return값은 56<br>
int b = obj.func() b의 최종 값은 56<br>
obj.a + b = 5+ 56 = 61

<hr>

<hr>

**22년 2회😿**<br>
출력 결과는?

```java
	public class Test{
 public static void main(String[] args){
  int []result = int[5];
  int []arr = [77,32,10,99,50];
  for(int i = 0; i < 5; i++) {
    result[i] = 1;
    for(int j = 0; j < 5; j++) {
      if(arr[i] <arr[j]) 
        result[i]++;
    }
  }
 
  for(int k = 0; k < 5; k++) {
    printf(result[k]);
   }
 }
}
``` 

<details>
<summary>✅ 정답</summary>
61
</details>
<br>

🖋 **문제 풀이** <br><br>
1. 배열 생성<br>
arr = {77, 32, 10, 99, 50}<br>
2. 순위 계산 로직<br>
result 배열을 만들어 각 숫자의 순위를 저장.<br>
3. 순위 계산 방법<br>
- 첫 번째 반복 (i): 각 숫자 선택<br>
- 두 번째 반복 (j): 모든 숫자와 비교<br>
if (arr[i] < arr[j]): 선택한 숫자보다 큰 숫자가 있으면 result[i]를 1 증가시킴.<br><br>
예시<br>
77: 보다 큰 수 99 → 1개 → 순위 2<br>
32: 보다 큰 수 50, 77, 99 → 3개 → 순위 4<br>
10:  보다 큰 수 32, 50, 77, 99 → 4개 → 순위 5<br>
99:  보다 큰 수 없음 → 0개 → 순위 1<br>
50:  보다 큰 수 77, 99 → 2개 → 순위 3<br>
4.최종 결과<br>
result 배열 = {2, 4, 5, 1, 3}

<hr>

**22년 2회**<br>
출력 결과는?

```java
public class Main {
  static int[] MakeArray(){
 
  int[] tempArr = new int[4];
  
  for(int i=0; i<tempArr.Length;i++){
    tempArr[i] = i;
  }
  
  return tempArr;
  }
  
  public static void main(String[] args){
  
  int[] intArr;
  intArr = MakeArray();
  
  for(int i=0; i < intArr.Length; i++)
  System.out.print(intArr[i]);
 
  }
}
``` 

<details>
<summary>✅ 정답</summary>
0123
</details>
<br>

🖋 **문제 풀이** <br><br>
1. 배열 생성<br>
- MakeArray 메서드에서 크기가 4인 tempArr 배열을 만듬.<br>

2. 값 할당<br>
- for 루프를 사용해 tempArr의 각 인덱스에 0부터 3까지의 값을 할당.<br>

4. 배열 반환<br>
- tempArr 배열을 반환.<br>
- 
4. 메인 메서드<br>
- MakeArray를 호출해 intArr에 저장<br>
- 다시 for 루프를 사용해 intArr의 모든 값을 출력<br>

<hr>

**22년 3회**<br>
출력 결과는?

```java
public class Exam {
  public static void main(String[] args){
  
  int a = 0;
  for(int i=1; i<999; i++){
    if(i%3==0 && i%2!=0)
      a = i;
    }
    System.out.print(a);
  }
}
``` 

<details>
<summary>✅ 정답</summary>
993
</details>
<br>

🖋 **문제 풀이** <br><br>

3의 배수 (i % 3 == 0) <br>
2의 배수가 아님 (i % 2 != 0) <br>
이 두 조건을 모두 만족하는 마지막 숫자가 993이기 때문에 993이 출력됨

<hr>

### <h3 id="year23">📋23년 기출</h3>

**23년 1회**<br>
출력 결과는?

```java
class Static{
  public int a=20;
  static int b=0;
}
 
 
public class Main {
  public static void main(String[] args) {
    int a=10;
    Static.b=a;
    Static st=new Static();
 
    System.out.println(Static.b++);
     System.out.println(st.b);
     System.out.println(a);
     System.out.println(st.a);
  }
}
``` 

<details>
<summary>✅ 정답</summary>
10
11
10
20
</details>
<br>

🖋 **문제 풀이** <br><br>
1. 클래스 Static<br>
- a: 인스턴스 변수 (기본값 20)<br>
- b: 정적 변수 (기본값 0)<br>

2. 메인 클래스 Main<br>
- int a = 10;: 지역 변수 a (값 10)<br>
- Static.b = a;: Static.b에 10을 할당 → b는 이제 10.<br>

3. 출력 결과 설명<br>
3-1. System.out.println(Static.b++);<br>
- 현재 Static.b는 10. 이를 출력하고 1 증가시킴 → 출력: 10.<br>

3-2. System.out.println(st.b);:<br>
st.b는 정적 변수, 현재 값은 11. → 출력: 11.<br>

3-3.System.out.println(a);<br>
메인 메서드의 지역 변수 a는 10. → 출력: 10.<br>

3-4. System.out.println(st.a);<br>
st.a는 인스턴스 변수, 기본값은 20. → 출력: 20.

<hr>

**23년 1회**<br>
출력 결과는?(20년 3회 기출과 동일)

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
Vehicle name : Spark
</details>
<br>

🖋 **문제 풀이** <br><br>
1. Vehicle 클래스<br>
- 추상 클래스, getName(String val) 메서드가 추상.<br>
- getName() 메서드는 name을 반환.<br>

2. Car 클래스 (Vehicle 상속):<br>
- 생성자에서 name을 "Spark"로 초기화.<br>
- getName(String val)  메서드는 매개변수를 사용해 "Car name: "을 반환.<br>

3. Main 클래스<br>
- Car 객체를 생성하고 Vehicle 타입으로 참조.
- obj.getName() 호출 시 Vehicle의 getName() 메서드 실행.

이때 **추상 클래스**는 
- abstract class Vehicle로 선언된 클래스는 직접 인스턴스를 만들 수 없음. 즉, Vehicle 타입의 객체를 생성할 수 없음.
- 대신, Vehicle을 상속받은 구체적인 자식 클래스(예: Car)에서 구현을 제공해야 함.

<hr>

**23년 1회**<br>
출력 결과는?(20년 3회 기출과 동일)

```java
	class Parent {
int x = 100;
 
Parent() {
this(500);
}
Parent(int x) {
this.x = x;
}
int getX() {
return x;
}
}
class Child extends Parent {
int x = 1000;
 
Child() {
this(5000);
}
 
Child(int x) {
this.x = x;
}
 
 
}
 
public class Main {
public static void main(String[] args) {
Child obj = new Child();
System.out.println(obj.getX());
}
}
``` 

<details>
<summary>✅ 정답</summary>
Vehicle name : Spark
</details>
<br>

🖋 **문제 풀이** <br><br>
1. Vehicle 클래스<br>
- 추상 클래스, getName(String val) 메서드가 추상.<br>
- getName() 메서드는 name을 반환.<br>

2. Car 클래스 (Vehicle 상속):<br>
- 생성자에서 name을 "Spark"로 초기화.<br>
- getName(String val)  메서드는 매개변수를 사용해 "Car name: "을 반환.<br>

3. Main 클래스<br>
- Car 객체를 생성하고 Vehicle 타입으로 참조.
- obj.getName() 호출 시 Vehicle의 getName() 메서드 실행.

이때 **추상 클래스**는 
- abstract class Vehicle로 선언된 클래스는 직접 인스턴스를 만들 수 없음. 즉, Vehicle 타입의 객체를 생성할 수 없음.
- 대신, Vehicle을 상속받은 구체적인 자식 클래스(예: Car)에서 구현을 제공해야 함.

<hr>


**23년 1회**<br>
출력 결과는?

```java
	class Parent {
int x = 100;
 
Parent() {
this(500);
}
Parent(int x) {
this.x = x;
}
int getX() {
return x;
}
}
class Child extends Parent {
int x = 1000;
 
Child() {
this(5000);
}
 
Child(int x) {
this.x = x;
}
 
 
}
 
public class Main {
public static void main(String[] args) {
Child obj = new Child();
System.out.println(obj.getX());
}
}
``` 

<details>
<summary>✅ 정답</summary>
500
</details>
<br>

🖋 **문제 풀이** <br><br>
1. **`Child` 객체 생성**<br>
   - `Child obj = new Child();`로 `Child` 클래스의 객체를 생성.<br>
   - 이때 `Child()` 생성자가 호출되고, `this(5000);`을 통해 `Child(int x)` 생성자를 호출.<br>
2. **`Child(int x)` 생성자 실행**<br>
   - `Child(int x)`에서 `this.x = x;`를 통해 `Child` 클래스의 `x` 값을 `5000`으로 설정.<br>
   - 이 시점에서 `Child`의 `x`는 `5000`이야.<br>
3. **부모 클래스 생성자 호출**<br>
   - `Child` 클래스의 생성자가 끝나기 전에, `Parent` 클래스의 생성자도 호출돼.<br>
   - `Parent()` 생성자가 호출되고, 여기서 `this(500);`를 통해 `Parent(int x)` 생성자가 호출.<br>
4. **`Parent(int x)` 생성자 실행**<br>
   - `Parent(int x)`에서 `this.x = x;`가 실행되며, 여기서 `this`는 `Parent` 클래스의 변수를 참조, `Parent` 클래스의 `x`가 `500`으로 설정.<br>
5. **`getX()` 메서드 호출**<br>
   - `System.out.println(obj.getX());`에서 `getX()` 메서드를 호출하면, `Parent` 클래스의 `getX()`가 실행.<br>
   - 이 메서드는 `Parent` 클래스의 `x` 값을 반환하므로 결과적으로 `500`이 출력.<br><br>
**요약**
- `getX()`는 `Child` 객체에서 호출되지만, 실제로는 `Parent` 클래스의 메서드를 실행.
- `Child` 객체의 생성 과정에서 부모 클래스의 생성자도 호출되고, 그 결과로 `Parent` 클래스의 `x` 값이 설정.

<hr>

**23년 2회**<br>
출력 결과는?

```java
public class Main {
public static void main(String[] args) {
      String str1 = "Programming"; 
      String str2 = "Programming";
      String str3 = new String("Programming");
      
      System.out.println(str1==str2);
      System.out.println(str1==str3);
      System.out.println(str1.equals(str3));
      System.out.print(str2.equals(str3));
}
}
``` 

<details>
<summary>✅ 정답</summary>
true
false
true
true
</details>
<br>

🖋 **문제 풀이** <br><br>
1. `str1 == str2`<br>
- **결과**: `true`<br>
- **설명**: `str1`과 `str2`는 리터럴 문자열로, 자바는 같은 문자열 리터럴을 공유하기 때문에 두 변수는 같은 메모리 주소를 가리킴.<br>

2. `str1 == str3`<br>
- **결과**: `false`<br>
- **설명**: `str3`는 `new String("Programming")`을 사용하여 생성된 객체로, 새로운 메모리 공간에 할당됨. 그래서 `str1`과 `str3`는 서로 다른 객체를 가리키므로 `false`가 출력됨.<br>

3. `str1.equals(str3)`<br>
- **결과**: `true`<br>
- **설명**: `equals` 메서드는 두 객체의 내용이 같은지를 비교함. `str1`과 `str3`의 내용은 모두 `"Programming"`이므로 `true`가 출력됨.<br>

4. `str2.equals(str3)`<br>
- **결과**: `true`<br>
- **설명**: `str2`도 `str3`와 내용이 동일하므로, `equals` 메서드는 `true`를 반환함.<br>

요약<br>
- `==` 연산자는 객체의 메모리 주소를 비교하고, `equals` 메서드는 객체의 내용을 비교함<br>

<hr>

**23년 3회**<br>
출력 결과는?

```java
	public class Main {
	public static void main(String[] args) {
		A b = new B();
		b.paint();
		b.draw();
	}
}
class A {
	public void paint() {
		System.out.print("A");
		draw();
	}
	public void draw() {
		System.out.print("B");
		draw();
	}
}
class B extends A {
	public void paint() {
		super.draw();
		System.out.print("C");
		this.draw();
	}
	public void draw() {
		System.out.print("D");
	}
}
``` 

<details>
<summary>✅ 정답</summary>
true
false
true
true
</details>
<br>

🖋 **문제 풀이** <br><br>
1. `str1 == str2`<br>
- **결과**: `true`<br>
- **설명**: `str1`과 `str2`는 리터럴 문자열로, 자바는 같은 문자열 리터럴을 공유하기 때문에 두 변수는 같은 메모리 주소를 가리킴.<br>

2. `str1 == str3`<br>
- **결과**: `false`<br>
- **설명**: `str3`는 `new String("Programming")`을 사용하여 생성된 객체로, 새로운 메모리 공간에 할당됨. 그래서 `str1`과 `str3`는 서로 다른 객체를 가리키므로 `false`가 출력됨.<br>

3. `str1.equals(str3)`<br>
- **결과**: `true`<br>
- **설명**: `equals` 메서드는 두 객체의 내용이 같은지를 비교함. `str1`과 `str3`의 내용은 모두 `"Programming"`이므로 `true`가 출력됨.<br>

4. `str2.equals(str3)`<br>
- **결과**: `true`<br>
- **설명**: `str2`도 `str3`와 내용이 동일하므로, `equals` 메서드는 `true`를 반환함.<br>

요약<br>
- `==` 연산자는 객체의 메모리 주소를 비교하고, `equals` 메서드는 객체의 내용을 비교함<br>

<hr>


