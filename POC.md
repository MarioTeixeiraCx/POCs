## POC for NPM package `debug`

- Issue [#678](https://github.com/debug-js/debug/issues/678)
- [Repository](https://github.com/debug-js/debug)


### Steps to reproduce:

#### Option 1:
- Run the POC as described in the issue.

#### Option 2:
1. Install a vulnerable version of `debug`:
```npm i debug@4.2.0 pidusage```
2. Run the exploit:
```node exploit.js```
3. Wait until you see "Vulnerable!!!"