-   an extension for [[emacs]]
    - #go https://www.gnu.org/software/hyperbole/
    - to define [[wikilinks]] as implicit buttons, use:
```
        (require 's)

        (defil wikilink "[[" "]]" "[a-zA-Z].*"
          #'(lambda (s) (find-file
                         (s-with s
                           s-downcase
                           (s-replace-all '((" " . "-")))
                           (s-append ".md")))))
```
