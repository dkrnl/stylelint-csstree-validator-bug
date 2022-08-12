# stylelint-csstree-validator-bug

`npm run test` -- bug reproduce command

output
```
> stylelint-csstree-validator-bug@1.0.0 test
> npx stylelint test.css

TypeError: Cannot read properties of null (reading 'match')
    at ~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/test.css:1:2
    at matchSyntax (~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/css-tree/cjs/lexer/Lexer.cjs:82:51)
    at Lexer.matchAtrulePrelude (~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/css-tree/cjs/lexer/Lexer.cjs:289:16)
    at ~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/stylelint-csstree-validator/cjs/index.cjs:123:31
    at ~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/postcss/lib/container.js:119:18
    at ~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/postcss/lib/container.js:55:18
    at Root.each (~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/postcss/lib/container.js:41:16)
    at Root.walk (~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/postcss/lib/container.js:52:17)
    at Root.walkAtRules (~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/postcss/lib/container.js:117:19)
    at ~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/stylelint-csstree-validator/cjs/index.cjs:92:14
    at ~/stylelint-csstree-validator-bug.localhost/stylelint-csstree-validator-bug/node_modules/stylelint/lib/lintPostcssResult.js:113:8

```

`npm i css-tree@2.1 --save-exact` -- this fix command
