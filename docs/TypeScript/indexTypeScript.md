# TypeScript

Last update : 21/10/2021

[![TypeScript](https://badges.aleen42.com/src/typescript.svg)](https://www.typescriptlang.org/docs/handbook/intro.html)

## Access a property in Objects array

If valid type (use Dot notation):

```
obj.name
```

In typeScript, the error *Property do not exist* seems, prevent accidentatlly setting or getting non-existent properties on  an object.

If not valid type (use Bracket notation):

```
obj['name']
```

[![StackOverflow](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/44147937/property-does-not-exist-on-type-never)
[![StackOverflow](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://www.typescriptlang.org/docs/handbook/intro.html)

## Sort array of Objects

### Ascending

```
arrayOfObjects.sort((a, b) => (a.propertyToSortBy < b.propertyToSortBy ? -1 : 1));
```

### Descending

```
arrayOfObjects.sort((a, b) => (a.propertyToSortBy > b.propertyToSortBy ? -1 : 1));
```

### Ascending

```
testsSortedByNome = tests.sort((a, b) => (a.nome < b.nome ? -1 : 1));
testsSortedByCognome = tests.sort((a, b) => (a.cognome < b.cognome ? -1 : 1));
```

### Descending

```
testsSortedByNome = tests.sort((a, b) => (a.nome > b.nome ? -1 : 1));
testsSortedByCognome = tests.sort((a, b) => (a.cognome > b.cognome ? -1 : 1));
```

[![StackOverflow](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/43311121/sort-an-array-of-objects-in-typescript)

## Sources

* [TypeScript-Offical-Doc](https://www.typescriptlang.org/docs/handbook/intro.html)
* [TypeScript-Offical-Doc](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Operators/Property_Accessors)
