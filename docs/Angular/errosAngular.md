# List

## Property '...' has no initializer and is not definitely assigned in the constructor

### Problem

It's because TypeScript 2.7 includes a strict class checking where all the properties should be initialized in the constructor. A workaround is to add the ! as a postfix to the variable name.

### Solution 

On you tsconfig.json

```
"strictPropertyInitialization": false
```

or

```
variable!: any[];
```

[![Generic badge](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/49699067/property-has-no-initializer-and-is-not-definitely-assigned-in-the-construc)

## Cannot import Observable.fromEvent - RXJS

## Solution 1

```
import {fromEvent} from 'rxjs';
fromEvent(this.elementRef.nativeElement, 'keyup')
Observable.fromEvent(this.elementRef.nativeElement, 'keyup')
```

[![Generic badge](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/50355584/cannot-import-observable-fromevent-rxjs)

## Solution 2

```
distinctUntilChanged((obj1, obj2) => JSON.stringify({ obj: obj1 }) === JSON.stringify({ obj: obj2 })
```

[![Generic badge](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/61741276/rxjs-distict-utill-changed-check-deep-objects)

```
distinctUntilChanged(
      (pre: any, curr: any) => JSON.stringify(pre) === JSON.stringify(curr)
    )
```
[![Generic badge](https://aleen42.github.io/badges/src/stackoverflow.svg)](https://stackoverflow.com/questions/68029895/angular-distinctuntilchanged-value-comparison)