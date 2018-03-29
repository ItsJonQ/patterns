# Javascript

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
