# Docdown

Code fast documenting without learning curves...

* Easy fits to your document needing
* No need to know anything other than markdown
* Stay organized and focused in your code
* Adjustable to fit consistence of your work or project
* Very easy to parse or indexing

## Examples

**Javascript**
```Javascript
/*md
  getSomeElement(query) : DomNodeList | null
  * query : jquery query
*/
function getSomeElement(query) {
  return $(query)
}
```
Should render:
> getSomeElement(query) : DomNodeList | null
> * query : jquery query

**PHP**
```PHP

/*md
  test
  A simple class I made
*/
class test {
  /* test::doit(arg) : stuff
    * arg : mixed, can be a number or a string
    * stuff : something you want to be returned
    Maybe you have better examples...
  */
  public static function doit(arg) {
    // Some stuff
  }
}

```

**Lua**

```Lua
--[[md
  someClass:someAction(somearg) : res, err
  * somearg : what you want to pass the function
  * res : something returned on sucess or nil
  * err : message returned only on error
--]]
function someClass:someAction(somearg)
  -- Some stuff
  return res, err
end
```

Yes... these examples are very simplistic, but are intended only to show the simplicity.

## Processing

I'm documenting using this technique, but not developed a processor yet.
Somethings I planning to this processor:

* Parse retrieve blocks from each language multiline comments
* Detect only comments where comment opening, follow a `md` followed by newline
* Comments retrieved can have any size
* First line of each comment rendering as `h3` or `h6` to be easily indexed
* Make processor recurse under directories
