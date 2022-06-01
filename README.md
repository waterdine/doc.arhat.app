# Welcome to Arhat's documentation!

Arhat is a game prototyping tool that currently uses Studio Waterdine's 虎.engine.
Arhat prototypes games using Visual Novels.
Arhat is suitable for creating stories between friends, or as a way to design stories for larger games.
Arhat provides a simple Visual Novel script and project format, that can be shared.
Arhat provides a library or "asset pack" system to share characters, backgrounds and sound effects between Arhat projects.

## Arhat script
This is the scripting format for Visual Novels.
Arhat currently uses a simple per scene script format.
Our plan is to update to use a screenwriting format similar to http://fountain.io.
For now each new scene is delineated by a // followed by “Scene -“ and the scene type.
For example:

```// Scene - CutScene, Image: IntroTree
Line 1,
Line 2,
Line 3
```

There are a number of useful scene types:
CutScene,
Story,
Choice
And so on.

Example Arhat Script of a branching story:

```
// Scene 1 - Intro

/* Chapter 1 */

// Scene 2 - ChapterTransition, ShowPressToContinue: True
HorizontalNumber: Chapter 1
HorizontalTitle: Simple Scenes
VerticalNumber: 第一話
VerticalTitle: 第一話

// Scene - CutScene, Image: IntroTree
Arhat uses a simple scripting syntax to allow creation of visual novels.
Each scene allows a changing background a, transition and scene type.
This is a fullscreen “cutscene” type.

// Scene - Story, Image: IntroTree
GrubbyVillager: Hello I am Grubby Villager.
GrubbyVillager: This is a story based scene type with a character.

// Scene - Choice
DirectingText: Which path?
Choice1Text: Path A (Continue).
Choice2Text: Path B (Jump). // SkipTo: PathB

// Scene - Story, Image: IntroTree
GrubbyVillager: Welcome to Path A.
GrubbyVillager: At the end of Path A, you usually skip past Path B.
GrubbyVillager: In this example we SkipTo the Ending.

// SkipTo: Ending

// Label: PathB
// Scene - Story, Image: IntroTree
GrubbyVillager: Welcome to Path B.
GrubbyVillager: This has skipped over the scenes in Path A.

// Label: Ending
// Scene - Story, Image: IntroTree
GrubbyVillager: This ends the simple branching story example.
GrubbyVillager: Now to the credits!

// Scene - Credits
```

### 虎.engine

The 虎.engine is split into 3 frameworks.

虎.engine.base
虎.engine.story
虎.engine.puzzle

### Support or Contact

Please use the github issues to get in contact:
https://github.com/waterdine/doc.arhat.app/issues
