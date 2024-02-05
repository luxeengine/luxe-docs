Note: it's ok if the agent version is slightly different from your engine/editor.
Typically, the 2022.x is what matters for compatibility, the y part in 2022.x.y isn't as important.

# 2024.2.1

- Add code Outline to vscode! (Izzy)
- Lots of bug fixes and improvements to reliability

# 2022.0.4

- add completion for assets
- fix jump to definition on classes with a superclass

# 2022.0.3

- Fix bug causing the agent to die when it shouldn't, requiring restarts
- Fixed bug in code actions around offering imports for missing classes

# 2022.0.1-2

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