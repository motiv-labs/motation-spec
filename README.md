# motation-spec

## Validate Locally (Command Line)

Using this project: https://github.com/ajv-validator/ajv-cli

### Installation in Linux (Ubuntu 20.04)

Install `Node.js` and `npm` from the Ubuntu repository

```bash
  sudo apt update
  sudo apt install nodejs npm
```

Install `ajv-cli`
```bash
  npm install -g ajv-cli
```

Test if tool was successfully installed

```bash
  ajv help
```
#### Troubleshoot:

If you get this error:

```bash
npm ERR! path /usr/local/lib/node_modules
npm ERR! code EACCES
npm ERR! errno -13
npm ERR! syscall access
npm ERR! Error: EACCES: permission denied, access '/usr/local/lib/node_modules'
```

Follow the steps on this specific answer (not the accepted, but this one): https://stackoverflow.com/a/55274930

### Validating JSON with `ajv-cli`

From the project root directory:

```bash
  ajv validate --strict=false -s ./schema/full-definition-schema.json -r ./schema/common-schema.json -r ./schema/definition-content-schema.json -r ./schema/definition-field-schema.json -d ./examples/motationObject/example-definition-full-object.json
```