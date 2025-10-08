<!-- GETTING STARTED -->
## How to Resolve ESLint Errors in a TypeScript Project

When working with TypeScript, ESLint is an essential tool for maintaining clean, consistent, and error-free code. However, setting up ESLint for TypeScript can sometimes lead to errors due to misconfigurations. In this guide, we’ll walk through the steps to configure ESLint for TypeScript and resolve common errors.

### Step 1: Install ESLint Plugins for TypeScript

To enable ESLint to work effectively with TypeScript, you need to install the required plugins and parser. Run the following command:

  ```sh
    npm install @typescript-eslint/parser @typescript-eslint/eslint-plugin --save-dev
  ```
*    ```@typescript-eslint/parser ``` Allows ESLint to parse TypeScript code.
* 	 ```@typescript-eslint/eslint-plugin ``` Provides linting rules specific to TypeScript.

 ### Step 2: Update ESLint Configuration
Modify your .eslintrc.json or .eslintrc.js file to use the TypeScript parser and include the TypeScript plugin. 
Here’s an example .eslintrc.json setup:
```sh
{
   "parser":"@typescript-eslint/parser",
   "parserOptions":{
      "ecmaVersion":2020,
      "sourceType":"module",
      "project":"./tsconfig.json"
   },
   "plugins":[
      "@typescript-eslint"
   ],
   "extends":[
      "eslint:recommended",
      "plugin:@typescript-eslint/recommended"
   ],
   "rules":{
      
   }
}

 ```
*	 ```parser ``` Specifies the TypeScript parser.
*	 ```parserOptions``` Configures the environment and points to the TypeScript configuration (tsconfig.json).
*	 ```plugins ``` Includes the TypeScript-specific ESLint plugin.
*	 ```extends ``` Combines recommended rules from ESLint and ```@typescript-eslint```

### Step 3: Run ESLint
After updating the configuration, run the linting command again to check for errors:
```sh
 npm run lint
```

By following these steps, you should be able to resolve most ESLint errors in your TypeScript project and maintain a clean and consistent codebase.




