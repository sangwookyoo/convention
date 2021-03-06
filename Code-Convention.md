# π Coding convention (C-sharp)

β C# λͺ¨λ² μ¬λ‘λ₯Ό μ μν©λλ€. <br>
β λ μ΄μμμ΄ μλ λ΄μ©μ μ§μ€ν  μ μλλ‘ μΌκ΄μ± μκ² νμλλ μ½λλ₯Ό λ§λ­λλ€. <br>
β μ΄μ  κ²½νμ ν λλ‘ ν κ°μ μ ν΅ν΄ μ½λλ₯Ό λ³΄λ€ λΉ λ₯΄κ² μ΄ν΄ν  μ μλλ‘ ν©λλ€. <br>
β μ½λλ₯Ό λ³΄λ€ μ½κ² λ³΅μ¬, λ³κ²½ λ° μ μ§ κ΄λ¦¬ν  μ μλλ‘ ν©λλ€. <br>

### π’ λ μ΄μμ κ·μΉ
- κΈ°λ³Έ μ½λ νΈμ§κΈ° μ€μ (μ€λ§νΈ λ€μ¬μ°κΈ°, 4μ λ€μ¬μ°κΈ°, ν­μ κ³΅λ°±μΌλ‘ μ μ₯)μ μ¬μ©νλ€.
- ν μ€μ ν λ¬Έμ₯λ§ μμ±νλ€.
- ν μ€μ νλμ μ μΈλ§ μμ±νλ€.
- λ©μλ μ μμ μμ± μ μ μ¬μ΄μ νλ μ΄μμ λΉ μ€μ μΆκ°νλ€.
- μ€κ΄νΈμ μμΉλ BSD μ€νμΌμ μ€μνλ€.
- λ©μλλ Unity Script Lifecycle Flowchart μμλλ‘ μμ±νλ€.
- λ€μ μμ κ°μ΄, κ΄νΈλ₯Ό μ¬μ©νμ¬ μμ μ μ λͺννκ² κ΅¬λΆν©λλ€.
 ```cs
if ((val1 > val2) && (val1 > val3))
{
    // Take appropriate action.
}
```

### π’ μ£Όμμ²λ¦¬ κ·μΉ
- λλ¬Έμλ‘ μ£Όμ νμ€νΈλ₯Ό μμνλ€.
- λ§μΉ¨νλ‘ μ£Όμ νμ€νΈλ₯Ό μ’λ£νλ€.
- λ€μ μμ κ°μ΄, μ£Όμ κ΅¬λΆ κΈ°νΈ(//)μ μ£Όμ νμ€νΈ μ¬μ΄μ κ³΅λ°±μ νλ μ½μνλ€.
```cs
// The following declaration creates a query. It does not run
// the query.
```
- λ€μ μμ κ°μ΄, λ¬Έμνκ° νμν μ£Όμμ /* ... */ μ μ¬μ©νμ¬ μμ±νλ€.
```cs
/*
* The following declaration creates a query. It does not run
* the query.
*/
```

### π’ λͺλͺκ·μΉ
- μμ½μ΄λ₯Ό μ¬μ©νμ§ μλλ€.
- λ€μ μμ κ°μ΄, λ©μλλͺμ νμ€μΉΌ μΌμ΄μ€(Pascal case)λ₯Ό μ¬μ©νλ©° λμ¬λ‘ μμνλ€.
```cs
public void SetMethod()
{
    // Take appropriate action.
}
```
- λ€μ μμ κ°μ΄, λ©μλ μΈμ λ° λ³μμλ μΉ΄λ© μΌμ΄μ€(Camel case)λ₯Ό μ¬μ©νλ©° λͺμ¬λ‘ μμνλ€.
```cs
public float myTimer;
public int myCount;
public string myName;
```
- λ€μ μμ κ°μ΄, private λ³μλͺμ '_'λ₯Ό μΆκ°νλ€.
```cs
private float _myTimer;
private int _myCount;
private string _myName;
```
- λ€μ μμ κ°μ΄, μ΄κ±°ν ν€μλλ μλ¬Έ λλ¬Έμλ₯Ό μ¬μ©νλ€.
```cs
public enum Sound
{
    BGM,
    EFFECT,
    3DSOUND
}
```
- λ€μ μμ κ°μ΄, URL, HTMLμ κ°μ λ²μ©μ μΈ λλ¬Έμ μ½μ΄λ λλ¬Έμ κ·Έλλ‘ μ¬μ©νλ€.
```cs
parseHTML
parseXML
```

### π’ μΈμ΄μ§μΉ¨
  - λ€μ μμ κ°μ΄, μ κ·Όμ νμλ public-private μμλλ‘ μ μΈνλ€.
```cs
// Bad:
public float timer = 1.2f;
private string _name = "myString";
public int count = 1;

// Good:
public float timer = 1.2f;
public int count = 1;
private string _name = "myString";
```
  - λ€μ μμ κ°μ΄, μ μΈκ³Ό λμμ ν λΉνλ λ³μ λ¨Όμ  μ μΈνλ€.
```cs
// Bad:
public float timer = 1.2f;
public int count;
public string name = "myString";

// Good:
public float timer = 1.2f;
public string name = "myString";
public int count;
```
  - λ€μ μμ κ°μ΄, λ¦¬ν°λ΄ μ μ μ λμμ°μ°μ μλ€μ κ³΅λ°±μ μΆκ°νλ€.
```cs
// Bad:
public float timer= 1.2f;
public int count =1;
public string name="myString";

// Good:
public float timer = 1.2f;
public int count = 1;
public string name = "myString";
```
  - λ€μ μμ κ°μ΄, μ°μ°μ μλ€μ κ³΅λ°±μ μΆκ°νλ€.
```cs
// Bad:
a+b +c+ d = 15;
new Vector3(1,0,0);

// Good:
a + b + c + d = 15;
new Vector3(1, 0, 0);
```
  - λ€μ μμ κ°μ΄, μΆμ½μ΄ κ°λ₯ν μ°μ μ°μ°μλ μΆμ½νλ€.
```cs
// Bad:
a = a + b;
a = a - b;
a = a * b;
a = a / b;
a = a % b;

// Good:
a += b;
a -= b;
a *= b;
a /= b;
a %= b;
```
  - λ€μ μμ κ°μ΄, μ±λ₯κ°μ μ μν΄ κ°λ₯ν κ²½μ° μ°μ μ°μ°μλ₯Ό λμ²΄νλ€.
```cs
// Bad:
int count = 1;
int num = count / 10;

// Good:
int count = 1;
int num = count * 0.1;
```

### π’ μ°Έκ³ λ¬Έμ
- [C# μ½λ© κ·μΉ | Microsoft Docs](https://docs.microsoft.com/ko-kr/dotnet/csharp/fundamentals/coding-style/coding-conventions)
