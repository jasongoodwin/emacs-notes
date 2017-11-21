# emacs-notes

# Windowing Management
I've been slack with managing buffers. Couple notes:
- split window horizontally/vertically: `C-x 2` or `C-x 3`
- close the current window with `C-x 0`
- close all _other_ windows with `C-x 1`
- change to other window with `C-x o`

- open an entire new frame with `C-x 5 2` (delete with 0 and 1 as with windows)

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


# init.el backup...
```
;; probably don't need this anymore but ¯\_(ツ)_/¯
(global-unset-key (kbd "<left>"))
(global-unset-key (kbd "<right>"))
(global-unset-key (kbd "<up>"))
(global-unset-key (kbd "<down>"))
(global-unset-key (kbd "<C-left>"))
(global-unset-key (kbd "<C-right>"))
(global-unset-key (kbd "<C-up>"))
(global-unset-key (kbd "<C-down>"))
(global-unset-key (kbd "<M-left>"))
(global-unset-key (kbd "<M-right>"))
(global-unset-key (kbd "<M-up>"))
(global-unset-key (kbd "<M-down>"))

;; use shift + arrow keys to switch between visible buffers
(when (fboundp 'windmove-default-keybindings)
  (windmove-default-keybindings))

;; save on loose focus!
(add-hook 'focus-out-hook (lambda () (save-some-buffers t)))

;; speedbar is disabled, but if I use it I want it to show all files
(custom-set-variables
 '(speedbar-show-unknown-files t)
)

;; put time in modeline
(display-time-mode 1)

```
