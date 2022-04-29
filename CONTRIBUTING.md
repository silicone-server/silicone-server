*psst! up here. I stole this markdown file from [Anuken](https://github.com/Anuken/Mindustry/blob/master/CONTRIBUTING.md) and edited it, check him out! he's pretty cool.*

# Contributing
## Basic Guidelines

### Always test your changes.
Do not submit something without at least running the game to see if it compiles.  
If you are submitting a new block, make sure it has a name and description, and that it works correctly in-game. If you are changing existing block mechanics, test them out first.

### Do not make large changes before discussing them first.
If you are interested in adding a large mechanic/feature or changing large amounts of code, first contact me (Anuken) via [Discord](https://discord.gg/mindustry) - either via PM or by posting in the `#pulls` channel.
For most changes, this should not be necessary. I just want to know if you're doing something big so I can offer advice and/or make sure you're not wasting your time on it.

### Do not make formatting PRs.
Yes, there are occurrences of trailing spaces, extra newlines, empty indents, and other tiny errors. No, I don't want to merge, view, or get notified by your 1-line PR fixing it. If you're implementing a PR with modification of *actual code*, feel free to fix formatting in the general vicinity of your changes, but please don't waste everyone's time with pointless changes.

## Style Guidelines

### Follow the formatting guidelines.
This means:
- No spaces around parentheses: `if(condition){`, `SomeType s = (SomeType)object`
- Same-line braces.
- 4 spaces indentation
- `camelCase`, **even for constants or enums**. Why? Because `SCREAMING_CASE` is ugly, annoying to type and does not achieve anything useful. Constants are *less* dangerous than variables, not more. Any reasonable IDE should highlight them for you anyway.
- No underscores for anything. (Yes, I know `Bindings` violates this principle, but that's for legacy reasons and really should be cleaned up some day)
- Do not use braceless `if/else` statements. `if(x) statement else statement2` should **never** be done. In very specific situations, having braceless if-statements on one line is allowed: `if(cond) return;` would be valid.
- Prefer single-line javadoc `/** @return for example */` instead of multiline javadoc whenever possible
- Short method/variable names (multipleLongWords should be avoided if it's possible to do so reasonably, especially for variables)
- Use wildcard imports - `import some.package.*` - for everything. This makes incorrect class usage more obvious (*e.g. arc.util.Timer vs java.util.Timer*) and leads to cleaner-looking code.
- 
