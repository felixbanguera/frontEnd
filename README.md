# frontEnd
Front End notes, books and Q&amp;A 

The following should be organized, I'll just use the Readme for taking temp notes as I study....

## Typescript overview
...it is a "superset of JavaScript with optional Type cecking"

### Objectives:
#### Add types to JS
- Why: Types help in development, erros can be caught in compilation rather than excution. Types help document the code.
- Types can be implicit (by assigning a value: `var text = 'text';`) or explicit (by defining a variable type: `var text: string = 'text';`)
- Types are structural: so it validates the types structure not the type name/definition, example:
```
interface obj1 {
    x: number,
    y: number
}

interface obj2 {
    x: number,
    y: number
}

var test1: obj1;
var test2: obj2;
test2 = {x: 1, y:2};

test1 = test2;
```

#### Add future functionalities to current JS version
... for example `class` and `=>` arrow function, among other


## Javascript 
Best parctices in JS ensure best practices in TS, although the latest will help enforce that.

### Equality
`==` tries to do type coercion between two variables: `0 == ""` -> `true`
So always use `===` and `!==` except for `null`

### Structural Equality
ALthough it's not common, if thre's the need to compare object structures `===` won't do: `{a:123} === {a:123}` -> `false`
Tip, use the library [deep-equal](https://www.npmjs.com/package/deep-equal)

