# MiniZinc mode

minizinc-mode is offered as a major mode for editing [minizinc][1] model file.
Currently it only offer syntax highlight.

# Installation and Configuration

## Manual install

```bash
git clone $THiS_REPOSITORY
```

In your `~/.emacs` file or emacs start file, add the following lines

```elisp
(require 'minizinc-mode)
(add-to-list 'load-path $PATH_OF_CLONED_DIR)
(add-to-list 'auto-mode-alist '("\\.mzn\\'" . minizinc-mode))
```

## Install from melpa

Add the following to your emacs init file, normally `~/.emacs`

```elisp
(require 'package)
(add-to-list 'package-archives
             '("melpa" . "https://melpa.org/packages/"))
(unless package-archive-contents (package-refresh-contents))
(package-initialize)
```

In your emacs, Use `M-x`, `package-install` then type `minizinc-mode` to
install the latest version from [melpa][https://melpa.org].

Then add the following line to your emacs init file for configuration.

```elisp
(require 'minizinc-mode)
(add-to-list 'auto-mode-alist '("\\.mzn\\'" . minizinc-mode))
```

## Pretty-render logic symbols

Some logic symbols can be rendered as Unicode characters. To enable
this, customize the variable `minizinc-font-lock-symbols` to true. You
can change the replacements by customizing the variable
`minizinc-font-lock-symbols-alist`.


# TODO

- [ ] Implement keywords auto complete
- [ ] Implement run model and show result in echo area or another buffer

# License

Copyright © 2015-2017 by Yushi Wang

Distributed under the GNU General Publicense, view LICENSE for details.


[1]: http://www.minizinc.org
