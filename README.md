# emacs-notes

Quick reference for things to learn well. Once They're in my head, remove or put em in the graveyard.

## Magit
`magit-branch-popup` - `b` - checkout branches, etc
`magit-show-refs-popup` - or `y` - see branches

## Smex
`C-h f`, while Smex is active, runs describe-function on the currently selected command.
`M-.` jumps to the definition of the selected command.
`C-h w` shows the key bindings for the selected command. (Via where-is.)
`smex-show-unbound-commands` shows frequently used commands that have no key bindings.

## Zoom
```
C-x C-+ 
C-x C--
```


# Graveyard

## Windowing Management
I've been slack with managing buffers. Couple notes:
- split window horizontally/vertically: `C-x 2` or `C-x 3`
- close the current window with `C-x 0`
- close all _other_ windows with `C-x 1`
- change to other window with `C-x o`

- open an entire new frame with `C-x 5 2` (delete with 0 and 1 as with windows)

## helm-projectile project navigation
Speed bar isn't really suitable for navigating projects. I've been trying to use helm-projectile for super fast navigation

- set a project with `C-c p p`
- find a file with `C-c p f`
most of the commands of interest (delete, move etc) can be executed from the find file command 
