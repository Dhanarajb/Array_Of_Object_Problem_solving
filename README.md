# Array_Of_Object_Problem_solving
---
#### Array Of Object
```
const people = [
  { name: 'John', age: 30 },
  { name: 'Alice', age: 25 },
  { name: 'Bob', age: 35 }
];
```
---
#### Problem 1: Find the Total Age
```
const totalAge = people.reduce((acc, person) => acc + person.age, 0);
console.log(totalAge); 
```
---
#### Problem 2: Filter by Age
```
const peopleAbove30 = people.filter(person => person.age > 30);
console.log(peopleAbove30);
```
---
#### Problem 3: Find the Youngest Person
```
const youngestPerson = people.reduce((min, person) => (person.age < min.age ? person : min));
console.log(youngestPerson);
```
---
#### Problem 4: Convert to Array of Names
```
const names = people.map(person => person.name);
console.log(names);
```
---
#### Problem 5: Check for Property
```
const hasProperty = people.every(person => 'age' in person);
console.log(hasProperty);
```
---
#### Problem 6: Sort by Age
```
const sortedByAge = people.sort((a, b) => a.age - b.age);
console.log(sortedByAge);
```
---
#### Problem 7: Group by Age
```
const groupedByAge = people.reduce((group, person) => {
  const age = person.age;
  group[age] = group[age] || [];
  group[age].push(person);
  return group;
}, {});

console.log(groupedByAge);
```
---
#### Problem 8: Sum Property
```
const sumAges = people.reduce((sum, person) => sum + person.age, 0);
console.log(sumAges);
```
---
#### Problem 9: Find by Name
```
const findByName = name => people.find(person => person.name === name);
console.log(findByName('Alice'));
```
---
#### Problem 10: Remove Duplicates
```
const uniquePeople = Array.from(new Set(people.map(person => person.name)))
  .map(name => people.find(person => person.name === name));
console.log(uniquePeople);
```
---
#### Problem 11: Update Property
```
const updateAge = (name, newAge) => {
  const updatedPeople = people.map(person => (person.name === name ? { ...person, age: newAge } : person));
  console.log(updatedPeople);
};

updateAge('Alice', 26);
```
---
#### Problem 12: Find Average Age
```
const averageAge = totalAge / people.length;
console.log(averageAge);
```
----
#### Problem 13: Check for Adults
```
const allAdults = people.every(person => person.age >= 18);
console.log(allAdults);
```
---
#### Problem 14: Extract Unique Ages
```
const uniqueAges = Array.from(new Set(people.map(person => person.age)));
console.log(uniqueAges);
```
---
#### Problem 15: Separate Adults and Minors
```
const adults = people.filter(person => person.age >= 18);
const minors = people.filter(person => person.age < 18);
console.log(adults, minors);
```
---
#### Problem 16: Count People by Age
```
const countByAge = people.reduce((count, person) => {
  count[person.age] = (count[person.age] || 0) + 1;
  return count;
}, {});

console.log(countByAge);
```
---

