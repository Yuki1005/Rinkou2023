# Javaとは
Javaは、世界中にたくさんの開発者がいる有名な言語。  
大規模システム、Webアプリケーション、スマートフォンアプリなど、Javaはあなたの周りの様々な場所で活躍している。（なお、JavaとJavaScriptは全くの無関係）

# classとは
クラス（class）はオブジェクト指向プログラミングの基本的な仕組みを提供するもので、オブジェクト（インスタンス とも言う）が持つ、属性（アトリビュート、プロパティ とも呼ばれる）や、メソッド（関数、ファンクション と呼ばれる）などを定義する。

```Java
class クラス名 {
    型 属性;
     :
    型 メソッド() { ... }
     :
}
```
# print文
## Python
```Python
str1 = "ささのは"
str2 = "たきいこ"
print("Hello Java")
print(3+1)
print(3*4)
print(str1 + str2 )
print()
print(str1)
print(str2)
```
## Java
```Java
class Main {
  public static void main(String[] args) {
    String str1 ="ささのは";
    String str2 = "たきいこ";
    System.out.println("Hello Java");
    System.out.println(3+1);
    System.out.println(3*4);
    System.out.println(str1 + str2);
    System.out.println();
    System.out.print(str1);
    System.out.print(str2);
  }
}
```
## 結果
```
Hello Java  
4  
12  
ささのはたきいこ  
  
ささのはたきいこ  
```

# 例
```Java
class Person {
    String myName;
    int myAge;
    public void SetName(String name) {
        myName = name;
    }
    public String GetName() {
        return myName;
    }
    public void SetAge(int age) {
        myAge = age;
    }
    public int GetAge() {
        return myAge;
    }
}
```

```java
class PersonTest {
    public static void main(String[] args) {
        Person tanaka = new Person();
        tanaka.SetName("Tanaka");
        tanaka.SetAge(26);

        Person suzuki = new Person();
        suzuki.SetName("Suzuki");
        suzuki.SetAge(32);

        System.out.println(tanaka.GetName());
        System.out.println(tanaka.GetAge());
        System.out.println(suzuki.GetName());
        System.out.println(suzuki.GetAge());
    }
}
```




| 用語 | 別の呼び方 | サンプルでの具体例 |
| ---- | ---- | ---- |
| クラス |  | Person |
| 属性 | アトリビュート、プロパティ | myName、myAge |
| メソッド | ファンクション、関数 | SetName()、GetName()、SetAge()、GetAge() |
| インスタンス | オブジェクト | tanaka、suzuki |

# voidとは
avaでメソッドを定義するときは、メソッド名・引数・戻り値の３つを指定して宣言をします。この時、メソッドの戻り値の型にvoidを指定すると、そのメソッドは値を返さないメソッドとして定義される。  
  
voidとは「何もない」という意味で、Javaではメソッドの戻り値のみに指定できる特別な型として存在し、戻り値がvoidとして宣言されたメソッドは、return時には何も値をかえさない。（逆にreturn時に値を戻すとコンパイルエラーとなる）

# クラスの継承（extends）
あるクラスのメンバ変数やメソッドを 継承 した サブクラス（子クラス）を定義するには extends を用いる。
```Java
class クラス名 extends 親クラス名 {
    :
}
```

下記の例では、上記で作成した Person クラスを継承する Member クラスを定義しています。Member クラスは Person クラスを継承しているので、myName、myAge などの属性や、GetName()、SetName() などのメソッドを引き継ぎ、加えて、myNumber や SetNumber() などの属性やメソッドを備えている。

```Java
class Member extends Person {
    int myNumber;
    public void SetNumber(int number) {
        myNumber = number;
    }
    public int GetNumber() {
        return myNumber;
    }
}
```