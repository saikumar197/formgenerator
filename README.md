# Angular form schematic

This repository is a basic Schematic implementation to generate Angular Forms using a JSON description

## Getting started

To test this schematic you must follow the steps:

1. Install dependencies on form generator folder

```
cd formgenerator
npm install
npm run build
```

2. By npm linking ,link in your project by folder linking or by package 

```
npm link ../formgenerator/forms
```
3.By`npm pack` command, generates a `.tgz` file which can be installed anywhere in schematics-cli

`npm install ../formgenerator/forms/schematics-forms.tgz`

Now you can proccede creating forms component and testing the generator.

PS: Inside angular-template/jsons folder has some form schemas example to be used.

## Form Generator

This schematic is responsible for generate a form schematic using a pass by JSON, using bootstrap!

```
ng g form path/name-component ./jsons/schema.json
```

or

```
ng g f path/name-component ./jsons/schema.json
```


## How to configure this schematic in another project

1. First you should install dependencies and build the schematic form lib

```
cd form-generator
npm install
npm run build
```

2. You should install the schematic in your project

```
npm link ../formgenerator/forms
```

Inside your angular json in "cli" key you should add:

```
"defaultCollection": "forms"
```

will stay:

```
"cli": {
    "analytics": false,
    "defaultCollection": "forms"
}
```



## Testing

To test locally, install `@angular-devkit/schematics-cli` globally and use the `schematics` command line tool. That tool acts the same as the `generate` command of the Angular CLI, but also has a debug mode.

Check the documentation with

```bash
schematics --help
```

## Unit Testing

`npm run test` will run the unit tests, using Jasmine as a runner and test framework.

## Publishing

To publish, simply do:

```bash
npm run build
npm publish
```

That's it!

## Contribute

Pickup an item on backlog, create an issue and submit the PR.

