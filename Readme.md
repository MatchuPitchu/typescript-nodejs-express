# Node.js and Express with TypeScript

- Node.js isn't capable of parsing and compiling TypeScript -> it treats every file that is executed as JavaScript

## Setup in Visual Studio Code

- `npm init` to initialize package manager and configuration
- `tsc --init` to initialize TS configuration
  - tsconfig.json file setup:
    ```JSON
    "compilerOptions": {
      "target": "es2018",
      "module": "commonjs",
      "moduleResolution": "node", // add this to tell TS how different files and imports work together
      "outDir": "./dist",
      "rootDir": "./src",
      "strict": true,
      "esModuleInterop": true,
      "skipLibCheck": true,
      "forceConsistentCasingInFileNames": true
    }
    ```
- `npm i --save express body-parser` to install Express framework and body parsing middleware to be able to parse incoming request bodies in a middleware before your handlers, available under the `req.body` property.
- `npm i --save-dev nodemon` -> allows to execute file with node.js and watches this file and the folder for changes to restart server in case of changes
