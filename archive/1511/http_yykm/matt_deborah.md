Assessors: Meeka

path: https://github.com/pindell-matt/http_youknowme

The project will be assessed with the following rubric:

## Overall Functionality

Score: 3

* Have:
  0. Hello World
  1. Diagnostics
  2. Supporting Paths, different counts on hello / total
  3. Supports params

```
4: Application implements all five iterations and at least one extension
3: Application implements four iterations
2: Application implements three iteration
1: Application implements two or fewer iterations
```

## Fundamental Ruby & Style

Score: 3

* Good job on refactoring and avoiding 'god objects'
* Keep an eye out for splitting [these](https://github.com/pindell-matt/http_youknowme/blob/master/lib/http_request.rb#L18) out things like this into named methods. While it's relatively small, it's confusing to scan while reading and understand what's going on!

4: Application demonstrates excellent knowledge of Ruby syntax, style, and refactoring
3: Application shows some effort toward organization but still has 6 or fewer long methods (> 8 lines) and needs some refactoring.
2: Application runs but the code has many long methods (>8 lines) and needs significant refactoring
1: Application generates syntax error or crashes during execution

## Test-Driven Development

Score: 3

* Good effort and work put forward to test!
* Remember to test unhappy or edgecase paths - like `?word=''` or `?word=PIZZA` or `?word=plu`

4: Application is broken into components which are well tested in both isolation and integration
3: Application uses tests to exercise core functionality and some edge cases, but fails to break out component objects/tests.
2: Application uses tests to exercise core functionality but leaves many common edge cases untested.
1: Application does not demonstrate strong use of TDD

## Breaking Logic into Components

Score: 3

* Start thinking about 'endpoints' and logic being separated in those ways. For example, [this 'hello' specific logic](https://github.com/pindell-matt/http_youknowme/blob/master/lib/http_request.rb#L23-L25) is just sitting in the request loop. It will be hard to track down everything if you ever change the logic for what the '/hello' endpoint does or change the '/hello' input itself.

4: Application effectively breaks logical components apart with clear intent and usage
3: Application has multiple components with defined responsibilities but there is some leaking of responsibilities
2: Application has some logical components but divisions of responsibility are inconsistent or unclear and/or there is a "Goddess" object taking too much responsibility
1: Application logic shows poor decomposition with too much logic mashed together
