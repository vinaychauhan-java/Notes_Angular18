## **Introduction**

**Pipes**, a powerful feature used to transform data in templates. Pipes allow developers to format and manipulate data dynamically without modifying the actual data in the component. It enhances the readability and help in reducing code complexity by handling transformations directly within the HTML template.

---

## **What Are Pipes in Angular 18?**

Pipes are simple functions that take input data and return transformed output. They are used in Angular templates with the `|` (pipe) symbol.

### **Basic Syntax:**
```html
{{ value | pipeName }}
```
For example:
```html
{{ 'hello world' | uppercase }}
```
This converts **'hello world'** into **'HELLO WORLD'**.

---

## **Types of Pipes in Angular 18**
Angular provides **two types** of Pipes:

### **1. Built-in Pipes** (Provided by Angular)
- **DatePipe** → Formats dates
- **UpperCasePipe & LowerCasePipe** → Changes text case
- **CurrencyPipe** → Formats numbers as currency
- **DecimalPipe** → Formats numbers with decimals
- **PercentPipe** → Converts numbers to percentage format
- **SlicePipe** → Extracts a portion of a string or array
- **AsyncPipe** → Handles Promises and Observables

### **2. Custom Pipes** (User-defined for specific use cases)
- You can create custom pipes for **custom transformations**.

---

## **1. Built-in Pipes with Examples**

### **DatePipe - Formatting Dates**
```html
<p>Today: {{ today | date:'fullDate' }}</p>
```
**Output:** `Today: Monday, February 12, 2025`

### **UpperCasePipe & LowerCasePipe**
```html
<p>Uppercase: {{ 'angular pipes' | uppercase }}</p>
<p>Lowercase: {{ 'ANGULAR PIPES' | lowercase }}</p>
```
**Output:**
```
Uppercase: ANGULAR PIPES
Lowercase: angular pipes
```

### **CurrencyPipe - Formatting Currency**
```html
<p>Price: {{ price | currency:'USD' }}</p>
```
**Output:** `Price: $199.99`

### **DecimalPipe - Formatting Numbers**
```html
<p>Formatted Number: {{ numberValue | number:'1.2-3' }}</p>
```
**Output:** `Formatted Number: 12,345.679`

### **PercentPipe - Displaying Percentages**
```html
<p>Discount: {{ discount | percent }}</p>
```
**Output:** `Discount: 25%`

### **SlicePipe - Extracting Parts of Strings**
```html
<p>Short Text: {{ 'AngularPipes' | slice:0:7 }}</p>
```
**Output:** `Short Text: Angular`

### **AsyncPipe - Handling Promises**
```html
<p>Message: {{ asyncMessage | async }}</p>
```
**Output after 3 seconds:** `Message: Hello from Async Pipe!`

```typescript
asyncMessage = new Promise(resolve => {
  setTimeout(() => resolve('Hello from Async Pipe!'), 3000);
});
```

---

## **2. Creating a Custom Pipe in Angular 18**

If built-in pipes don’t meet your needs, you can create a **custom pipe**.

### **Step 1: Generate a Custom Pipe**
```sh
ng generate pipe reverseString
```

### **Step 2: Implement Custom Logic**
```typescript
import { Pipe, PipeTransform } from '@angular/core';

@Pipe({ name: 'reverseString' })
export class ReverseStringPipe implements PipeTransform {
  transform(value: string): string {
    return value.split('').reverse().join('');
  }
}
```

### **Step 3: Use Custom Pipe in Template**
```html
<p>Original: {{ message }}</p>
<p>Reversed: {{ message | reverseString }}</p>
```
**Output:**
```
Original: Angular Pipes
Reversed: sepiP ralugnA
```

---

## **When to Use Pipes in Angular 18?**
✅ **For Data Formatting** – Dates, numbers, currency, etc.  
✅ **For String Manipulation** – Uppercase, lowercase, reversing text, etc.  
✅ **For Handling Async Data** – Promises and Observables  
✅ **For Improving Readability** – Avoid writing extra logic in components  
