# Javascript

## Arrays

### Mutation-free modification

If mutation is a concern, before doing something, anything, to an array, clone it by using `...spread`:

```js
const newToys = [...oldToys].filter(toy => toy.name !== 'lotsOHugginBear')
```


---


## Boolean

### Double Bang

Use `!!` if you're type checking and require either `true` or `false`.

```js
/**
 * Without
 */
buzz.isACowboy
// undefined

/**
 * With
 */
!!buzz.isACowboy
// false
```


---


## Conditional

### Stacking statements

Inspired by patterns from languages like [Reasons](https://reasonml.github.io/), stacking statements within `if` conditions makes it easier to write and read (especially if it's super complex)

```js
if (
  wasInToyStory(buzz, [1, 2, 3])
  || encountered(buzz, 'Sid')
) {
  return youveGotAFriendInMe()
}
```

This applies to nested conditionals as well!

```js
if (
  isAToy(buzz)
  && buzz.belongsTo === 'Andy'
  && (
      wasInToyStory(buzz, [1, 2, 3])
      || encountered(buzz, 'Sid')
      || friendsWith(buzz, 'Woody')
    )
) {
  return youveGotAFriendInMe()
}
```


---


## Import

### Custom name

When doing an `import`, you can assign the `default` `export` of a file to whatever variable you'd like.

```js
import toy from '../andy/toyChest'
```

If you need to import the `default` with other things from a single file, you can assign a custom name using `as`:

```js
import {
  default as toy
  woody,
  buzz,
  jessie,
  bullseye
} from '../andy/toyChest'
```

You can, of course, customize the non-default things as well:

```js
import {
  default as toy
  woody,
  buzz as spaceRanger,
  jessie,
  bullseye
} from '../andy/toyChest'
```
