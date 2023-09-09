![Shellcheck](https://github.com/jeircul/tmux-tokyonight-theme/actions/workflows/shellcheck.yml/badge.svg)

# TMUX - Tokyonight theme  

![tmux-tokyonight-theme Preview](https://raw.githubusercontent.com/jeircul/tmux-tokyonight-theme/master/theme.png)

## 📦 Installation via [TPM](https://github.com/tmux-plugins/tpm) (recommended)

1.  Add plugin to the list of TPM plugins in `.tmux.conf`:

    ``` tmux
    set -g @plugin 'jeircul/tmux-tokyonight-theme'
    ```
2.  Use <kbd>prefix</kbd>–<kbd>I</kbd> to install `tmux-tokyonight-theme`.
3.  When you want to update `tmux-tokyonight-theme` use <kbd>prefix</kbd>–<kbd>U</kbd>.

<details>
<summary>📦 Manual Installation</summary>

1. Clone the repo:
   ```sh
   git clone https://github.com/jeircul/tmux-tokyonight-theme ~/.config/tmux/plugins/
   ```
2. Add this line to the bottom of `.tmux.conf`:
   ```tmux
   run-shell ~/.config/tmux/plugins/tmux-tokyonight-theme/tmux-tokyonight-theme.tmux
   ```
3. Use <kbd>prefix</kbd>–<kbd>R</kbd> to Reload TMUX environment
</details>

## ⚙️ Configuration

<details>
<summary>Widgets</summary>
    
```
set -g @tokyonight_widgets "#(date +%s)"
```
- Once set, these widgets will show on the right.
- **default**: empty string.
</details>

<details>
<summary>Time format</summary>

```
set -g @tokyonight_time_format "%I:%M %p"
```
- `%I` - The hour as a decimal number using a 12-hour clock  
- `%M` - The minute as a decimal number
- `%p` -  Either "AM" or "PM" according to the given time value.
- **default**: `%R` - The time in 24-hour notation (%H:%M).

> **Note**
> These modifiers were taken from from [strftime manpage](http://man7.org/linux/man-pages/man3/strftime.3.html).

</details>

<details>
<summary>Date format</summary>

```
set -g @tokyonight_date_format "%D"
```
- `%D` - Equivalent to %m/%d/%y (American format).   
- `%m` - The month as a decimal number.  
- `%d` - The day of the month as a decimal number  
- `%y` - The year as a decimal number without the century.  
- **default**: `%d/%m/%Y` - The date in non-American format.

> **Note**
> These modifiers were taken from from [strftime manpage](http://man7.org/linux/man-pages/man3/strftime.3.html).

</details>

## 🛠️ Issues

<details>
<summary>Symbols are missing</summary>

* The theme requires Powerline symbols exist and set on your system. Follow [these instructions](https://github.com/powerline/fonts) to install them, then update your terminal fonts to use them.
</details>

<details>
<summary>Symbols are corrupted</summary>

- Patched Powerline fonts aren't picked up when `$LANG` isn't set to `en_US`. You can change the default locale settings at `/etc/default/locale`.
</details>

<details>
<summary>Widgets not working</summary>
    
- Make sure that you put the `set -g @plugin 'jeircul/tmux-tokyonight-theme'` before other scripts that alter the status line, or they won't be able to pickup the plugin's changes.
</details>

<details>
<summary>True Color</summary>
    
- Make sure TrueColor is enabled and working. follow [these instructions](https://sunaku.github.io/tmux-24bit-color.html#usage) to do so.
</details>

## ⚖ License

[MIT](LICENSE)
