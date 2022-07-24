# ts magic

## merge 2 objects
```js
// const x = {hello: 1};
// const y = {hi: 2}
// const z = extend(x, y);

// z.hello
// z.hi
export function extend<T, U>(first: T, second: U): T & U {
    let result = <T & U>{};
    for (let id in first) {
        (<any>result)[id] = (<any>first)[id];
    }
    for (let id in second) {
        (<any>result)[id] = (<any>second)[id];
    }
    return result;
}
```
