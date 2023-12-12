# C-like languages

The following are ways in which the coding style of some
of these repos written in C-like languages differs from
more popular styles. For an example of a repo that does
follow more common conventions, please see
[RPG Bank](https://github.com/kirkiano/rpg-bank-spring).


## Variable names

Some coding styles recommend spelled-out variable names. For example:
```
public ElephantRepository elephantRepository;
```
This repo uses short variable names, and single-letter ones when
the method itself is short enough.


## Exception names

Some coding styles recommend the suffixing
of `Exception` to the name of an exception, as in `NullPointerException`.
This repo leaves `Exception` off  exception names.


## Curly braces

### Newline before brace

Some coding styles recommend preceding a curly brace with a newline,
as at the beginning of class declarations or method definitions.
This repo favors omitting the newline, thus making the brace the last
character of the declaration. For example
```
class Foo {
    void bar() {
        /* ... */
    }
}
```
An exception arises when the declaration is long enough to
need multiple lines.

### Newline after brace

Some coding styles recommend following an open curly brace with
a newline. This repo usually follows this guideline, but when readability
is not impaired it sometimes favors a pleasing concision.

### One-line branches

When a branch of a conditional consists of a single line, this
style guide permits the omission of both the newline and the
corresponding braces (unless other considerations countervail).
For example:
```
if (condition) short_enough();
else also_short_enough();
```
Likewise for `try`-`catch`-`finally`.

Note that some languages, such as Go, forbid this style, forcing
the above `if`-`else` example to take up at least four lines.
