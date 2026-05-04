[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![JCS-ELPA](https://raw.githubusercontent.com/jcs-emacs/badges/master/elpa/v/on.svg)](https://jcs-emacs.github.io/jcs-elpa/#/on)

# on.el -- utility hooks and functions from Doom Emacs

[![CI](https://github.com/elp-revive/on.el/actions/workflows/test.yml/badge.svg)](https://github.com/elp-revive/on.el/actions/workflows/test.yml)

This package exposes a number of utility hooks and functions ported
from Doom Emacs. The hooks make it easier to speed up Emacs startup
by providing finer-grained control of the timing at which packages
are loaded.

For example, `use-package` users can delay loading the `which-key`
package until the first key is pressed:

```elisp
(use-package which-key
  :hook (on-first-input . which-key-mode))
```

The list of hooks provided by `on.el` is as follows:

- `on-first-input-hook`: run before the first user input.
- `on-first-file-hook`: run before the first interactively opened file.
- `on-first-buffer-hook`: run before the first interactively opened buffer.
- `on-init-ui-hook`: run when the UI has been initialized. This one is useful for setting fonts and enabling custom themes without having to worry about whether Emacs is running as a daemon or not.
