# [You don't (may not) need Lodash/Underscore](https://you-dont-need.github.io/You-Dont-Need-Lodash-Underscore/#/)

Lodash and Underscore are great modern JavaScript utility libraries, and they are widely used by Front-end developers. However, when you are targeting modern browsers, you may find out that there are many methods which are already supported natively thanks to ECMAScript5 [ES5] and ECMAScript2015 [ES6]. If you want your project to require fewer dependencies, and you know your target browser clearly, then you may not need Lodash/Underscore.

You are welcome to contribute with more items provided below.

- If you are targeting legacy JavaScript engine with those ES5 methods, you can use [es5-shim](https://github.com/es-shims/es5-shim)
- Please note that, the examples used below are just showing you the native alternative of performing certain tasks. For some functions, Lodash provides you more options than native built-ins. This list is not a 1:1 comparison.
- Please send a PR if you want to add or modify the code. No need to open an issue unless it's something big and you want to discuss.

## Voice of Developers

> [Make use of native JavaScript object and array utilities before going big.](https://twitter.com/codylindley/status/692356631007342593)

> &mdash;Cody Lindley, Author of [jQuery Cookbook](http://shop.oreilly.com/product/9780596159788.do) and [JavaScript Enlightenment](http://shop.oreilly.com/product/0636920027713.do)

 

> [You probably don't need Lodash. Nice List of JavaScript methods which you can use natively.](https://twitter.com/daniellmb/status/692200768556916740)

> &mdash;Daniel Lamb, Computer Scientist, Technical Reviewer of [Secrets of the JavaScript Ninja](https://www.manning.com/books/secrets-of-the-javascript-ninja-second-edition) and [Functional Programming in JavaScript](https://www.manning.com/books/functional-programming-in-javascript)

 

> [I guess not, but I want it.](https://twitter.com/teropa/status/692280179666898944)

> &mdash;Tero Parviainen, Author of [build-your-own-angular](http://teropa.info/build-your-own-angular)

 

> [I'll admit, I've been guilty of overusing #lodash. Excellent resource.](https://twitter.com/therebelrobot/status/692907269512642561)

> &mdash;@therebelrobot, Maker of web things, Facilitator for Node.js/io.js

## ESLint Plugin

If you're using [ESLint](http://eslint.org/), you can install a [plugin](http://eslint.org/docs/user-guide/configuring#using-the-configuration-from-a-plugin) thatwill help you identify places in your codebase where you don't (may not) need Lodash/Underscore.

Install the plugin ...

```sh
npm install --save-dev eslint-plugin-you-dont-need-lodash-underscore
```

... then update your config

```json
"extends" : ["plugin:you-dont-need-lodash-underscore/compatible"],
```

For more information, see [Configuring the ESLint Plugin](configuring.md)

> [!IMPORTANT]
> Note that, while many Lodash methods are null safe (e.g. _.keys, _.entries),
> this is not necessarily the case for their Native equivalent. If null safety is critical for your application, we
> suggest that you take extra precautions [e.g. consider using the native `Object.keys` as `Object.keys(value || {})`].

## Quick Links

**[Array](#array)**

1. [_.chunk](#_chunk)
2. [_.compact](#_compact)
3. [_.concat](#_concat)
4. [_.difference](#_difference)
5. [_.drop](#_drop)
6. [_.dropRight](#_dropRight)
7. [_.fill](#_fill)
8. [_.find](#_find)
9. [_.findIndex](#_findindex)
10. [_.first](#_first)
11. [_.flatten](#_flatten)
12. [_.flattenDeep](#_flattendeep)
13. [_.fromPairs](#_frompairs)
14. [_.head and _.tail](#_head-and-_tail)
15. [_.indexOf](#_indexof)
16. [_.intersection](#_intersection)
17. [_.isArray](#_isarray)
18. [_.isArrayBuffer](#_isarraybuffer)
19. [_.join](#_join)
20. [_.last](#_last)
21. [_.lastIndexOf](#_lastindexof)
22. [_.reverse](#_reverse)
23. [_.slice](#_slice)
24. [_.without](#_without)
25. [_.initial](#_initial)
26. [_.pull](#_pull)
27. [_.unionBy](#_unionBy)

**[Collection*](#collection)**

> [!IMPORTANT]
> Note that most native equivalents are array methods,
> and will not work with objects. If this functionality is needed and no object method is provided,
> then Lodash/Underscore might be the better option. Bear in mind however, that all iterable
> objects can easily be converted to an array by use of the
> [spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax).

1. [_.each](#_each)
2. [_.every](#_every)
3. [_.filter](#_filter)
4. [_.groupBy](#_groupby)
5. [_.includes](#_includes)
6. [_.keyBy](#_keyBy)
7. [_.map](#_map)
8. [_.minBy and _.maxBy](#_minby-and-_maxby)
9. [_.orderBy](#_sortby-and-_orderby)
10. [_.pluck](#_pluck)
11. [_.range](#_range)
12. [_.reduce](#_reduce)
13. [_.reduceRight](#_reduceright)
14. [_.reject](#_reject)
15. [_.size](#_size)
16. [_.some](#_some)
17. [_.sortBy](#_sortby-and-_orderby)
18. [_.uniq](#_uniq)
19. [_.uniqWith](#_uniqWith)

**[Function](#function)**

1. [_.after](#_after)
2. [_.bind](#_bind)
3. [_.debounce](#_debounce)
4. [_.isFunction](#_isFunction)
5. [_.partial](#_partial)
6. [_.throttle](#_throttle)

**[Lang](#lang)**

1. [_.castArray](#_castarray)
2. [.cloneDeep](#_clonedeep)
3. [_.gt](#_gt)
4. [_.gte](#_gte)
5. [_.isDate](#_isdate)
6. [_.isEmpty](#_isempty)
7. [_.isFinite](#_isfinite)
8. [_.isInteger](#_isInteger)
9. [_.isNaN](#_isnan)
10. [_.isNil](#_isnil)
11. [_.isNull](#_isnull)
12. [_.isUndefined](#_isundefined)

**[Object](#object)**

1. [_.assign](#_assign)
2. [_.defaults](#_defaults)
3. [_.extend](#_extend)
4. [_.has](#_has)
5. [_.get](#_get)
6. [_.invert](#_invert)
7. [_.isPlainObject](#_isplainobject)
8. [_.keys](#_keys)
9. [_.mapKeys](#_mapKeys)
10. [_.omit](#_omit)
11. [_.pick](#_pick)
12. [_.pickBy](#_pickby)
13. [_.toPairs](#_topairs)
14. [_.values](#_values)

**[String](#string)**

1. [_.capitalize](#_capitalize)
2. [_.endsWith](#_endsWith)
3. [_.isString](#_isString)
4. [_.lowerFirst](#_lowerFirst)
5. [_.padStart and _.padEnd](#_padstart-and-_padend)
6. [_.repeat](#_repeat)
7. [_.replace](#_replace)
8. [_.split](#_split)
9. [_.startsWith](#_startsWith)
10. [_.template](#_template)
11. [_.toLower](#_tolower)
12. [_.toUpper](#_toupper)
13. [_.trim](#_trim)
14. [_.upperFirst](#_upperFirst)

**[Util](#util)**

1. [_.times](#_times)

**[Number](#number)**

1. [_.clamp](#_clamp)
2. [_.inRange](#_inRange)
3. [_.random](#_random)

## Array

### _.chunk

Creates an array of elements split into groups the length of size.

```js
// Underscore/Lodash
_.chunk(['a', 'b', 'c', 'd'], 2);
// => [['a', 'b'], ['c', 'd']]

_.chunk(['a', 'b', 'c', 'd'], 3);
// => [['a', 'b', 'c'], ['d']]


// Native

const chunk = (input, size) => {
  return input.reduce((arr, item, idx) => {
    return idx % size === 0
      ? [...arr, [item]]
      : [...arr.slice(0, -1), [...arr.slice(-1)[0], item]];
  }, []);
};

chunk(['a', 'b', 'c', 'd'], 2);
// => [['a', 'b'], ['c', 'd']]

chunk(['a', 'b', 'c', 'd'], 3);
// => [['a', 'b', 'c'], ['d']]
```

#### Browser Support for Spread in array literals


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | 8.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.compact

Creates an array with all falsy values removed.

#### Browser Support for `array.prototype.filter`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.concat

Creates a new array concatenating array with any additional arrays and/or values.

#### Browser Support for `Array.prototype.concat()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | 5.5 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.difference

Similar to [without](#_without), but returns the values from array that are not present in the other arrays.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.drop

Creates a slice of array with n elements dropped from the beginning.

#### Browser Support for `Array.prototype.slice()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.dropRight

Creates a slice of array with n elements dropped at the end.

#### Browser Support for `Array.prototype.slice()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.fill

Fills elements of array with value from start up to, but not including, end.

> [!NOTE]
> `fill` is a mutable method in both native and Lodash/Underscore.

#### Browser Support for `Array.prototype.fill()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 31.0 ✔                                                                                                        | ✖                                                                                                                                              | 32.0 ✔                                                                                                  | 8 ✔                                                                                                        |


**[⬆ back to top](#quick-links)**

### _.find

Returns the value of the first element in the array that satisfies the provided testing function. Otherwise undefined is returned.

#### Browser Support for `Array.prototype.find()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 25.0 ✔                                                                                                        | ✖                                                                                                                                              | 32.0 ✔                                                                                                  | 7.1 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.findIndex

Returns the index of the first element in the array that satisfies the provided testing function. Otherwise -1 is returned.

#### Browser Support for `Array.prototype.findIndex()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 25.0 ✔                                                                                                        | ✖                                                                                                                                       | 32.0 ✔                                                                                                  | 7.1 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.first

Returns the first element of an array. Passing n will return the first n elements of the array.

#### Browser Support for `Array.prototype.slice()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


#### Browser Support for `Array.prototype.at()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 92 ✔                                                                                                       | 92 ✔                                                                                                 | 90 ✔                                                                                                          | ✖                                                                                                                                       | 78 ✔                                                                                                    | 15.4 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.flatten

Flattens array a single level deep.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                          | 10.5 ✔                                                                                                  | 4 ✔                                                                                                        |


#### Browser Support for `Array.prototype.flat()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 69 ✔                                                                                                       | 79 ✔                                                                                                 | 62 ✔                                                                                                          | ✖                                                                                                                                       | 56 ✔                                                                                                    | 12 ✔                                                                                                       |


#### Browser Support for `Array.prototype.flatMap()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 69 ✔                                                                                                       | 79 ✔                                                                                                 | 62 ✔                                                                                                          | ✖                                                                                                                                       | 56 ✔                                                                                                    | 12 ✔                                                                                                       |


**[⬆ back to top](#quick-links)**

### _.flattenDeep

Recursively flattens array.

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | ✔                                                                                                    | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | 7.1 ✔                                                                                                      |


#### Browser Support for `Array.prototype.flat()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 69 ✔                                                                                                       | 79 ✔                                                                                                 | 62 ✔                                                                                                          | ✖                                                                                                                                       | 56 ✔                                                                                                    | 12 ✔                                                                                                       |


#### Browser Support for `Array.prototype.flatMap()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 69 ✔                                                                                                       | 79 ✔                                                                                                 | 62 ✔                                                                                                          | ✖                                                                                                                                       | 56 ✔                                                                                                    | 12 ✔                                                                                                       |


**[⬆ back to top](#quick-links)**

### _.fromPairs

Returns an object composed from key-value pairs.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


#### Browser Support for `Object.fromEntries()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 73.0 ✔                                                                                                     | 79.0 ✔                                                                                               | 63.0 ✔                                                                                                        | ✖                                                                                                                                              | 60 ✔                                                                                                    | 12.1 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.head and _.tail

Gets the first element or all but the first element.

#### Browser Support for Spread in array literals


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | 8.0 ✔                                                                                                      |


#### Browser Support for `Array.prototype.at()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 92 ✔                                                                                                       | 92 ✔                                                                                                 | 90 ✔                                                                                                          | ✖                                                                                                                                       | 78 ✔                                                                                                    | 15.4 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.indexOf

Returns the first index at which a given element can be found in the array, or -1 if it is not present.

#### Browser Support for `Array.prototype.indexOf()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                          | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.intersection

Returns an array that is the intersection of all the arrays. Each value in the result is present in each of the arrays.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.takeRight

Creates a slice of array with n elements taken from the end.

> [!IMPORTANT]
> Native slice does not behave entirely the same as the `Lodash` method. See example below to understand why.

#### Browser Support for `Array.prototype.slice()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.isArray

Returns true if given value is an array.

#### Browser Support for `Array.isArray()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 5.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isArrayBuffer

Checks if value is classified as an ArrayBuffer object.

> [!WARNING]
> You will get the wrong result if you get `ArrayBuffer` from another realm.
> [See details](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/instanceof#instanceof_and_multiple_context_e.g._frames_or_windows).

#### Browser Support for `instanceof`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.join

> [!IMPORTANT]
> Not in Underscore.js

Joins a list of elements in an array with a given separator.

#### Browser Support for `Array.prototype.join()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | 5.5 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.last

Returns the last element of an array. Passing n will return the last n elements of the array.

#### Browser Support for `Array.prototype.concat()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | 5.5 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


#### Browser Support for `Array.prototype.at()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 92 ✔                                                                                                       | 92 ✔                                                                                                 | 90 ✔                                                                                                          | ✖                                                                                                                                       | 78 ✔                                                                                                    | 15.4 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.lastIndexOf

Returns the index of the last occurrence of value in the array, or -1 if value is not present.

#### Browser Support for `Array.prototype.lastIndexOf()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.reverse

> [!IMPORTANT]
> Not in Underscore.js

Reverses array so that the first element becomes the last, the second element becomes the second to last, and so on.

Voice from the Lodash author:

> Lodash's `_.reverse` just calls `Array#reverse` and enables composition like `_.map(arrays, _.reverse).`
> It's exposed on _ because previously, like `Underscore`, it was only exposed in the chaining syntax.
> --- [jdalton](https://github.com/cht8687/You-Dont-Need-Lodash-Underscore/commit/22c4bcf2be48dd415d2b073759805562e520b615#)

#### Browser Support for `Array.prototype.reverse()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9 ✔                                                                                                                                     | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.slice

Returns a shallow copy of a portion of an array into a new array object selected from `begin` to `end` (`end` not included)

#### Browser Support for `Array.prototype.slice()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.without

> [!IMPORTANT]
> Not in Underscore.js

Returns an array where matching items are filtered.

#### Browser Support for `Array.prototype.filter()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9 ✔                                                                                                                                     | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.initial

Returns everything but the last entry of the array. Pass n to exclude the last n elements from the result.

#### Browser Support for `Array.prototype.slice()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.pull

Removes all provided values from the given array using strict equality for comparisons, i.e. ===.

#### Browser Support for `Array.prototype.filter()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9 ✔                                                                                                                                            | ✔                                                                                                       | ✔                                                                                                          |


#### Browser Support for `Set.prototype.has()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 38 ✔                                                                                                       | 12 ✔                                                                                                 | 13 ✔                                                                                                          | 11 ✔                                                                                                                                    | 25 ✔                                                                                                    | 8 ✔                                                                                                        |


**[⬆ back to top](#quick-links)**

### _.unionBy

Creates an array of unique values, taking an `iteratee` to compute uniqueness with
(note that to iterate by a key in an object you must use `x => x.key` instead of `key` for the `iteratee`)

#### Browser Support for `Array.prototype.flat()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 69 ✔                                                                                                       | 79 ✔                                                                                                 | 62 ✔                                                                                                          | ✖                                                                                                                                       | 56 ✔                                                                                                    | 12 ✔                                                                                                       |


#### Browser Support for `Array.isArray()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 5.0 ✔                                                                                                      |


#### Browser Support for `Set.prototype.has()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 38 ✔                                                                                                       | 12 ✔                                                                                                 | 13 ✔                                                                                                          | 11 ✔                                                                                                                                    | 25 ✔                                                                                                    | 8 ✔                                                                                                        |


**[⬆ back to top](#quick-links)**

## Collection*

> [!IMPORTANT]
> Most native equivalents are array methods,
> and will not work with objects. If this functionality is needed and no object method is provided,
> then Lodash/Underscore is the better option.

### _.each

Iterates over a list of elements, yielding each in turn to an iteratee function.

#### Browser Support for `Array.prototype.forEach()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


#### Browser Support for `Object.entries().forEach()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 54 ✔                                                                                                       | 14 ✔                                                                                                 | 47 ✔                                                                                                          | ✖                                                                                                                                       | 41 ✔                                                                                                    | 10.1✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.every

Tests whether all elements in the array pass the test implemented by the provided function.

#### Browser Support for `Array.prototype.every()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.filter

Creates a new array with all elements that pass the test implemented by the provided function.

#### Browser Support for `Array.prototype.filter()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9 ✔                                                                                                                                     | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.groupBy

Group items by key.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.includes

Checks if a value is in collection.

#### Browser Support for `Array.prototype.includes`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 47.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 43.0 ✔                                                                                                        | ✖                                                                                                                                       | 34.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


#### Browser Support for `Array.prototype.indexOf`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                          | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.keyBy

> [!WARNING]
> Not in Underscore.js

Creates an object composed of keys generated from the results of running each element of collection through iteratee.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | 12.0 ✔                                                                                               | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.map

Translates all items in an array or object to new array of items.

#### Browser Support for `Object.entries()` and destructuring


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | ✖                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


#### Browser Support for `Array.prototype.map()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.minBy and _.maxBy

Use `Array.prototype.reduce()` for find the maximum or minimum collection item

Extract a functor and use es2015 for better code

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.pluck

`array.map` or `_.map` can also be used to replace `_.pluck`.
Lodash v4.0 removed `_.pluck` in favor of `_.map` with iteratee shorthand.
Details can be found in [Changelog](https://github.com/lodash/lodash/wiki/Changelog)

#### Browser Support for `Array.prototype.map()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.reduce

Applies a function against an accumulator and each value of the array (from left-to-right) to reduce it to a single value.

#### Browser Support for `Array.prototype.reduce()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.range

Creates an array of numbers progressing from start up to.

#### Browser Support for `Array.from()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 32.0 ✔                                                                                                        | ✖                                                                                                                                       | ✔                                                                                                       | 9.0 ✔                                                                                                      |


#### Browser Support for keys and spread in Array literals


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | 7.1 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.reduceRight

This method is like _.reduce except that it iterates over elements of collection from right to left.

#### Browser Support for `Array.prototype.reduceRight()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.reject

The opposite of _.filter; this method returns the elements of collection that predicate does not return truthy for.

#### Browser Support for `Array.prototype.filter()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | 12 ✔                                                                                                 | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 9.5 ✔                                                                                                   | 3.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.sample

Gets a random element from `array`.

#### Browser Support for `Array.prototype.length()` and `Math.random()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.size

Returns the number of values in the collection.

#### Browser Support for `Object.keys()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 12.0 ✔                                                                                                  | 5.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.some

Tests whether any of the elements in the array pass the test implemented by the provided function.

#### Browser Support for `Array.prototype.some()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | ✔ 9.0                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.sortBy and _.orderBy

Sorts an array of object based on an object key provided by a parameter (note this is more limited than Underscore/Lodash).

#### Browser Support for `Array.prototype.concat()` and `Array.prototype.sort()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 1.0 ✔                                                                                                      | ✔                                                                                                    | 1.0 ✔                                                                                                         | 5.5 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.uniq

Produces a duplicate-free version of the array, using === to test object equality.

#### Browser Support for Spread in array literals


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | 8.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

## Function

### _.after

> [!WARNING]
> This is an alternative implementation

Creates a version of the function that will only be run after first being called count times. Useful for grouping asynchronous responses, where you want to be sure that all the async calls have finished, before proceeding.

#### Browser Support for `Array.prototype.forEach()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


 **[⬆ back to top](#quick-links)**

### _.bind

Create a new function that calls *func* with *thisArg* and *args*.

#### Browser Support for `Function.prototype.bind()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 7.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 11.6 ✔                                                                                                  | 5.1 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isFunction

Checks if value is classified as a *Function* object.

```js
// Lodash
_.isFunction(console.log);
// => true

_.isFunction(/abc/);
// => false

// Native
function isFunction(func) {
  return typeof func === "function";
}

isFunction(setTimeout);
// => true

isFunction(123);
// => false
```

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.debounce

Create a new function that calls `func` with `thisArg` and `args`.

#### Browser Support for `debounce`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 7.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 11.6 ✔                                                                                                  | 5.1 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.partial

Create a new function that calls `func` with `args`.

#### Browser Support for Spread


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 46.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | 8.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.throttle

Create a new function that limits calls to `func` to once every given timeframe.

#### Browser Support for `throttle`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | 12.0 ✔                                                                                               | 3.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 4.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

## Lang

### _.castArray

Puts the value into an array of length one if it is not already an array.

```js
// Underscore
console.log(_.castArray(5))
// output: [5]
console.log(_.castArray([2]))
// output: [2]

// Native
function castArray(arr) {
  return Array.isArray(arr) ? arr : [arr]
}
// output: true
console.log(castArray(5));
// output: [5]
console.log(castArray([2]));
// output: [2]
```

#### Browser Support for `Array.isArray()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 5.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.cloneDeep

Creates a deep copy by recursively cloning the value.

```js
// Lodash
var objects = [{ 'a': 1 }, { 'b': 2 }];

var clone = _.cloneDeep(objects);
console.log(clone[0] === objects[0]);
// output: false

// Native
var objects = [{ 'a': 1 }, { 'b': 2 }];

var clone = structuredClone(objects);
console.log(clone[0] === objects[0]);
// output: false
```

#### Browser Support for `structuredClone()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 98.0 ✔                                                                                                     | 98.0 ✔                                                                                               | 94.0 ✔                                                                                                        | ✖                                                                                                                                       | 84.0 ✔                                                                                                  | 15.4 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.isDate

Checks if value is classified as a Date object.

```js
// Lodash
console.log(_.isDate(new Date));
// output: true

// Native
console.log(Object.prototype.toString.call(new Date) === "[object Date]");
// output: true
```

#### Browser Support for `String.prototype.toString.call()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.gt

Checks if value is greater than other.

```js
// Lodash
console.log(_.gt(3, 1))
// output: true

// Native
console.log(3 > 1);
// output: true
```

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.gte

Checks if value is greater than or equal to other.

```js
// Lodash
console.log(_.gte(3, 1))
// output: true

// Native
console.log(3 >= 1);
// output: true
```

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.isEmpty

Checks if value is an empty object or collection.

> [!WARNING]
> The Native version does not support evaluating a Set or a Map

#### Browser Support for `Array.prototype.includes()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 47.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 43.0 ✔                                                                                                        | ✖                                                                                                                                       | 34.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isFinite

Checks if value is a finite primitive number.

#### Browser Support for `Number.isFinite()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 19.0 ✔                                                                                                     | ✔                                                                                                    | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | 15.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isInteger

Checks if value is an integer.

#### Browser Support for `Number.isInteger()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | 12 ✔                                                                                                 | 16.0 ✔                                                                                                        | ✖                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.isPlainObject

Checks if value is a plain object, that is, an object created by the Object constructor or one with a [[Prototype]] of null.

#### Browser Support for `Object.getPrototypeOf()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | 12.0 ✔                                                                                               | 3.5 ✔                                                                                                         | ✖                                                                                                                                       | 12.1 ✔                                                                                                  | 5.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isNaN

Checks if a value is NaN.

MDN:

> In comparison to the global `isNaN()` function, `Number.isNaN()` doesn't suffer the problem of forcefully converting the parameter to a number. This means it is now safe to pass values that would normally convert to `NaN`, but aren't actually the same value as `NaN`. This also means that only values of the type number, that are also `NaN`, return true. [Number.isNaN()](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Number/isNaN)

Voice from the Lodash author:

> Lodash's `_.isNaN` is equiv to ES6 `Number.isNaN` which is different than the global `isNaN`.
> --- [jdalton](https://github.com/cht8687/You-Dont-Need-Lodash-Underscore/commit/b8559a603dccaaa2449b5a68a2d8325cf1fb29cd#)

#### Browser Support for `isNaN`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


#### Browser Support for `Number.isNaN`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 25.0 ✔                                                                                                     | ✔                                                                                                    | 15.0 ✔                                                                                                        | ✖                                                                                                                                       | ✔                                                                                                       | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isNil

> [!WARNING]
> Not in Underscore.js

Checks if value is null or undefined.

```js
// Lodash
console.log(_.isNil(null))
// output: true
console.log(_.isNil(NaN))
// output: false
console.log(_.isNil(undefined))
// output: true

// Native
console.log(null == null);
// output: true
console.log(NaN == null);
// output: false
console.log(undefined == null)
// output: true
```

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.isNull

Checks if value is null.

```js
// Underscore/Lodash
console.log(_.isNull(null))
// output: true
console.log(_.isNull(void 0))
// output: false

// Native
console.log(null === null);
// output: true
console.log(void 0 === null);
// output: false
```

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.isUndefined

Checks if value is undefined.

```js
// Underscore/Lodash
console.log(_.isUndefined(a))
// output: true

// Native
console.log(typeof a === 'undefined');
// output: true
console.log(a === undefined);
// output: true
```

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1 ✔                                                                                                           | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

## Object

### _.assign

The method is used to copy the values of all enumerable own properties from one or more source objects to a target object.

#### Browser Support for `Object.assign()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 34.0 ✔                                                                                                        | ✖                                                                                                                                       | 32.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.defaults

The method is used to apply new values over an object with default values for keys.

#### Browser Support for `Object.assign()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 34.0 ✔                                                                                                        | ✖                                                                                                                                              | 32.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


 **[⬆ back to top](#quick-links)**

### _.extend

The method is used to copy the values of all enumerable own and inherited properties from one or more source objects to a target object.

#### Browser Support for `Object.assign()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 34.0 ✔                                                                                                        | ✖                                                                                                                                       | 32.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.has

Checks if `key` is a direct property of `object`. Key may be a path of a value separated by `.`

#### Browser Support for Object .hasOwnProperty


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | 12 ✔                                                                                                 | ✔                                                                                                             | 5.5 ✔                                                                                                                                   | 5 ✔                                                                                                     | 3 ✔                                                                                                        |


**[⬆ back to top](#quick-links)**

### _.get

Gets the value at path of object.

> [!NOTE]
> If provided path does not exist inside the object js will generate error.

#### Browser Support for Object destructing


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 49.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 41.0 ✔                                                                                                        | ✖                                                                                                                                              | 41.0 ✔                                                                                                  | 8.0 ✔                                                                                                      |


#### Browser Support for optional chaining `?.`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 80.0 ✔                                                                                                     | 80.0 ✔                                                                                               | 74.0 ✔                                                                                                        | ✖                                                                                                                                       | 67.0 ✔                                                                                                  | 13.1 ✔                                                                                                     |


#### Browser Support for nullish coalescing operator `??`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 80.0 ✔                                                                                                     | 80.0 ✔                                                                                               | 72.0 ✔                                                                                                        | ✖                                                                                                                                       | ✖                                                                                                       | 13.1 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.invert

Creates an object composed of the inverted keys and values of object. If object contains duplicate values, subsequent values overwrite property assignments of previous values.

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 4.0 ✔                                                                                                      | ✔                                                                                                    | 2.0 ✔                                                                                                         | 6.0 ✔                                                                                                                                   | 10.0 ✔                                                                                                  | 3.1 ✔                                                                                                      |


#### Browser Support for `Object.entries()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 54.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 47.0 ✔                                                                                                        | ✖                                                                                                                                       | 41.0 ✔                                                                                                  | 10.1 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.keys

Retrieves all the names of the object's own enumerable properties.

#### Browser Support for `Object.keys()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | ✔                                                                                                    | 4.0 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 12.0 ✔                                                                                                  | 5.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.mapKeys

The opposite of _.mapValues; this method creates an object with the same values as object and keys generated by running each own enumerable string keyed property of object thru iteratee. The iteratee is invoked with three arguments: (value, key, object).

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 4.0 ✔                                                                                                      | ✔                                                                                                    | 2.0 ✔                                                                                                         | 6.0 ✔                                                                                                                                          | 10.0 ✔                                                                                                  | 3.1 ✔                                                                                                      |


#### Browser Support for `Object.entries()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 54.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 47.0 ✔                                                                                                        | ✖                                                                                                                                       | 41.0 ✔                                                                                                  | 10.1 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.omit

Returns a copy of the object, filtered to omit the keys specified.

#### Browser Support for Spread in object literals


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 60.0 ✔                                                                                                     | 79 ✔                                                                                                 | 55.0 ✔                                                                                                        | ✖                                                                                                                                       | 37.0 ✔                                                                                                  | ✖                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.pick

Creates an object composed of the object properties predicate returns truthy for.

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 38.0 ✔                                                                                                     | ✔                                                                                                    | 13.0 ✔                                                                                                        | 12.0 ✔                                                                                                                                  | 25.0 ✔                                                                                                  | 7.1 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.pickBy

Creates an object composed of the object properties predicate returns truthy for.

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | 6.0 ✔                                                                                                                                   | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.toPairs

Retrieves all the given object's own enumerable property `[ key, value ]` pairs.

#### Browser Support for `Object.entries()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 54.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 47.0 ✔                                                                                                        | ✖                                                                                                                                       | 41.0 ✔                                                                                                  | 10.1 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.values

Retrieves all the given object's own enumerable property values.

#### Browser Support for `Object.values()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 54.0 ✔                                                                                                     | 14.0 ✔                                                                                               | 47.0 ✔                                                                                                        | ✖                                                                                                                                       | 41.0 ✔                                                                                                  | 10.1 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

## String

### _.capitalize

> [!WARNING]
> Not in Underscore.js

Converts the first character of string to upper case and the remaining to lower case.

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.endsWith

> [!WARNING]
> Not in Underscore.js

Checks if string ends with the given target string.

#### Browser Support for `String.prototype.endsWith()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 41.0 ✔                                                                                                     | ✔                                                                                                    | 17.0 ✔                                                                                                        | ✖                                                                                                                                       | 28.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.isString

Checks if value is classified as a String primitive or object.

#### Browser Support


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.lowerFirst

> [!WARNING]
> Not in Underscore.js

Converts the first character of string to lower case.


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.padStart and _.padEnd

> [!WARNING]
> Not in Underscore.js

Pads the current string with another string (multiple times, if needed) until the resulting string reaches the given length.

#### Browser Support for `String.prototype.padStart()` and `String.prototype.padEnd()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 57.0 ✔                                                                                                     | 15.0 ✔                                                                                               | 48.0 ✔                                                                                                        | ✖                                                                                                                                       | 44.0 ✔                                                                                                  | 10.0 ✔                                                                                                     |


**[⬆ back to top](#quick-links)**

### _.repeat

> [!WARNING]
> Not in Underscore.js

Repeats the given string n times.

#### Browser Support for `String.prototype.repeat()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 41.0 ✔                                                                                                     | ✔                                                                                                    | 24.0 ✔                                                                                                        | ✖                                                                                                                                              | 28.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.replace

Returns a new string with some or all matches of a `pattern` replaced by a `replacement`.

#### Browser Support for `String.prototype.replace()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.split

> [!WARNING]
> Not in Underscore.js

Splits string by separator.

#### Browser Support for `String.prototype.split()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.startsWith

> [!WARNING]
> Not in Underscore.js

Checks if string starts with the given target string.

#### Browser Support for `String.prototype.startsWith()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 41.0 ✔                                                                                                     | ✔                                                                                                    | 17.0 ✔                                                                                                        | ✖                                                                                                                                       | 28.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.template

> [!NOTE]
> This is an alternative implementation. Native template literals not escape html.

Create a template function.

#### Browser Support for String (template) literals


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 41.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 34.0 ✔                                                                                                        | ✖                                                                                                                                       | 28.0 ✔                                                                                                  | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.toLower

> [!WARNING]
> Not in Underscore.js

Lowercases a given string.

#### Browser Support for `String.prototype.toLowerCase()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.toUpper

> [!WARNING]
> Not in Underscore.js

Uppercases a given string.

#### Browser Support for `String.prototype.toUpperCase()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | 1.0 ✔                                                                                                         | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.trim

> [!WARNING]
> Not in Underscore.js

Removes the leading and trailing whitespace characters from a string.

#### Browser Support for `String.prototype.trim()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 5.0 ✔                                                                                                      | ✔                                                                                                    | 3.5 ✔                                                                                                         | 9.0 ✔                                                                                                                                   | 10.5 ✔                                                                                                  | 5.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

### _.upperFirst

> [!WARNING]
> Not in Underscore.js

Uppercases the first letter of a given string.


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

## Reference

- [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference)
- [Underscore.js](http://underscorejs.org)
- [Lodash.js](https://lodash.com/docs)

**[⬆ back to top](#quick-links)**

### _.uniqWith

Similar to `_.uniq` except that it accepts comparator which is invoked to compare elements of array. The order of result values is determined by the order they occur in the array.

### Browser Support for `Array.prototype.filter()` and `Array.prototype.findIndex()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | 12.0 ✔                                                                                               | 25.0 ✔                                                                                                        | ✖                                                                                                                                       | 32.0 ✔                                                                                                  | 8.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

## Util

### _.times

Invokes the iteratee n times, returning an array of the results of each invocation.

#### Browser Support for `Array.from()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| 45.0 ✔                                                                                                     | ✔                                                                                                    | 32.0 ✔                                                                                                        | ✖                                                                                                                                       | ✔                                                                                                       | 9.0 ✔                                                                                                      |


**[⬆ back to top](#quick-links)**

## Number

### _.clamp

Clamps number within the inclusive lower and upper bounds.

```js
// Lodash
_.clamp(-10, -5, 5);
// => -5

_.clamp(10, -5, 5);
// => 5

_.clamp(10, -5);
// => -5

_.clamp(10, 99);
// => 10

// Native
const clamp = (number, boundOne, boundTwo) => {
  if (!boundTwo) {
    return Math.max(number, boundOne) === boundOne ? number : boundOne;
  } else if (Math.min(number, boundOne) === number) {
    return boundOne;
  } else if (Math.max(number, boundTwo) === number) {
    return boundTwo;
  }
  return number;
};

clamp(-10, -5, 5);
// => -5

clamp(10, -5, 5);
// => 5

clamp(10, -5);
// => -5

clamp(10, 99);
// => 10
```

#### Browser Support for `Math.min() and Math.max()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.inRange

Checks if n is between start and up to, but not including, end. If end is not specified, it's set to start with start then set to 0. If start is greater than end the params are swapped to support negative ranges.

#### Browser Support for `Math.min() and Math.max()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) | ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                       | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

### _.random

Produces a random number between the inclusive lower and upper bounds. If only one argument is provided a number between 0 and the given number is returned. If floating is true, or either lower or upper are floats, a floating-point number is returned instead of an integer.

#### Browser Support for `Math.random()`


|  ![Chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png) |  ![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png) |  ![Firefox](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png) |  ![IE](https://raw.githubusercontent.com/alrra/browser-logos/master/src/archive/internet-explorer_9-11/internet-explorer_9-11_48x48.png) |  ![Opera](https://raw.githubusercontent.com/alrra/browser-logos/master/src/opera/opera_48x48.png) |  ![Safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png) |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| ✔                                                                                                          | ✔                                                                                                    | ✔                                                                                                             | ✔                                                                                                                                              | ✔                                                                                                       | ✔                                                                                                          |


**[⬆ back to top](#quick-links)**

## Inspired by:

- [You-Dont-Need-jQuery](https://github.com/oneuijs/You-Dont-Need-jQuery)
- [Rui's blog](http://ktei.github.io/2016/01/07/some-general-js-tips-1.html)

## License

MIT