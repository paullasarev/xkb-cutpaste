Refs:
* https://superuser.com/questions/385748/binding-superc-superv-to-copy-and-paste
* http://rus-linux.net/MyLDP/x/xkb/xkb.html

Run
* to set
```sh
setxkbmap -v -option cutpaste:super
```
* to get current map
```sh
xkbcomp -a $DISPLAY - 
```


Location
* /usr/share/X11/xkb/types/cutpaste
* /usr/share/X11/xkb/symbols/cutpaste
* /usr/share/X11/xkb/rules/evdev
  * rules that starts with:
    ```
    ! option =   symbols
    * add line after that:
        ```
        cutpaste:super     = +cutpaste
        ```
  * rule that starts with: ! option    =   types
    * add line after that: 
        ```
        cutpaste:super     = +cutpaste
        ```
* /usr/share/X11/xkb/rules/evdev.lst
  * rules that starts with: ! option
    *  add a line: 
        ```
        cutpaste:super     Add super equivalents of cut and paste operations
        ```

