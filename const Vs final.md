# Dart: `final` vs `const`

## Definitions
- **final**  
  A `final` variable can be assigned only once and its value cannot be changed afterwards. However, it can be initialized at *runtime*, meaning the value can be determined dynamically when the program runs.

- **const**  
  A `const` variable is a *compile-time* constant — its value must be known and fixed at compile time. It also implies immutability (like `final`), but with stricter requirements.

---

## Key Differences

| Aspect | `final` | `const` |
|---|---:|---:|
| When assigned | At runtime (once assigned, cannot change) | At compile time (must be known beforehand) |
| Can be reassigned | No | No |
| Use case | Values computed dynamically (e.g., current time) | Fixed constant values (e.g., π, literals) |
| Performance | Slightly less efficient (runtime value) | More efficient (evaluated at compile time) |
| Example | `final now = DateTime.now();` | `const pi = 3.14159;` |

---

## Example Usage

```dart
void main() {
  // final variable - runtime assigned once
  final String name = "Surya";
  print("Final variable: $name");

  // const variable - compile-time constant
  const int age = 28;
  print("Const variable: $age");

  // final can be assigned a runtime value
  final DateTime now1 = DateTime.now();
  print("Final DateTime: $now1");

  // const DateTime now2 = DateTime.now();  // Error: needs compile-time value
}
