# Replication Steps
In case you want to replicate the steps to do it yourself instead of copying this
## Requirements
- [Node.js](https://nodejs.org/) installed
## Git
- Use [toptal.com/developers/gitignore](https://www.toptal.com/developers/gitignore) to create **.gitignore** file
## Node
- Run `npm init`
## Typescript
- Follow instructions in [typescriptlang.org/download](https://www.typescriptlang.org/download) to install Typescript in the project. Or just run `npm i -D typescript`
- Run `tsc --init` to initialize the project with TypeScript and create the **tsconfig.json** file
- Use the following links to edit the **tsconfig.json** file according to the project needs. [What is a tsconfig.json](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html), [TSConfig Reference](https://www.typescriptlang.org/tsconfig)
- Run `npm i -D @types/node` to install types for node
- In the **tsconfig.json** file uncomment the `outDir` property and set it as `"outDir": "dist"`
- Create a **src** folder in the project root folder
- Create an **index.ts** file inside the **src** folder with the content `console.log('Hello World!')`
- In the **package.json** file:
  - Set the `main` property to `"main": "dist/index.js"`
  - Inside the `scripts` property:
    - Add the property `build` and set it as `"build": "tsc"`
    - Add the property `prestart` and set it as `"prestart": "npm run build"`
    - Change the `start` propety to `"start": "node dist/index.js"`