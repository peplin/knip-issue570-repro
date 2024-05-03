## Knip issue #570 repro

```
$ npm run knip

> knip
> knip

Analyzing workspace ....
node:internal/modules/cjs/loader:1202
  const err = new Error(message);
              ^

Error: Cannot find module '/Users/peplin/dev/knip-570-repro/app/src/.eslintrc.js'
Require stack:
- /Users/peplin/dev/knip-570-repro/index.js
    at Module._resolveFilename (node:internal/modules/cjs/loader:1202:15)
    at Function.resolve (node:internal/modules/helpers:199:19)
    at Function._resolve [as resolve] (/Users/peplin/dev/knip-570-repro/node_modules/jiti/dist/jiti.js:1:251148)
    at resolve (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/util/require.js:13:48)
    at getDependenciesDeep (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/plugins/eslint/helpers.js:31:50)
    at getDependenciesDeep (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/plugins/eslint/helpers.js:34:34)
    at async Object.resolveConfig (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/plugins/eslint/index.js:12:26)
    at async WorkspaceWorker.findDependenciesByPlugins (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/WorkspaceWorker.js:210:55)
    at async main (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/index.js:106:108)
    at async run (file:///Users/peplin/dev/knip-570-repro/node_modules/knip/dist/cli.js:23:73) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [ '/Users/peplin/dev/knip-570-repro/index.js' ]
}

Node.js v22.0.0
```
