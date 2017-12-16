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
(setq gc-cons-threshold 100000000)

(defconst spacemacs-version          "0.200.9" "Spacemacs version.")
(defconst spacemacs-emacs-min-version   "24.4" "Minimal version of Emacs.")

(if (not (version<= spacemacs-emacs-min-version emacs-version))
    (error (concat "Your version of Emacs (%s) is too old. "
                   "Spacemacs requires Emacs version %s or above.")
           emacs-version spacemacs-emacs-min-version)
  (load-file (concat (file-name-directory load-file-name)
                     "core/core-load-paths.el"))
  (require 'core-spacemacs)
  (spacemacs/init)
  (configuration-layer/sync)
  (spacemacs-buffer/display-startup-note)
  (spacemacs/setup-startup-hook)
  (require 'server)
  (unless (server-running-p) (server-start)))

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

(add-hook 'focus-out-hook (lambda () (save-some-buffers t)))

(custom-set-variables
 '(speedbar-show-unknown-files t)
)

(display-time-mode 1)

(setq-default flycheck-scalastylerc "/Users/jasongoodwin/scalastyle_config.xml")

(setq-default dotspacemacs-configuration-layers '(
  (scala :variables scala-indent:use-javadoc-style t)))

(setq-default dotspacemacs-configuration-layers '(
    (scala :variables scala-auto-start-ensime t)))
```
