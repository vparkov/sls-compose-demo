Steps to reproduce.

### 1. File already exists (node_modules) on `sls offline`

`npm run dev` - this create a .build directory withing the /api folder.
Run `npm run dev` a second time to see the error.

```
Error:
Error: EEXIST: file already exists, symlink '/***/fullstack-app/api/node_modules' -> '/***/fullstack-app/api/.build/node_modules'
Error: 
```

### 2. `sls deploy` not working - looking for node_modules in the wrong place

Run `npm run deploy`
```

Error:
Error: ENOENT: no such file or directory, stat '/***/fullstack-app/api/node_modules'
```