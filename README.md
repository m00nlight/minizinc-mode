# MiniZinc mode 

minizinc-mode is offered as a major mode for editing [minizinc][1] model file. 
Currently it only offer syntax highlight. 

# Configure

```bash
git clone $THiS_REPOSITORY
```

In your `~/.emacs` file or emacs start file, add the following lines

```elisp
(add-to-list 'load-path $PATH_OF_CLONED_DIR)
(add-to-list 'auto-mode-alist '("\\.mzn\\'" . minizinc-mode))
```


# TODO 

- [ ] Implement keywords auto complete
- [ ] Implement run model and show result in echo area or another buffer

# License

Copyright © 2015 by Yushi Wang

Distributed under the GNU General Publicense, view LICENSE for details.


[1]: http://www.minizinc.org
