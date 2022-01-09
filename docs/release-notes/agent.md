Note: it's ok if the agent version is slightly different from your engine/editor.
Typically, the 2021.x is what matters for compatibility, the y part in 2021.x.y isn't as important.

# 2022.0.1

Rewrite of a lot of stuff by Ronja, includes a ton of changes. 
Let us know if you find issues. Some key things:

- Improves completion in general
- Improves completion on inheritance
- Improves completion on missing classes (IO/Input/Wren Core)
- Improves import completion flow
- Adds automatic import code actions
- Fix import as redirections
- Add jump to import
- And more

# 2021.0.2-3

- parses doc comments from attributes on classes + methods
- fix infinite loop that sometimes leaves it eating all the ram ever
- fix recursive imports not finding the actual class for completion
- add completion for fields in a class