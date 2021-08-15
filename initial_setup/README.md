# Learning Node Project

## Initial Setup

**Create Project**
```
❯ mkdir yarn-node-ts-test
❯ cd yarn-node-ts-test
```

**Initialize the project**
```
❯ yarn init

yarn init v1.22.10
question name (yarn-node-ts-test): 
question version (1.0.0): 0.0.1
question description: Yarn Node Typescript Learn Project
question entry point (index.js): src/app.ts
question repository url: git@github.com:git@github.com:carlosjmviana/node-typescript-learn.git
question author: Carlos Viana
question license (MIT): 
question private: 
success Saved package.json
✨  Done in 651.23s.
```

**Install Dependencies**

Install Node types and typescript
```
❯ yarn add @types/node typescript

yarn add v1.22.10
info No lockfile found.
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...
success Saved lockfile.
success Saved 2 new dependencies.
info Direct dependencies
├─ @types/node@16.4.13
└─ typescript@4.3.5
info All dependencies
├─ @types/node@16.4.13
└─ typescript@4.3.5
✨  Done in 4.67s.
```

Install _ts-node_

The Overview of _ts-node_ in [npmjs.com](https://github.com/actions/setup-node):

> _ts-node is a TypeScript execution engine and REPL for Node.js._
> 
> _It JIT transforms TypeScript into JavaScript, enabling you to directly execute TypeScript on Node.js without precompiling. This is accomplished by hooking node's module loading APIs, enabling it to be used seamlessly alongside other Node.js tools and libraries._
```
❯ yarn add -D ts-node

yarn add v1.22.10
[1/4] 🔍  Resolving packages...
[2/4] 🚚  Fetching packages...
[3/4] 🔗  Linking dependencies...
[4/4] 🔨  Building fresh packages...
success Saved lockfile.
success Saved 13 new dependencies.
info Direct dependencies
└─ ts-node@10.1.0
info All dependencies
├─ @tsconfig/node10@1.0.8
├─ @tsconfig/node12@1.0.9
├─ @tsconfig/node14@1.0.1
├─ @tsconfig/node16@1.0.2
├─ arg@4.1.3
├─ buffer-from@1.1.2
├─ create-require@1.1.1
├─ diff@4.0.2
├─ make-error@1.3.6
├─ source-map-support@0.5.19
├─ source-map@0.6.1
├─ ts-node@10.1.0
└─ yn@3.1.1
✨  Done in 2.99s.
```

**Creating tsconfig.json**
tsconfig.json file is create to configure the typescript compiler (tsc) and typescript engine (ts-node) to compile typescript to javascript.

```
❯ yarn tsc --init --rootDir src --outDir ./build --esModuleInterop --lib ES2019 --module commonjs --noImplicitAny true
yarn run v1.22.10

$ ~/yarn-node-ts-test/node_modules/.bin/tsc --init --rootDir src --outDir ./build --esModuleInterop --lib ES2019 --module commonjs --noImplicitAny true
message TS6071: Successfully created a tsconfig.json file.
✨  Done in 0.80s.
```

**Create Hello World Files**
```
❯ mkdir src
❯ echo "console.log('Hello World')" > src/app.ts
```

**Compile**

The _tsc_ yarn command compile *.ts files and convert to javascript with output to _build_ directory.

```
❯ yarn tsc

yarn run v1.22.10
$ ~/yarn-node-ts-test/node_modules/.bin/tsc
✨  Done in 2.17s.
```

**Run**

_With node command_
```
❯ node ./build/app.js

Hello World
````

_Using development mode_
```
❯ yarn ts-node ./src/app.ts

yarn run v1.22.10
$ ~/yarn-node-ts-test/node_modules/.bin/ts-node ./src/app.ts
Hello World
✨  Done in 2.61s.
```

## References

* [Alex Losikov - Project Initial Setup](https://losikov.medium.com/part-1-project-initial-setup-typescript-node-js-31ba3aa7fbf1)