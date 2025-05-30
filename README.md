# typescript-journey

## How to Run TypeScript Code 

  <details>
  <summary> Without `tsconfig.json`</summary>

  If you don't have a `tsconfig.json` file set up, you can follow these steps to compile and run your TypeScript code:

  1. Open PowerShell and navigate to your project directory:
    ```powershell
    PS D:\typescript-journey>
    ```

  2. Temporarily bypass the execution policy (if required):
    ```powershell
    PS D:\typescript-journey> Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

  3. Compile your TypeScript file (e.g., `index.ts`) to JavaScript:
    ```powershell
    PS D:\typescript-journey> tsc index.ts
    ```

  4. Run the generated JavaScript file using Node.js:
    ```powershell
    PS D:\typescript-journey> node index.js
    ```

  ### Setting Up `tsconfig.json`

  To simplify the process and enable advanced TypeScript features, you can create a `tsconfig.json` file in your project directory. Run the following command to generate a default configuration file:

  ```powershell
  PS D:\typescript-journey> tsc --init
  ```

  This will create a `tsconfig.json` file with default settings. You can customize it as needed for your project.

  </details>
  <details>
  <summary>With `tsconfig.json` </summary>

  Once you have created a `tsconfig.json` file, you can configure it to streamline your TypeScript workflow:

  1. Initialize the `tsconfig.json` file (if not already created):
    ```powershell
    PS D:\typescript-journey> tsc --init
    ```

  2. Open the `tsconfig.json` file and set the following options:
    ```json
    {
      "compilerOptions": {
       "rootDir": "./src",
       "outDir": "./dist"
      }
    }
    ```

    - `rootDir`: Specifies the root directory of your TypeScript files.
    - `outDir`: Specifies the output directory for the compiled JavaScript files.

  3. Compile your TypeScript files by running:
    ```powershell
    PS D:\typescript-journey> tsc
    ```

  4. Alternatively, use the `--watch` flag to automatically recompile on file changes:
    ```powershell
    PS D:\typescript-journey> tsc --watch
    ```

  5. In a new terminal, run the compiled JavaScript file using Node.js:
    ```powershell
    PS D:\typescript-journey> node ./dist/index.js
    ```

  </details>

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