# 🔧 Методы и прототипы объектов в JavaScript 💡

> 🧠 В JavaScript всё основано на объектах.  
> Методы Object и система прототипов позволяют создавать, изменять и наследовать поведение объектов.  
> Разберёмся, как это работает — просто и красиво 👇

---

## 🧩 Что такое прототип?

Каждый объект в JS имеет *прототип* — это *другой объект*, от которого он наследует свойства и методы.

```js
const user = { name: "Ali" };
console.log(Object.getPrototypeOf(user)); 
// 👉 вернёт Object.prototype

const animal = { eats: true };
const dog = Object.create(animal);
dog.barks = true;

console.log(dog.eats); // true (унаследовано от animal)
console.log(dog.barks); // true (собственное)

for (let [key, value] of Object.entries(user)) {
  console.log(${key}: ${value});
}

const entries = [["name", "Ali"], ["age", 25]];
const obj = Object.fromEntries(entries);

console.log(obj); // { name: "Ali", age: 25 }

const user = { name: "Ali", age: 25 };
console.log(Object.keys(user)); // ["name", "age"]
