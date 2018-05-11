# Homeless
A collection of reuasble project agnostic typescript packages.

## Development
After cloning this repository run `lerna bootstrap` to install all dependencies

**Add dependencies**
To add a (--dev) dependency to all packages run:
```sh
$ lerna add <module-name>
```

To add dependencies to a specific package run:
```sh
$ lerna add <module-name> --scope=package
```
**Add package**
To add a new package create a new folder inside `/packages` and create a package.json using run:
```sh
$ yarn init
```

## Distribution
After making changes or adding a packages you can update the monorepo with:
```sh
$ lerna publish --skip-npm
```
this wil bump the version and create a tag + commit. Before doing this always run the following in the root folder:
```sh
$ yarn test && yarn build
```

## Usage
To install and use this monorepo's packages add it to your project using
```sh
$ yarn add git+ssh://git@github.com:home-ht/homeless.git
```
and import the package like this:
```typescript
import { isValidPhonenumber } from 'homeless/packages/validator';
```
## Packages

**Validator**
```typescript
const isValidPhonenumber()
default Empty
```
