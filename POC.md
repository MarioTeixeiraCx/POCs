## Update ##
After reanalyzing this case, we concluded this is not a vulnerability because it's usually not exploitable. The memory starts leaking to the point of denying the service if multiple "debug" instances are created by calling the affected function, but this is generally not controllable by attackers. Unless, in a specific use case of the library, a malicious actor could intentionally trigger the specific function to create "debug" instances. However, this would probably require exploiting a different vulnerability in the dependent application or, if chained with another vulnerability, such as prototype pollution.


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
