# Custom Lint Rules


# but why?

* API usage
    * how many ways are there to write bad backbone code?
* Education
* Team code standards
* Code smells
    * for loops?


# but, really, why?

* 200,000 lines of JavaScript
* 70 developers
* developers are new to JavaScript
* plans for growth



# How


# ESLint

> The goal of ESLint is to provide a pluggable linting
> utility for JavaScript.
> While JSHint and JSLint dominate JavaScript linting,
> neither one provides an API for
> plugging in your own rules


* via esprima/MDN Parser API


# Example

Warn on usage of underscore when ES5 methods exist which do the same


* `_.map([], ...)` [ast][astmap1]
* `_([]).map(...)` [ast][astmap2]
* [Rule](https://github.com/ScottWeinstein/eslint-no-underscore/blob/master/rules/no-underscore.js)
* [Test](https://github.com/ScottWeinstein/eslint-no-underscore/blob/master/test/no-underscore.js)

[astmap1]:  http://esprima.org/demo/parse.html?code=_.map(%5B1%5D%2C%20function()%7B%7D)
[astmap2]:  http://esprima.org/demo/parse.html?code=_(%5B1%5D).map(function()%7B%7D)


# Objections



# Is it ready?

Not yet, wait for ESLint 0.6




# References

* https://github.com/eslint/eslint
* https://github.com/ScottWeinstein/eslint-no-underscore
* [@ScottWeinstein](https://twitter.com/ScottWeinstein)
