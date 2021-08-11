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

#### Motation
```bash
  ajv validate --strict=false -s ./schema/motation-schema.json -r ./schema/common-schema.json -r ./schema/content-schema.json -d ./examples/motation/example-motation.json
```

#### category 
```bash
  ajv validate --strict=false -s ./schema/category-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-category-motation-dependency.json
```

#### definition
```bash
  ajv validate --strict=false -s ./schema/definition-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-definition-motation-dependency.json
```

#### domain
```bash
  ajv validate --strict=false -s ./schema/domain-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-domain-motation-dependency.json
```

#### folder
```bash
  ajv validate --strict=false -s ./schema/folder-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-folder-motation-dependency.json
```

#### language
```bash
  ajv validate --strict=false -s ./schema/language-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-language-motation-dependency.json
```

#### relationship
```bash
  ajv validate --strict=false -s ./schema/relationship-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-relationship-motation-dependency.json
```

#### tag
```bash
  ajv validate --strict=false -s ./schema/tag-motation-dependency-schema.json -r ./schema/common-schema.json -d ./examples/motation/example-tag-motation-dependency.json
```
