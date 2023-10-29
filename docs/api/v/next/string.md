#![](../images/luxe-dark.svg){width="96em"}

# `luxe` API (`2023.10.1`)  


---

## `luxe: string` module

- [Loc](#loc)   
- [Str](#str)   

---

### Loc
`:::js import "luxe: string" for Loc`
> Interface for the localisation system.
> 
> Each translation always exists in a space and in a language.
> Spaces are contexts, so you might want different spaces for dialogue/menus/icons. Or you can leave everything in the default "game" translation space.
> 
> Unless specified otherwise, the system will fetch the string from the currently active language if possible, if its not available there it will fall back to the set primary language. If the key isn't registered for that either, "MISSING.STRING" will be returned.
> 
> By default there is no active active language set and the primary language is "en".
> 
> ```js
>     //by default language is not set and primary language is `en` with no registered strings
>     Log.print(Strings.get(Loc.get_language())) //null
>     Log.print(Strings.get(Loc.get_primary())) //en
>     Loc.set_language("en")
>     Log.print(Loc.get("start_game")) //MISSING.STRING
> 
>     //as soon as we add a line, we can query it
>     Loc.add("en", Loc.default_space, "start_game", "Start Game!")
>     Log.print(Loc.get("start_game")) //Start Game!
> 
>     //if we query a word in a language where that translation doesnt exist yet (like toki pona here), it falls back to the primary language
>     Log.print(Loc.get("tp", Loc.default_space, "start_game")) //Start Game!
> 
>     //but as soon as it is registered, the translation in the respective language is returned
>     Loc.add("tp", Loc.default_space, "start_game", "o open e musi!")
>     Log.print(Loc.get("tp", Loc.default_space, "start_game")) //o open e musi!
>         
>     //same when we set the current language and use the shorthand get
>     Loc.set_language("tp")
>     Log.print(Loc.get("start_game")) //o open e musi!
> ```

- [default_space](#Loc.default_space)
- [missing_string](#Loc.missing_string)
- [set_primary](#Loc.set_primary)(**language**: `String`)
- [get_primary](#Loc.get_primary)()
- [set_language](#Loc.set_language)(**language**: `String`)
- [get_language](#Loc.get_language)()
- [add_language](#Loc.add_language+2)(**language**: `String`, **plural_form**: `String`)
- [add](#Loc.add+4)(**language**: `String`, **space**: `String`, **key**: `String`, **string**: `String`)
- [add_plural](#Loc.add_plural+4)(**language**: `String`, **space**: `String`, **key**: `String`, **strings**: `List`)
- [get](#Loc.get+3)(**language**: `String`, **space**: `String`, **key**: `String`)
- [has](#Loc.has+3)(**language**: `String`, **space**: `String`, **key**: `String`)
- [get_plural](#Loc.get_plural+4)(**language**: `String`, **space**: `String`, **key**: `String`, **count**: `Num`)
- [get](#Loc.get+2)(**space**: `String`, **key**: `String`)
- [get](#Loc.get)(**key**: `String`)
- [has](#Loc.has)(**key**: `String`)

<hr/>
<endpoint module="luxe: string" class="Loc" signature="default_space"></endpoint>
<signature id="Loc.default_space">Loc.default_space
<a class="headerlink" href="#Loc.default_space" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The default space for localisations, \"game\".   

<endpoint module="luxe: string" class="Loc" signature="missing_string"></endpoint>
<signature id="Loc.missing_string">Loc.missing_string
<a class="headerlink" href="#Loc.missing_string" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> The missing string fallback for the engine, typically \"MISSING.STRING\".   

<endpoint module="luxe: string" class="Loc" signature="set_primary(language : String)"></endpoint>
<signature id="Loc.set_primary">Loc.set_primary(**language**: `String`)
<a class="headerlink" href="#Loc.set_primary" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the primary language that is used as fallback if a key can't be found in another language.   

<endpoint module="luxe: string" class="Loc" signature="get_primary()"></endpoint>
<signature id="Loc.get_primary">Loc.get_primary()
<a class="headerlink" href="#Loc.get_primary" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get the primary language.   

<endpoint module="luxe: string" class="Loc" signature="set_language(language : String)"></endpoint>
<signature id="Loc.set_language">Loc.set_language(**language**: `String`)
<a class="headerlink" href="#Loc.set_language" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Set the current language that strings are gotten for unless specified otherwise.   

<endpoint module="luxe: string" class="Loc" signature="get_language()"></endpoint>
<signature id="Loc.get_language">Loc.get_language()
<a class="headerlink" href="#Loc.get_language" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Get the current language.   

<endpoint module="luxe: string" class="Loc" signature="add_language(language : String, plural_form : String)"></endpoint>
<signature id="Loc.add_language+2">Loc.add_language(**language**: `String`, **plural_form**: `String`)
<a class="headerlink" href="#Loc.add_language+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js unknown`
> Add a language with the given `id` and `plural_form` expression string (just the expression part, not the whole header).   

<endpoint module="luxe: string" class="Loc" signature="add(language : String, space : String, key : String, string : String)"></endpoint>
<signature id="Loc.add+4">Loc.add(**language**: `String`, **space**: `String`, **key**: `String`, **string**: `String`)
<a class="headerlink" href="#Loc.add+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Add a string to the localisation system.   

<endpoint module="luxe: string" class="Loc" signature="add_plural(language : String, space : String, key : String, strings : List)"></endpoint>
<signature id="Loc.add_plural+4">Loc.add_plural(**language**: `String`, **space**: `String`, **key**: `String`, **strings**: `List`)
<a class="headerlink" href="#Loc.add_plural+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js None`
> Add a plural string to the localisation system.   

<endpoint module="luxe: string" class="Loc" signature="get(language : String, space : String, key : String)"></endpoint>
<signature id="Loc.get+3">Loc.get(**language**: `String`, **space**: `String`, **key**: `String`)
<a class="headerlink" href="#Loc.get+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string for a key (or fallback in primary language) from the localisation system for a specific language/space.   

<endpoint module="luxe: string" class="Loc" signature="has(language : String, space : String, key : String)"></endpoint>
<signature id="Loc.has+3">Loc.has(**language**: `String`, **space**: `String`, **key**: `String`)
<a class="headerlink" href="#Loc.has+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check if the string for a key exists in the localisation system for a specific language/space.   

<endpoint module="luxe: string" class="Loc" signature="get_plural(language : String, space : String, key : String, count : Num)"></endpoint>
<signature id="Loc.get_plural+4">Loc.get_plural(**language**: `String`, **space**: `String`, **key**: `String`, **count**: `Num`)
<a class="headerlink" href="#Loc.get_plural+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string for a key from the localisation system for a specific language/space, with the plural count.   

<endpoint module="luxe: string" class="Loc" signature="get(space : String, key : String)"></endpoint>
<signature id="Loc.get+2">Loc.get(**space**: `String`, **key**: `String`)
<a class="headerlink" href="#Loc.get+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string for a key (or fallback in primary language) from the localisation system in the current language and in a specific space.   

<endpoint module="luxe: string" class="Loc" signature="get(key : String)"></endpoint>
<signature id="Loc.get">Loc.get(**key**: `String`)
<a class="headerlink" href="#Loc.get" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string for a key (or fallback in primary language) from the localisation system in the current language and in the default space.   

<endpoint module="luxe: string" class="Loc" signature="has(key : String)"></endpoint>
<signature id="Loc.has">Loc.has(**key**: `String`)
<a class="headerlink" href="#Loc.has" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Check if the string for a key exists in the localisation system for the current language and default space   

### Str
`:::js import "luxe: string" for Str`
> Utility class for String functions.

- [split_lines](#Str.split_lines)(**string**: `String`)
- [split](#Str.split+2)(**string**: `String`, **delim**: `String`)
- [indent_strip](#Str.indent_strip)(**string**: `String`)
- [indent](#Str.indent)(**string**: `String`)
- [trim](#Str.trim)(**string**: `String`)
- [compare](#Str.compare+2)(**a**: `String`, **b**: `String`)
- [replace](#Str.replace+3)(**string**: `String`, **sub**: `String`, **repl**: `String`)
- [is_alphanumeric](#Str.is_alphanumeric)(**str**: `String`)
- [vec](#Str.vec)(**value**: `Vec`)
- [vec](#Str.vec+2)(**value**: `Vec`, **precision**: `Num`)
- [vec](#Str.vec+3)(**value**: `Vec`, **precision**: `Num`, **sep**: `String`)
- [fixed](#Str.fixed+2)(**number**: `Num`, **precision**: `Num`)
- [fixed](#Str.fixed)(**number**: `Num`)
- [fixed](#Str.fixed+3)(**number**: `Num`, **precision**: `Num`, **padded**: `Bool`)
- [hex](#Str.hex)(**number**: `Num`)
- [binary](#Str.binary)(**number**: `Num`)
- [binary](#Str.binary+2)(**number**: `Num`, **bit_width**: `Num`)
- [path_is_absolute](#Str.path_is_absolute)(**path**: `String`)
- [path_directory](#Str.path_directory)(**path**: `String`)
- [path_filename](#Str.path_filename)(**path**: `String`)
- [path_extension](#Str.path_extension)(**path**: `String`)
- [path_extensionless](#Str.path_extensionless)(**path**: `String`)
- [bytes_formatted](#Str.bytes_formatted)(**byte_count**: `Num`)
- [bytes_formatted](#Str.bytes_formatted+2)(**byte_count**: `Num`, **precision**: `Num`)
- [upper](#Str.upper)(**string**: `String`)
- [lower](#Str.lower)(**string**: `String`)
- [wrap](#Str.wrap+2)(**string**: `String`, **column**: `Num`)
- [path](#Str.path)(**path**: `String`)
- [strip_markup](#Str.strip_markup)(**string**: `String`)
- [format](#Str.format+2)(**string**: `String`, **arg0**: `Any`)
- [format](#Str.format+3)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`)
- [format](#Str.format+4)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`)
- [format](#Str.format+5)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`)
- [format](#Str.format+6)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`)
- [format](#Str.format+7)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`)
- [format](#Str.format+8)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`)
- [format](#Str.format+9)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`)
- [format](#Str.format+10)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`)
- [format](#Str.format+11)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`)
- [format](#Str.format+12)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`)
- [format](#Str.format+13)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`)
- [format](#Str.format+14)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`, **arg12**: `Any`)
- [format](#Str.format+15)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`, **arg12**: `Any`, **arg13**: `Any`)
- [format](#Str.format+16)(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`, **arg12**: `Any`, **arg13**: `Any`, **arg14**: `Any`)
- [format_list](#Str.format_list+2)(**string**: `String`, **args**: `List`)

<hr/>
<endpoint module="luxe: string" class="Str" signature="split_lines(string : String)"></endpoint>
<signature id="Str.split_lines">Str.split_lines(**string**: `String`)
<a class="headerlink" href="#Str.split_lines" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> Split a string into its lines.
> Returns `[""]` for empty strings.
> 
> ```js
>     var multiline_string = \"\"\"
>     leaf
>     tree
>     fruit
>     mushroom
>     \"\"\"
> 
>     var split_string = Str.split_lines(multiline_string)
>     Log.print(split_string) //[leaf, tree, fruit, mushroom]
> ```   

<endpoint module="luxe: string" class="Str" signature="split(string : String, delim : String)"></endpoint>
<signature id="Str.split+2">Str.split(**string**: `String`, **delim**: `String`)
<a class="headerlink" href="#Str.split+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js List`
> **Deprecated** use `string.split(delim)`
> Split a string at every occurance of an delimiter.
> 
> ```js
>     var input = "Owl eats Squirrel eats Nuts"
>     var split_string = Str.split(input, " eats ")
>     Log.print(split_string) //[Owl, Squirrel, Nuts]
> ```   

<endpoint module="luxe: string" class="Str" signature="indent_strip(string : String)"></endpoint>
<signature id="Str.indent_strip">Str.indent_strip(**string**: `String`)
<a class="headerlink" href="#Str.indent_strip" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Removes indentation from the first line of a string, and the same amount from subsequent lines if any. 
> Lines with shorter indentation than the first line are skipped.
> 
> ```js
>     var input = \"\"\"
>         Sparrow
>         Pidgeon
>             Crow
>     \"\"\"
>     var unindented = Str.indent_strip(input)
>     Log.print(unindented) //Sparrow\nPidgeon\n    Crow
> ```   

<endpoint module="luxe: string" class="Str" signature="indent(string : String)"></endpoint>
<signature id="Str.indent">Str.indent(**string**: `String`)
<a class="headerlink" href="#Str.indent" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> returns how much indentation characters (whitespace or tabs) a string has.
> 
> ```js
>     var line = "\t  text"
>     var indent = Str.indent(line)
>     Log.print(indent) //3
> ```   

<endpoint module="luxe: string" class="Str" signature="trim(string : String)"></endpoint>
<signature id="Str.trim">Str.trim(**string**: `String`)
<a class="headerlink" href="#Str.trim" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Trims whitespace characters (" ", "\n", "\t") from front and end of an string.
> Calls wren core `String.trim` internally.
> 
> ```js
>     var input = "  \n\t   Pallas's cat   \n\t  "
>     var trimmed = Str.trim(input)
>     Log.print(trimmed) //Pallas's cat
> ```   

<endpoint module="luxe: string" class="Str" signature="compare(a : String, b : String)"></endpoint>
<signature id="Str.compare+2">Str.compare(**a**: `String`, **b**: `String`)
<a class="headerlink" href="#Str.compare+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Num`
> Comparison function for strings. Order is based on the unicode number of the first non-equal codepoint or length.
> Returns `1` when `a > b`
> Returns `-1` when `a < b`
> returns `0` when theyre equal
> 
> ```js
>     Log.print(Str.compare("a", "b")) // -1
>     Log.print(Str.compare("a", "Z")) // 1
>     Log.print(Str.compare("abc", "abc")) // 0
>     Log.print(Str.compare("abc", "abcd")) // -1
>     Log.print(Str.compare("ö", "ä")) // 1
> ```   

<endpoint module="luxe: string" class="Str" signature="replace(string : String, sub : String, repl : String)"></endpoint>
<signature id="Str.replace+3">Str.replace(**string**: `String`, **sub**: `String`, **repl**: `String`)
<a class="headerlink" href="#Str.replace+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Replace all occurances of one substring with another.
> Call wren core `String.replace` internally.
> 
> ```js
>     var input = "Hello World"
>     var replaced = Str.replace(input, "o", "ø")
>     Log.print(replaced) //Hellø Wørld
> ```   

<endpoint module="luxe: string" class="Str" signature="is_alphanumeric(str : String)"></endpoint>
<signature id="Str.is_alphanumeric">Str.is_alphanumeric(**str**: `String`)
<a class="headerlink" href="#Str.is_alphanumeric" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether all characters in a string are alphanumeric (uppercase or lowercase latin characters or arabic numerals)
> 
> ```js
>     Log.print(Str.is_alphanumeric("Leaf")) //true
>     Log.print(Str.is_alphanumeric("4Leaf")) //true
>     Log.print(Str.is_alphanumeric("4-leaf")) //false
>     Log.print(Str.is_alphanumeric("Wørld")) //false
> ```   

<endpoint module="luxe: string" class="Str" signature="vec(value : Vec)"></endpoint>
<signature id="Str.vec">Str.vec(**value**: `Vec`)
<a class="headerlink" href="#Str.vec" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string representation of a vector. (uses 6 digits after decimal point and spaces between numbers)   

<endpoint module="luxe: string" class="Str" signature="vec(value : Vec, precision : Num)"></endpoint>
<signature id="Str.vec+2">Str.vec(**value**: `Vec`, **precision**: `Num`)
<a class="headerlink" href="#Str.vec+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string representation of a vector with the specified digits after the decimal point. (puts spaces between numbers)   

<endpoint module="luxe: string" class="Str" signature="vec(value : Vec, precision : Num, sep : String)"></endpoint>
<signature id="Str.vec+3">Str.vec(**value**: `Vec`, **precision**: `Num`, **sep**: `String`)
<a class="headerlink" href="#Str.vec+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string representation of a vector.
> You can specify both the precision (digits after decimal point) and the seperator of how the vector is rendered.
> 
> ```js
>     var vector = [1, 2, 3.14159265359]
>     Log.print(Str.print(vector)) //1 2 3.141593
>     Log.print(Str.print(vector, 2)) //1 2 3.14
>     Log.print(Str.print(vector, 1, ", ")) //1, 2, 3.1
> ```   

<endpoint module="luxe: string" class="Str" signature="fixed(number : Num, precision : Num)"></endpoint>
<signature id="Str.fixed+2">Str.fixed(**number**: `Num`, **precision**: `Num`)
<a class="headerlink" href="#Str.fixed+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string representation of a number with a specified amount of digits after the decimal point.   

<endpoint module="luxe: string" class="Str" signature="fixed(number : Num)"></endpoint>
<signature id="Str.fixed">Str.fixed(**number**: `Num`)
<a class="headerlink" href="#Str.fixed" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string representation of a number with 6 digits after the decimal points.   

<endpoint module="luxe: string" class="Str" signature="fixed(number : Num, precision : Num, padded : Bool)"></endpoint>
<signature id="Str.fixed+3">Str.fixed(**number**: `Num`, **precision**: `Num`, **padded**: `Bool`)
<a class="headerlink" href="#Str.fixed+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the string representation of a number with a specified amount of digits after the decimal point.
> If padded is true, this function adds zeroes until the requested amount of digits after the decimal point is reached.   

<endpoint module="luxe: string" class="Str" signature="hex(number : Num)"></endpoint>
<signature id="Str.hex">Str.hex(**number**: `Num`)
<a class="headerlink" href="#Str.hex" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get string representation of number in base-16/hexadecimal.   

<endpoint module="luxe: string" class="Str" signature="binary(number : Num)"></endpoint>
<signature id="Str.binary">Str.binary(**number**: `Num`)
<a class="headerlink" href="#Str.binary" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get string representation of number in base-2/binary.   

<endpoint module="luxe: string" class="Str" signature="binary(number : Num, bit_width : Num)"></endpoint>
<signature id="Str.binary+2">Str.binary(**number**: `Num`, **bit_width**: `Num`)
<a class="headerlink" href="#Str.binary+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get string representation of (positive integer) number in base-2/binary.
> `bit_width` declares to how many digits the number should be expanded (adds zeroes to left of it).   

<endpoint module="luxe: string" class="Str" signature="path_is_absolute(path : String)"></endpoint>
<signature id="Str.path_is_absolute">Str.path_is_absolute(**path**: `String`)
<a class="headerlink" href="#Str.path_is_absolute" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js Bool`
> Get whether a path is absolute (instead of relative).   

<endpoint module="luxe: string" class="Str" signature="path_directory(path : String)"></endpoint>
<signature id="Str.path_directory">Str.path_directory(**path**: `String`)
<a class="headerlink" href="#Str.path_directory" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the directory path of a path pointing to a file.   

<endpoint module="luxe: string" class="Str" signature="path_filename(path : String)"></endpoint>
<signature id="Str.path_filename">Str.path_filename(**path**: `String`)
<a class="headerlink" href="#Str.path_filename" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the filename (including extension) of a path pointing to a file.   

<endpoint module="luxe: string" class="Str" signature="path_extension(path : String)"></endpoint>
<signature id="Str.path_extension">Str.path_extension(**path**: `String`)
<a class="headerlink" href="#Str.path_extension" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the extension of a path pointing to a file.   

<endpoint module="luxe: string" class="Str" signature="path_extensionless(path : String)"></endpoint>
<signature id="Str.path_extensionless">Str.path_extensionless(**path**: `String`)
<a class="headerlink" href="#Str.path_extensionless" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get the filename (excluding extension) of a path pointing to a file.   

<endpoint module="luxe: string" class="Str" signature="bytes_formatted(byte_count : Num)"></endpoint>
<signature id="Str.bytes_formatted">Str.bytes_formatted(**byte_count**: `Num`)
<a class="headerlink" href="#Str.bytes_formatted" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get a byte size as bytes/KB/MB/GB/TB (whichever is the biggest unit that is at least 1) with 3 digits after the decimal place.   

<endpoint module="luxe: string" class="Str" signature="bytes_formatted(byte_count : Num, precision : Num)"></endpoint>
<signature id="Str.bytes_formatted+2">Str.bytes_formatted(**byte_count**: `Num`, **precision**: `Num`)
<a class="headerlink" href="#Str.bytes_formatted+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Get a byte size as bytes/KB/MB/GB/TB (whichever is the biggest unit that is at least 1) with `precision` digits after the decimal place.   

<endpoint module="luxe: string" class="Str" signature="upper(string : String)"></endpoint>
<signature id="Str.upper">Str.upper(**string**: `String`)
<a class="headerlink" href="#Str.upper" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Converts a string to all uppercase.   

<endpoint module="luxe: string" class="Str" signature="lower(string : String)"></endpoint>
<signature id="Str.lower">Str.lower(**string**: `String`)
<a class="headerlink" href="#Str.lower" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Converts a string to all lowercase.   

<endpoint module="luxe: string" class="Str" signature="wrap(string : String, column : Num)"></endpoint>
<signature id="Str.wrap+2">Str.wrap(**string**: `String`, **column**: `Num`)
<a class="headerlink" href="#Str.wrap+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Wraps text on spaces to keep line length within column width. Does not break words that are longer than column width.   

<endpoint module="luxe: string" class="Str" signature="path(path : String)"></endpoint>
<signature id="Str.path">Str.path(**path**: `String`)
<a class="headerlink" href="#Str.path" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Normalize a path.   

<endpoint module="luxe: string" class="Str" signature="strip_markup(string : String)"></endpoint>
<signature id="Str.strip_markup">Str.strip_markup(**string**: `String`)
<a class="headerlink" href="#Str.strip_markup" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Strips the luxe markup formatting from the given string, returning the raw value   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any)"></endpoint>
<signature id="Str.format+2">Str.format(**string**: `String`, **arg0**: `Any`)
<a class="headerlink" href="#Str.format+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any)"></endpoint>
<signature id="Str.format+3">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`)
<a class="headerlink" href="#Str.format+3" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any)"></endpoint>
<signature id="Str.format+4">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`)
<a class="headerlink" href="#Str.format+4" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any)"></endpoint>
<signature id="Str.format+5">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`)
<a class="headerlink" href="#Str.format+5" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any)"></endpoint>
<signature id="Str.format+6">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`)
<a class="headerlink" href="#Str.format+6" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any)"></endpoint>
<signature id="Str.format+7">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`)
<a class="headerlink" href="#Str.format+7" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any)"></endpoint>
<signature id="Str.format+8">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`)
<a class="headerlink" href="#Str.format+8" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any)"></endpoint>
<signature id="Str.format+9">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`)
<a class="headerlink" href="#Str.format+9" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any)"></endpoint>
<signature id="Str.format+10">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`)
<a class="headerlink" href="#Str.format+10" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any, arg9 : Any)"></endpoint>
<signature id="Str.format+11">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`)
<a class="headerlink" href="#Str.format+11" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any, arg9 : Any, arg10 : Any)"></endpoint>
<signature id="Str.format+12">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`)
<a class="headerlink" href="#Str.format+12" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any, arg9 : Any, arg10 : Any, arg11 : Any)"></endpoint>
<signature id="Str.format+13">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`)
<a class="headerlink" href="#Str.format+13" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any, arg9 : Any, arg10 : Any, arg11 : Any, arg12 : Any)"></endpoint>
<signature id="Str.format+14">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`, **arg12**: `Any`)
<a class="headerlink" href="#Str.format+14" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any, arg9 : Any, arg10 : Any, arg11 : Any, arg12 : Any, arg13 : Any)"></endpoint>
<signature id="Str.format+15">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`, **arg12**: `Any`, **arg13**: `Any`)
<a class="headerlink" href="#Str.format+15" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format(string : String, arg0 : Any, arg1 : Any, arg2 : Any, arg3 : Any, arg4 : Any, arg5 : Any, arg6 : Any, arg7 : Any, arg8 : Any, arg9 : Any, arg10 : Any, arg11 : Any, arg12 : Any, arg13 : Any, arg14 : Any)"></endpoint>
<signature id="Str.format+16">Str.format(**string**: `String`, **arg0**: `Any`, **arg1**: `Any`, **arg2**: `Any`, **arg3**: `Any`, **arg4**: `Any`, **arg5**: `Any`, **arg6**: `Any`, **arg7**: `Any`, **arg8**: `Any`, **arg9**: `Any`, **arg10**: `Any`, **arg11**: `Any`, **arg12**: `Any`, **arg13**: `Any`, **arg14**: `Any`)
<a class="headerlink" href="#Str.format+16" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> no docs found   

<endpoint module="luxe: string" class="Str" signature="format_list(string : String, args : List)"></endpoint>
<signature id="Str.format_list+2">Str.format_list(**string**: `String`, **args**: `List`)
<a class="headerlink" href="#Str.format_list+2" title="Permanent link">¶</a></signature>
<span class='api_ret'>returns</span> `:::js String`
> Format the string, replacing placeholder with other text.
> Placeholders are in the format `{x}`, where `x` is an index into the arguments list of `format_list`, or a numbered argument in the `format` function.
> Placeholders can appear multiple times and do not need to appear in order.
> 
> ```js
>     Log.print(Str.format("{0} {1} {2}", "Crown", "Trunk", "Roots")) //Crown Trunk Roots
>     Log.print(Str.format("{2} {1} {0}", "Crown", "Trunk", "Roots")) //Roots Trunk Crown
>     Log.print(Str.format("{0} {0} {1}", "Duck", "Goose")) //Duck Duck Goose
> ```   

