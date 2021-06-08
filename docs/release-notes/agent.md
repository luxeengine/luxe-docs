Note: it's ok if the agent version is slightly different from your engine/editor.
Typically, the 2021.x is what matters for compatibility, the y part in 2021.x.y isn't as important.

# 2021.0.2-3

- parses doc comments from attributes on classes + methods
- fix infinite loop that sometimes leaves it eating all the ram ever
- fix recursive imports not finding the actual class for completion
- add completion for fields in a class