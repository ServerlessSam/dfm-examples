# filename-list-generator-example
 A example showing how data-file-merge can be used to produce a list of file names from a directory tree. Try it for yourself!

 ## Example 1
 A simple hello-world example. It uses the `**` and `*` syntax from pathlib to ensure all json files are sourced from all directories.

 ## Example 2
 A slightly more complex version of Example 1. This example uses 2 `SourceFile`s to merge all nested file names to a different key in the final file.

 ## Example 3 (Requires the parameter Prefix=Sub to run)
 An example demonstrating the substitution options you have available:
 - A literal substiution is made from a long string (`1-foo-bar-baz`) which is passed through a regex expression to find the first string before an `-`
 - A parameter subsitution is made for the parameter with the name `Prefix`. The value (`Sub`) of this is then passed through a naming convention converter, converting from Pascal case to lowercase (`sub`)
