# typescript-journey

## TypeScript Basics

<details>
<summary>Types Basics in TypeScript</summary>

- **`string`**: Represents textual data.
  ```typescript
  let name: string = "John";
  ```

- **`number`**: Represents numeric values.
  ```typescript
  let age: number = 25;
  ```

- **`boolean`**: Represents true or false values.
  ```typescript
  let isActive: boolean = true;
  ```

- **`null`**: Represents the absence of a value.
  ```typescript
  let emptyValue: null = null;
  ```

- **`undefined`**: Represents an uninitialized variable.
  ```typescript
  let notAssigned: undefined = undefined;
  ```

- **`any`**: Allows any type of value (use with caution).
  ```typescript
  let randomValue: any = "Hello";
  randomValue = 42;
  ```

- **`void`**: Represents the absence of a return value in functions.
  ```typescript
  function logMessage(): void {
    console.log("This function returns nothing.");
  }
  ```

- **`never`**: Represents values that never occur (e.g., a function that always throws an error).
  ```typescript
  function throwError(message: string): never {
    throw new Error(message);
  }
  ```

- **`object`**: Represents non-primitive types (e.g., arrays, objects).
  ```typescript
  let person: object = { name: "Alice", age: 30 };
  ```

- **`unknown`**: Represents a value whose type is not known at the time of declaration.
  ```typescript
  let input: unknown = "Hello";
  if (typeof input === "string") {
    console.log(input.toUpperCase());
  }
  ```

</details>