# Difference between interfaces and classes in TypeScript ?

Tags: Theory

## **Interface:**

- interface is a virtual structure witch define the properties and methods for object with name and data type.
- in TypeScript we use `Interface` keyword to create new interface with identity.
- interface is a virtual structure that is used for type-checking

### Example:

```jsx
// Interface for Class
interface myInterface {
  name: string;
  age: number;
}

let myProfile: myInterface = {
  name: "sandeep",
  age: 23,
};
console.log("myProfile", myProfile);

// Interface for object with extands Class
interface myInterfaceNew extends myInterface {
  role: string;
}

let myProfileNew: myInterfaceNew = {
  name: "sandeep",
  age: 23,
  role: "developer",
};
console.log("myProfileNew", myProfileNew);
```

## **Classes:**

- classes are the skeleton of the objects where we implement objects
- we use `Class` keyword to create the constructor of the object
- it can have properties, methods and variables.

### Example:

```jsx
// first letter of class name should be capital for indentify its a class
class AboutClass {
  name: string;
  age: number;
  role: string;

// Constructor of class
  constructor(name: string, age: number, role: string) {
    this.name = name;
    this.age = age;
    this.role = role;
  }

// aboutMe Object
  aboutMe() {
    console.log("name", this.name);
    console.log("age", this.age);
    console.log("role", this.role);
  }
}

const about = new AboutClass("sandeep", 23, "dev");
console.log("aboutMe", about.aboutMe());
```

## **The difference between interface and classes are below:**

| Interface | Classes |
| --- | --- |
| We can Create the interface with the use of the interface keyword.
i.e. interface Interface_Name{   \\ Interface Body } | We can create the class with class keyword.
i.e. class Class_Name{ \\ Class Body } |
| The interface blueprint is mainly the Type structure of object. It is object with only defining the type of parameter inside. | Class is the blueprint of the object. the create purposes of class is how we implement the object of our code. |
| It is used for type checking purpose. Use of interface if TypeScript language is mainly focused on the checking the type of parameters in object. | Classes in Types script is used to made the object for something. It is used for implementing the object. |
| We cannot create the instance of interface with new in typescript. It means that we cannot create the copy of instance in Typescript. | We can create a new instance of the class in TypeScript. It means that we can create the copy of class with new keyword. |
| Interface is virtual structure. Means it only present in TypeScript code not in TypeScript compiled JavaScript code. | It always exists in code after the compilation of TypeScript to JavaScript. |