/*void main() {
  int num1 = 20;
  double num2 = 10.5;
  double result1 = num1 + num2;
  double result2 = num1 * num2;
  double result3 = num1 - num2;
  double result4 = num1 / num2;
  double result5 = num1 % num2;
  bool isGreater = num1 > num2;
  bool isLess = num1 < num2;
  print(' these is result : $num1 + $num2 = $result1');
  print(' these is result : $num1 * $num2 = $result2');
  print(' these is result : $num1 - $num2 = $result3');
  print(' these is result : $num1 / $num2 = $result4');
  print(' these is result : $num1 % $num2 = $result5');
  print(' is $num1 greater than $num2? : $isGreater');
  print(' is $num1 less than $num2? : $isLess');
}*/
/*void main(){
  const double pi = 3.14;
  const double radius = 5.0;
  double area = pi * radius * radius;
  print('The area of the circle with radius $radius is $area');
}*/
/*void main() {
  String name = 'elia';
  int age = 23;
  String massege = 'my name is $name and my age is $age yers old';
  print(massege);
}*/
/*import 'dart:io';*/
/*void main() {
  print('entar your farst number:');
  double? num1 = double.tryParse(stdin.readLineSync()!);
  print('entar your operation (+, -, *, /, %):');
  String? operation = stdin.readLineSync();
  print('entar your second number:');
  double? num2 = double.tryParse(stdin.readLineSync()!);
  if (num1 == null || num2 == null || operation == null) {
    print('Invalid input. Please enter valid numbers and operation.');
    return;
  }
  double? result;
  if (operation == '+') {
    result = num1 + num2;
  } else if (operation == '-') {
    result = num1 - num2;
  } else if (operation == '*') {
    result = num1 * num2;
  } else if (operation == '/') {
    result = num1 / num2;
  } else if (operation == '%') {
    result = num1 % num2;
  }
  print('Result: $result');
}*/
/*import 'dart:io';*/
/*void main() {
  print('enter your day');
  int? day = int.tryParse(stdin.readLineSync()!);
  switch (day) {
    case 1:
      print(' Today is monday');
      break;
    case 2:
      print(' Today is tuesday');
      break;
    case 3:
      print(' Today is wednesday');
      break;
    case 4:
      print(' Today is thursday');
      break;
    case 5:
      print(' Today is friday');
      break;
    case 6:
      print(' Today is saturday');
      break;
    case 7:
      print(' Today is sunday');
      break;
    default:
      print('invalid day');
  }
}*/
/*void main() {
  for (int i = 1; i <= 20; i++) {
    if (i % 2 == 0) {
      print(i);
    }
  }
}*/
/*void main() {
  int i = 1;
  while (i <= 20) {
    if (i % 2 != 0) {
      print(i);
    }
    i++;
  }
}*/
/*import 'dart:io';*/
/*void main() {
  print("Enter a positive integer:");
  String? input = stdin.readLineSync();
  int number = int.parse(input ?? '0');
  int originalNumber = number;
  int sum = 0;
  do {
    int digit = number % 10;   
    sum += digit;               
    number = number ~/ 10;  
  } while (number > 0);
  print("The sum of digits in $originalNumber is: $sum");
}*/
/*void main(){
  for(int i=1;i<=50;i++){
    if (i%3==0)continue;
    print(i);
  }
}*/
/*void multiply (int a, int b) {
  int result = a * b;
  print('the result of $a * $b = $result');}
}
void main(){
  multiply(5, 6);
int multiply(int x, int y) => x * y;
void main(){
  int result = multiply(4, 7);
  print('the result of 4 * 7 = $result');
}*/
/*bool isEven(int number) {
  if (number % 2 == 0) {
    return true;
  } else {
    return false;
  }
}
void main() {
  print(isEven(10)); 
  print(isEven(7));  
}*/
/*void massage(String name) {
  print('hello $name');
}
void main() {
  massage('elia');
}*/
// 1. Function with Required and Optional Named Parameters
/*void describePerson({
  required String name,
  int age = 0,
  String occupation = 'Unknown',
}) {
  print('$name is $age years old and works as a $occupation.');
}
void main() {
  describePerson(name: 'Alice', age: 30, occupation: 'Engineer');
  describePerson(name: 'Bob', age: 25);
  describePerson(name: 'Charlie');
}*/
/*double calculateArea([double length = 1, double width = 1]) {
  return length * width;
}
void main() {
  print({calculateArea()}); 
  print({calculateArea(5, 4)});
}*/
/*void main() {
  List<int> numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  var doubledNumbers = numbers.map((number) => number * 2).toList();
  print(doubledNumbers);
}*/
/*Function makeMultiplier(int factor) {
  return (int number) => number * factor;
}
void main() {
  var doubleIt = makeMultiplier(2);
  var tripleIt = makeMultiplier(3);
  print(doubleIt(5));   
  print(tripleIt(5));   
}*/
// دالة الجمع
/*double add(double a, double b) => a + b;

// دالة الطرح
double subtract(double a, double b) => a - b;

// دالة الضرب
double multiply(double a, double b) => a * b;

// دالة القسمة مع معالجة القسمة على صفر
double? divide(double a, double b) {
  if (b == 0) {
    print("Error: Cannot divide by zero.");
    return null;
  }
  return a / b;
}

// الدالة الرئيسية للعمليات التي تستدعي الدوال الأخرى
void calculate(double num1, double num2, String operator) {
  double? result;

  switch (operator) {
    case '+':
      result = add(num1, num2);
      break;
    case '-':
      result = subtract(num1, num2);
      break;
    case '*':
      result = multiply(num1, num2);
      break;
    case '/':
      result = divide(num1, num2);
      break;
    default:
      print("Invalid operator!");
      return;
  }

  if (result != null) {
    print("Result: $num1 $operator $num2 = $result");
  }
}

void main() {
  // أمثلة لتشغيل الآلة الحاسبة
  calculate(10, 5, '+'); // الجمع
  calculate(10, 5, '-'); // الطرح
  calculate(10, 5, '*'); // الضرب
  calculate(10, 2, '/'); // القسمة
  calculate(10, 0, '/'); // تجربة القسمة على صفر
}*/
// دالة لتحويل أول حرف إلى كبير
/*String capitalize(String text) {
  if (text.isEmpty) return text;
  return text[0].toUpperCase() + text.substring(1).toLowerCase();
}

// دالة لإضافة علامة تعجب في النهاية
String exclaim(String text) {
  return "$text!";
}

// دالة التحية التي تدمج الدوال السابقة
String greet(String name) {
  String capitalizedName = capitalize(name);
  String shoutedName = exclaim(capitalizedName);
  return "Hello, $shoutedName";
}

void main() {
  // اختبار دالة greet بأسماء مختلفة
  print(greet("ahmed"));  // المخرجات: Hello, Ahmed!
  print(greet("SARA"));   // المخرجات: Hello, Sara!
  print(greet("gemini")); // المخرجات: Hello, Gemini!
}*/
/*void main() {
  List<int> ages = [20, 25, 30, 35];
  ages.add(40);          
  ages.addAll([45, 50]);
  ages.removeAt(0);
  print("Updated ages list: $ages");
  print("Total number of elements: ${ages.length}");
}*/
/*void main() {
  Set<String> words = {'welcom', 'elia', 'hi'};
  words.add('nagi');
  words.addAll({'elia', 'hi', 'oky'});
  words.remove('hi');
  print("Final set of words: $words");
}*/
/*void main() {
  // 1. قائمة الكتب المفضلة (List)
  List<String> favoriteBooks = [
    "Clean Code",
    "The Pragmatic Programmer",
    "Dart in Action",
    "Refactoring",
    "Design Patterns"
  ];

  print("--- Top 5 Favorite Books (using for loop) ---");
  // استخدام for loop التقليدية
  for (int i = 0; i < favoriteBooks.length; i++) {
    print("${i + 1}. ${favoriteBooks[i]}");
  }

  print("\n--- Favorite Hobbies (using forEach) ---");
  // 2. مجموعة الهوايات (Set)
  Set<String> hobbies = {"Reading", "Coding", "Gaming", "Swimming"};

  // استخدام forEach loop
  hobbies.forEach((hobby) {
    print("I love $hobby");
  });

  print("\n--- Item Prices (using Map forEach) ---");
  // 3. خريطة الأصناف وأسعارها (Map)
  Map<String, double> items = {
    "Laptop": 1200.50,
    "Mouse": 25.0,
    "Keyboard": 45.99,
    "Monitor": 250.0
  };

  // استخدام forEach لطباعة المفتاح والقيمة
  items.forEach((item, price) {
    print("Item: $item | Price: \$$price");
  });
}*/
/*void main() {
  // 1. استخدام reduce لإيجاد المجموع
  List<int> numbers = [10, 20, 30, 40, 50];

  // دالة reduce تدمج عناصر القائمة في قيمة واحدة
  int sum = numbers.reduce((value, element) => value + element);
  
  print("Sum of numbers: $sum"); // المخرجات: 150

  // ---------------------------------------------------------

  // 2. استخدام contains للتحقق من وجود عنصر في Set
  Set<String> fruits = {'Apple', 'Banana', 'Orange'};
  
  bool hasMango = fruits.contains('Mango');
  bool hasApple = fruits.contains('Apple');

  print("Contains Mango? $hasMango"); // false
  print("Contains Apple? $hasApple"); // true

  // ---------------------------------------------------------

  // 3. استخدام remove لحذف عنصر من Map
  Map<int, String> students = {
    101: "Ahmed",
    102: "Sara",
    103: "Ali"
  };


  // حذف الطالب صاحب الرقم 102
  students.remove(102);

  print("Updated Students Map: $students"); // المخرجات: {101: Ahmed, 103: Ali}
}*/