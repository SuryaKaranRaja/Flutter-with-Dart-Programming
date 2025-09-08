# Zoo Animal Organizer (Dart Example)

This sample Dart program demonstrates how to manage and analyze a collection of zoo animals using core Dart types, a **List**, and a **Map**. It teaches the essentials of list manipulation, filtering, and map usage.

---

### Example Dart Program
```
void main() {
  List<String> animals = ['Cat', 'Dog', 'Rabbit'];
  animals.add('Elephant');
  animals.insert(1, 'Tiger');
  animals.remove('Dog');
  animals.removeAt(2);
  String firstAnimal = animals[0];
  print('Animals list: $animals');
  print('First animal: $firstAnimal');
  animals.addAll(["Cow", "Fox"]);
  print("After add all the animals : $animals");
  animals.sort();
  print("After sorting the animals : $animals");
  bool isTiger = animals.contains("Tiger");
  isTiger
      ? print("Tiger was present in the zoo collection")
      : print("Tiger was not in the zoo collection");

  animals.add('Cow');
  animals.add('Cow');
  // Using where - returns an Iterable of elements equal to "Cow"
  var cows = animals.where((element) => element == "Cow").toList();

  if (cows.isNotEmpty) {
    print("Cow was present ${cows.length} time(s) in the zoo collection");
  } else {
    print("Cow was not in the zoo list");
  }

  // Mapping functions

  Map<String, dynamic> animalData = {
    "collection": "Zoo Collection",
    "Place": "India",
    "animal": animals,
  };

  String india = animalData['Place'];

  print("Zoo is in $india");
  print(animalData.keys);
  print(animalData.values);
}

```

---

### Example Output
```
Animals list: [Cat, Tiger, Elephant]
First animal: Cat
After add all the animals : [Cat, Tiger, Elephant, Cow, Fox]
After sorting the animals : [Cat, Cow, Elephant, Fox, Tiger]
Tiger was present in the zoo collection
Cow was present 3 time(s) in the zoo collection
Zoo is in India
(collection, Place, animal)
(ZOO Collection, India, [Cat, Cow, Elephant, Fox, Tiger, Cow, Cow])
```
---

## Program Output Explanation

- Shows the state of the animals list after each modification.
- Confirms presence of `"Tiger"`.
- Counts and displays how often `"Cow"` appears.
- Prints the location of the zoo and displays map keys and values.
- 
## Key Concepts

### List Operations
- The `animals` list stores animal names.
- Elements are added (`add`, `addAll`), inserted (`insert`), removed (`remove`, `removeAt`), and sorted (`sort`).
- The `contains` method checks for the presence of an item.
- The `where` method filters elements based on a condition.

### Duplicate Handling
- Multiple `"Cow"` entries illustrate handling duplicates.
- `where` filters and counts occurrences of `"Cow"`.

### Map Usage
- The `animalData` map holds structured information about the zoo collection.
- Keys include `"collection"`, `"Place"`, and `"animal"`.
- Keys and values can be printed or accessed directly.

---

---
