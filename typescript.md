# TypeScript

---

### **Table of Contents**  
1. [Introduction to TypeScript](#introduction-to-typescript)  
2. [Installing TypeScript](#installing-typescript)  
3. [Setting Up the Environment](#setting-up-the-environment)  
4. [Code Examples](#code-examples)  
5. [Useful TypeScript Commands](#useful-typescript-commands)  
6. [Additional Resources and Links](#additional-resources-and-links)  

---

### **Introduction to TypeScript**  

TypeScript is a superset of JavaScript that adds optional static typing and other advanced features to JavaScript, making it easier to develop scalable and less error-prone applications. It is widely used in medium to large-scale projects and is especially helpful when working with modern libraries and frameworks like React, Angular, and Vue.js.  

---

### **Installing TypeScript**  

To install TypeScript globally in your development environment, use **npm** (Node Package Manager):  
```bash
npm install -g typescript
```  

To check if the installation was successful:  
```bash
tsc --version
```  

---

### **Setting Up the Environment**  

1. **Starting a TypeScript Project:**  
   Use the command below to create the `tsconfig.json` configuration file:  
   ```bash
   tsc --init
   ```  

2. **Example of `tsconfig.json`:**  
   ```json
   {
     "compilerOptions": {
       "target": "es6",
       "module": "commonjs",
       "strict": true,
       "outDir": "./dist",
       "rootDir": "./src"
     },
     "include": ["src/**/*"],
     "exclude": ["node_modules"]
   }
   ```  

3. **Project File Structure:**  
   ```
   my-typescript-project/
   ├── src/
   │   ├── index.ts
   ├── dist/
   ├── tsconfig.json
   ├── package.json
   ```

---

### **Code Examples**  

#### Basic Typing  
```typescript
let message: string = "Hello, TypeScript!";
console.log(message);
```

#### Functions  
```typescript
function add(a: number, b: number): number {
  return a + b;
}
console.log(add(5, 10));
```

#### Interfaces and Classes  
```typescript
interface Person {
  name: string;
  age: number;
}

class Student implements Person {
  constructor(public name: string, public age: number, public course: string) {}

  introduce(): string {
    return `Hi, I'm ${this.name}, and I study ${this.course}.`;
  }
}

const student = new Student("Alice", 22, "Computer Science");
console.log(student.introduce());
```

#### Generics  
```typescript
function identity<T>(arg: T): T {
  return arg;
}

console.log(identity<number>(42));
console.log(identity<string>("TypeScript is great!"));
```

#### Handling Promises and Async/Await  
```typescript
async function fetchData(url: string): Promise<string> {
  const response = await fetch(url);
  return response.text();
}

fetchData("https://jsonplaceholder.typicode.com/posts/1").then(data => console.log(data));
```

---

### **Useful TypeScript Commands**  

1. **Compile TypeScript Files:**  
   ```bash
   tsc
   ```  

2. **Watch for Code Changes:**  
   ```bash
   tsc --watch
   ```  

3. **Run TypeScript Files with `ts-node`:**  
   Install `ts-node`:  
   ```bash
   npm install -g ts-node
   ```  
   Run the file directly:  
   ```bash
   ts-node src/index.ts
   ```  
