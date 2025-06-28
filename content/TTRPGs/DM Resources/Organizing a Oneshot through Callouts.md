---
title: 
draft: 
tags:
  - bonfire
  - ttrpg
---
**Callout box types** can be used to differentiate how and when to give players certain information in a visually intuitive fashion. This guide is meant to both showcase how to use the callouts and to explain (under the Advanced Usage section) some extra little things that can be added in order to make the whole note easier to navigate or to better keep track of things.

Partially referenced from [Attovia Wiki](https://attovia.wiki/DM-Resources/DM-Guide).

# Basic Usage
Blocks can (and probably should) be made collapsible `> [!like this]+` in order to make it possible to close them once the moment they're needed in passes (both for reduced clutter and for a visual aid in figuring out how much progress has been made).

> [!info]+ Info Blocks
> **Info Blocks** are used to describe in-world happenings or events which the players are experiencing firsthand. They should be **read aloud** to the players, but can be summarized or adapted depending on the circumstances of the game.

> [!note]+ Note Blocks
> **Note Blocks** are used for DM-first information, that may or may not be revealed to the players (depending on the actual play + what the DM decides is the most appropriate course of action)

> [!cite]+ Quote Blocks
> **Quote Blocks** are used for direct speech and things said directly (and verbatim) to the players.  
> The voice speaking the quote should either be the title of the block or be added at the bottom with some form of indicator.
> 
> 💬 Like this, for example.

> [!warning]+ Warning Blocks
> **Warning Blocks** are for key elements that you should NEVER forget, either needed for foreshadowing or just to ensure the session goes as planned.  
> Forgetting some notes shouldn't be too big of a problem, usually. Forgetting a key element might actively impair the session and the flow of gameplay.

> [!example]+ Example Blocks
> **Example Blocks** are used to explain mechanical effects, whether they're custom mechanics or explanations of effects/reactions of something on the world.

> [!danger]+ Danger Blocks
> **Danger Blocks** are used for custom conditions and status effects.

---
# Advances Usage

## Nesting Callout Blocks 

Blocks can be **nested** in order to give context clues, suggest an order-of-operation, or detail secondary effects/explanations. Only the topmost callout has to be collapsible; the rest can be left as-is.
Text can be added in between multiple nested blocks (usually in the top level one) in order to add extra context. There is no real limit to levels of nesting, but overdoing it is discouraged in order to reduce visual clutter and all.

**How to nest callouts:**

``` markdown
> [!info]+ Top Level Info
> Read this to players first
> > [!quote] Nested Quote
> > This is said after that
```

**Output:**

> [!info]+ Top Level Info
> Read this to players first
> > [!quote] Nested Quote
> > This is said after that

For more complex nesting, make sure to insert a blank line between the items in order to prevent conflicts that may end up messing up the whole nested block. Checking whether everything works as intended in Reader View every once in a while is strongly recommended.

**Another, more complex example (code + output):**

``` markdown
> [!info]+ Top Level Info
> Read this to players first
> 
> > [!quote] Nested Quote
> > This should be read second
> 
> Read this to players third
> 
> > [!note] Nested Note
> > A DM note here, read fourth
> 
> > [!example] Nested Effect
> > This effect happens fifth
> > > [!danger] Nested Condition
> > > The effect causes this condition sixth
```

> [!info]+ Top Level Info
> Read this to players first
> 
> > [!quote] Nested Quote
> > This should be read second
> 
> Read this to players third
> 
> > [!note] Nested Note
> > A DM note here, revised fourth
> 
> > [!example] Nested Effect
> > This effect happens fifth
> > > [!danger] Nested Condition
> > > The effect causes this condition sixth
## Anchor Links

Linking to other headings in the note can be a useful way to navigate the text with more ease and to keep things organized and readily accessible (for example, putting all status effects at the bottom and linking to them earlier in the note where needed). An anchor link can be made in the same way as a normal Wikilink, using the following syntax: `[[note title#heading|display text]]`.

Example of an anchor link: [[Organizing a Oneshot through Callouts#Basic Usage|Basic Usage]]