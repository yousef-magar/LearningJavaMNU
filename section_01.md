## 🎯 الفكرة العامة

الـ **class** = "وصف أو تصميم لشيء" (زي قالب أو blueprint).
الـ **object** = "النسخة الحقيقية من الشيء دا" (اللي بتتكوّن من الكلاس).

مثال من الحياة الواقعية:

* عندك **class** اسمه `Car` = وصف عام لأي عربية (فيها اسم، سرعة، موديل...).
* لكن لما تعمل عربية معينة (زي تويوتا أو BMW) = دي بقت **object** من الكلاس دا.

---

## 🧩 مثال بسيط من دماغي

### تعريف الكلاس

```java
package section_001;

public class Car {
    // الخصائص (Attributes)
    private String name;
    int maxSpeed;
    float price;

    // دالة setter (علشان نحط قيمة)
    void setName(String n) {
        name = n;
    }

    // دالة getter (علشان نرجع القيمة)
    String getName() {
        return name;
    }

    // دالة تمثل سلوك (Behavior)
    void drive() {
        System.out.println(name + " is driving at speed " + maxSpeed + " km/h");
    }
}
```

---

### استخدام الكلاس (Main)

```java
package section_001;
import java.util.*;

public class MainCar {
    public static void main(String[] args) {

        // عمل object من الكلاس Car
        Car myCar = new Car();
        
        // استخدام الـ setter لتحديد الاسم
        myCar.setName("Toyota");
        myCar.maxSpeed = 220;
        myCar.price = 300000;

        // استخدام الـ getter لطباعة الاسم
        System.out.println("Car name: " + myCar.getName());
        System.out.println("Max speed: " + myCar.maxSpeed);
        System.out.println("Price: " + myCar.price);

        // تجربة method أخرى
        myCar.drive();
    }
}
```

🔹 **الناتج:**

```
Car name: Toyota
Max speed: 220
Price: 300000.0
Toyota is driving at speed 220 km/h
```

---

## 🧠 كدا نجي للفكرة الأساسية:

| المفهوم                     | المعنى                                   | مثال                                |
| --------------------------- | ---------------------------------------- | ----------------------------------- |
| **Class**                   | التصميم أو القالب                        | `Car`, `Student`, `Animal`          |
| **Object**                  | النسخة الفعلية                           | `new Car()`, `new Student()`        |
| **Attribute (خصائص)**       | معلومات عن الكائن                        | `name`, `age`, `price`              |
| **Method (دوال)**           | سلوك أو وظيفة                            | `setName()`, `getName()`, `drive()` |
| **Encapsulation (الكبسلة)** | إخفاء البيانات (private + getter/setter) | عشان محدش يغيّر `name` مباشرة       |

---

## 🧩 مثال Assignment بتاعك: Student

```java
package section_001;

public class Student {
    private String name;
    private int age;

    // Setter methods
    void setName(String n) {
        name = n;
    }

    void setAge(int a) {
        age = a;
    }

    // Getter methods
    String getName() {
        return name;
    }

    int getAge() {
        return age;
    }
}
```

---

### المين كلاس

```java
package section_001;
import java.util.*;

public class MainStudent {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // عمل object من الكلاس Student
        Student s1 = new Student();

        // إدخال بيانات من المستخدم
        System.out.print("Enter student name: ");
        String name = sc.nextLine();

        System.out.print("Enter student age: ");
        int age = sc.nextInt();

        // تخزين البيانات في الـ object
        s1.setName(name);
        s1.setAge(age);

        // طباعة البيانات
        System.out.println("\nStudent Details:");
        System.out.println("Name: " + s1.getName());
        System.out.println("Age: " + s1.getAge());
    }
}
```

🔹 **ناتج التنفيذ:**

```
Enter student name: Yousef
Enter student age: 21

Student Details:
Name: Yousef
Age: 21
```

---

## 🧱 الخلاصة

| الكلمة                 | معناها                            |
| ---------------------- | --------------------------------- |
| `class`                | تعريف الشيء بشكل عام              |
| `object`               | نسخة من الكلاس                    |
| `new`                  | كلمة بنستخدمها لإنشاء object      |
| `Scanner`              | كلاس جاهز من Java بناخد منه input |
| `System.out.println()` | بتطبع سطر على الكونسول            |

---


