# babel_test

## npm run babel -> working
```bash
 > npx babel "*/src" --out-dir ../webapp --source-maps true --extensions ".ts" --copy-files --include-dotfiles --relative --verbose

subFolder1\src\test1.ts -> subFolder1\webapp\test1.js
subFolder2\src\test2.ts -> subFolder2\webapp\test2.js
Successfully compiled 2 files with Babel (444ms).
```

## npm run babelWatch
### Initial compilation working
```bash
npx babel "*/src" --out-dir ../webapp --source-maps true --extensions ".ts" --copy-files --include-dotfiles --relative --watch --verbose

subFolder1\src\test1.ts -> subFolder1\webapp\test1.js
subFolder2\src\test2.ts -> subFolder2\webapp\test2.js
Successfully compiled 2 files with Babel (576ms).
```


### After editing 1 file (test*.ts) it gets compiled to different directories (input and output directory)

```bash
subFolder1\src\test1.ts -> subFolder1\webapp\test1.js
subFolder1\src\test1.ts -> subFolder1\src\test1.js
```

## Use npm run resetFiles to reset to initial stricture