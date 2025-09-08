# Personal Information Organizer (Dart Example)

This sample Dart program demonstrates how to organize and display personal data using core Dart types, a **List**, and a **Map**. It helps beginners understand the essentials of variable declaration, the role of the `main()` function, and how collection types are handled in Dart.

---

### Key Concepts

#### main() Function
- Every Dart program starts with the `main()` function.  
- It acts as the entry point and contains all executable statements.

#### Variable Declaration
- `String`, `int`, and `double` are used to store basic personal information such as **name**, **age**, **SSLC marks**, and **HSC marks**.  
- `bool` is used to indicate gender.  
- `List<String>` holds the subjects of interest.  

These variables demonstrate Dart’s **strong typing** and **modern syntax**.

#### Map Usage
- A `Map<String, dynamic>` called **myData** is used to store all personal attributes.  
- The values in the map cover different data types: string, integer, double, boolean, and list.  
- This demonstrates how Dart can handle **complex and mixed data** effectively.

#### forEach Loop with Type Checking
- The program uses `forEach` to iterate over the map.  
- A type check (`value is List`) ensures lists are displayed as **comma-separated strings** instead of Dart’s default bracketed format.  
- Non-list values are displayed directly, producing **clean, readable output**.

---

### What the Program Does
1. Declares basic personal attributes (name, age, marks, gender, qualification, and interests).
2. Stores them inside a map called **myData**.
3. Iterates through the map using a loop.
4. Prints each key-value pair in a neat format, formatting lists properly.

---

### Example Dart Program
```
void main() {
  String name = "Surya Karan";
  int age = 28;
  double SSLC = 462;
  double HSC = 930;
  bool isMale = true;
  String qualification = "BE (ECE)";
  List<String> subjectOfInterest = [
    "Transmission Lines and Waveguides",
    "Electronics Devices 1 and 2"
  ];

  Map<String, dynamic> myData = {
    "Name": name,
    "Age": age,
    "Male ": isMale,
    "SSLC Mark out of 500": SSLC,
    "HSC Mark out of 1200": HSC,
    "Educational qualification": qualification,
    "Area of Interest": subjectOfInterest
  };

  myData.forEach((key, value) {
    if (value is List) {
      print("$key : ${value.join(', ')}"); // prints list neatly
    } else {
      print("$key : $value");
    }
  });
}
```

---

### Example Output
```
Name : Surya Karan
Age : 28
Male : true
SSLC Mark out of 500 : 462.0
HSC Mark out of 1200 : 930.0
Educational qualification : BE (ECE)
Area of Interest : Transmission Lines and Waveguides, Electronics Devices 1 and 2
```

---

### Learning Points
- **Maps can store dynamic values**, making them versatile for representing structured data.  
- **Type checking** allows proper handling of lists vs. primitive values.  
- Such structured examples build the foundation for more advanced **Dart** and **Flutter** applications.  
```
