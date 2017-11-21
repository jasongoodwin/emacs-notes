# emacs-notes
starting to work on non-scala projects more so want to become more proficient with emacs.

# Rectangular editing
Just mark a rectangle and then `C-x r *` where `*` is the associate  command. 

# Windowing Management
I've been slack with managing buffers. Couple notes:
- split window horizontally/vertically: `C-x 2` or `C-x 3`
- close the current window with `C-x 0`
- close all _other_ windows with `C-x 1`
- change to other window with `C-x o`

- open an entire new frame with `C-x 5 2` (delete with 0 and 1 as with windows)

# Buffer management
- select buffer in minibuffer with `C-x b` 
- see all buffers in window with `C-x C-b`
- kill a buffer with `C-x k`

For the buffer view:
- M	An asterisk (*) is displayed in this column if the buffer has been modified since it was last saved
- R	A percent sign (%) is displayed in this column if the buffer is read-only
- Buffer	The name of the buffer
- Size	Size of the buffer in Bytes
- Mode	The Major mode active in the buffer
 - File	The name of the file, if any, load into the buffer

# helm-projectile project navigation
Speed bar isn't really suitable for navigating projects. I've been trying to use helm-projectile for super fast navigation

- set a project with `C-c p p`
- find a file with `C-c p f`
most of the commands of interest (delete, move etc) can be executed from the find file command 
 
# Zoom
```
C-x C-+ 
C-x C--
```
