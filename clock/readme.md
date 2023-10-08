# Rofi clock
Rofi clock is a bash script that displays time and date using [rofi](https://github.com/davatorium/rofi) and [rofi-blocks.](https://github.com/OmarCastro/rofi-blocks)
## Install
To install the script, simply copy it to any directory in $PATH
```
sudo cp rofi-clock /bin
```
## Usage
If it has been installed, you can just run
```
rofi-clock
```

Else, you can just specify the path:
```
/path/to/rofi-clock
```
note: using the above method requires modifying the script to include the path on line 43.

If you want to use a custom rofi command, you can modify the default one:
```
rofi -modi blocks -show blocks -blocks-wrap "rofi-clock from_blocks" -theme-str "listview {lines: 7; columns: 7; flow: horizontal;}"
```
If you choose to directly call rofi, **DO NOT** use `-mode "clock:rofi-clock from_blocks" -show clock`. It could freeze your screen and force you to restart your device, as rofi does not support updating values live and will wait until the never ending script has finished executing before showing the menu.
