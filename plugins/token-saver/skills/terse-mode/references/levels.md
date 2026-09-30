# One answer at two levels

The user asked: "How do I undo my last local commit but keep the changes?"

## Normal (no mode)

Good question! There are a few ways to handle this depending on what you want. If you'd like to undo your most recent commit while keeping your changes staged, you can use a soft reset. Here's the command:

```
git reset --soft HEAD~1
```

This moves your branch back by one commit and leaves your changes staged, so you can edit and commit again. Note that if you have already pushed the commit, rewriting history can cause problems for others. Let me know if you'd like to know about other options!

## L1 Lean

Use a soft reset:

```
git reset --soft HEAD~1
```

It moves the branch back one commit and keeps your changes staged. If the commit is already pushed, other people's copies will no longer match, so coordinate before pushing again.

## L2 Compact

```
git reset --soft HEAD~1
```

- Branch moves back one commit; changes stay staged.
- If the commit is already pushed, other people's copies will no longer match. Coordinate before pushing again.

## What stayed the same at every level

- The command, character for character.
- The warning about a commit that was already pushed, as a full sentence.

## What was removed

- The opening compliment and the "depending on what you want" lead-in.
- The closing offer of more help.
- At L2, the sentence form of the explanation.
