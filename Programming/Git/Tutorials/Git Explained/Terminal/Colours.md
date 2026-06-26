# `Colouring the Terminal`
While `GitBash` is commonly referred to as `Git`, the `Bash` portion is relevant.
`Bash` is the terminal that `Git` runs on.

A parallel could be:
`Bash` is `Windows`
`Git` is `Windows 11`
While `Windows 11` is certainly different than `Windows 7`, they are both (at the end of the day), `Windows`.
The functionality may be vastly different, but its base/core of how it's coded is the same.

`Bash` is a `truecolor` ("**24-bit**") terminal.
This means that a vast array of colors are supported within it.
It is important to check the specifications of the programs you work on to check *their* capabilities.

While it is a `truecolor` terminal, `ANSI` is a very common color scheme supported by many machines.
In `ANSI`, there are many variants depending on what specific subset is being used.
Most terminals support `8`/`16` colours as well as `256` ("**8-bit**").
This can include base colours and their respective **bright** or **bold** colours.

The ANSI colours run through a **Select Graphic Rendition** (`SGR`).
These colours share specific parameters, separated by semicolons.
The changes remain in effect until a subsequent SGR resets it.
When no codes are given, it is treated as a reset/normal colour.

### 256 ("8-bit") [`;5`]
Use an `escape sequence`, represented by `ESC[` `...` here.
- Foreground ("Text") [`38;`]
  - `...` `38;5;` `#` `m`
- Background [`48;`]
  - `...` `48;5;` `#` `m`

### Common Escape Sequences
- Not guaranteed to work in all languages/compilers.
  - `\e` (for `ESC`)
    - Recommended to generally use decimal, octal, or hex codes as they are much more widely supported.
- Hexadecimal ("Hex Codes")
  - `\x1b`
- Octal ("8-bit")
  - `\033`
- Unicode
  - `\u001b`

The colours for foreground and background share the same `#`.
Several reference tables exist, see below for both foreground and background captured.
![Two tables are split evenly down the middle. Both depict the 8-bit ANSI colour schema, with numbers from 0-256. The left table depicts a black background with each number coloured by its respective colour code. The right table depicts white text with each background coloured by its respective colour code.](ANSI256Visual.png)

Due to the `truecolor` nature of the `Bash` terminal, we can augment the above 8-bit colour scheme to support any RGB colour.
### Truecolor ("24-bit") [`;2`]
`ESC[` `...`
- Foreground ("Text") [`;38`]
  - `...` `38;2;` `#R` `#G` `#B`  `m`
- Background [`48;`]
  - `...` `48;2;` `#R` `#G` `#B`  `m`

The second number, the `;5` or `;2` identify the identification format of the colour.

A third number comes into play that further provides colour customisation.
That number comes by itself in an escape sequence.

### `ESC[` `#` `;m` [In # Order]
`0` = `Reset All`/`Default to Normal`
`1` = `Bold`/`Increased Intensity`
`2` = `Dim`/`Decreased Intensity`
`3` = `Italic`
`4` = `Underline` (`Single`)
`5` = `Blink` (`Slow`)
`6` = `Blink` (`Rapid`)
`7` = `Invert` (Foreground and Background Colours)/`Reverse Video` 
`8` = `Hide`/`Conceal`
`9` = `Strikethrough`/`Cross-Out`
`10` = `Default Font`/`Primary Font`
`11`-`19` = `Alternative Font`
`20` = `Fraktur`/`Gothic` (`Calligraphic Latin`)
`21` = `Underline` (`Double`)
`22` = `Normal Intensity`
`23` = `Italic` (`Removal`)
`24` = `Underline` (`Removal`)
`25` = `Blink` (`Removal`)
`26` = `Proportional Spacing`
`27` = `Inverse` (`Removal`)
`28` = `Reveal`
`29` = `Strikethrough`/`Cross-Out` (`Removal`)
`30`-`37` = `Foreground Colour` (`8`/`16`)
`38` = `Foreground Colour` (`8-bit`)
`39` = `Default Foreground Colour`
`40`-`47` = `Background Colour` (`8`/`16`)
`48` = `Background Colour` (`8-bit`)
`49` = `Default Background Colour`
`50` = `Proportional Spacing` (`Removal`)
`51` = `Frame`
`52` = `Encircle`
`53` = `Overline`
`54` = `Frame`/`Encircle` (`Removal`)
`55` = `Overline` (`Removal`)
`56`-`57` = `???`
`58` = `Underline Colour`
`59` = `Default Underline Colour`
#### Ideogram
`60` = `Underline` or `Right Side Line`
`61` = `Double Underline` or `Double Right Side Line`
`62` = `Overline` or `Left Side Line`
`63` = `Double Overline` or `Double Left Side Line`
`64` = `Stress Marker`
`65` = `Reset`
`66`-`72` = `???`
#### mintty
`73` = `Superscript`
`74` = `Subscript`
`75` = `Reset`
#### aixterm
`90`-`97`=`Set Bright Foreground Colour`
`100`-`107` = `Set Bright Background Colour`


## The ones to keep in mind that actually work in `Bash` are as follows.
### `Default to Normal` = `0` | *Everything*.

Most other resets, add `20` and that is the reset code.
Each individual reset code is listed below their option.

## Cell Colour
`Foreground` = `38`
<sub> `Default (Foreground)` = `39`

`Background` = `48`
<sub> `Default (Background)` = `49`

## Bold
`Dim` = `2` |  `Bold` = `1`
<sub> `Default Intensity` = `22`

## Italic
`Italic` = `3`
<sub> `Default, Non-Italicized` = `23`

## Lines

### Over
`Overline` `53` = `Reset` (No Overline) = `55`
<sub>

### Through
`Strikethrough` = `9`
<sub> `Default, Unstriked` = `29`

### Under
`Single` = `4` | `Double` = `21`
<sub> `Default, No Underline` = `24`

`Colour` = `58`
<sub> `Default Colour` = `59`

### Blink
`Slow` = `5` | `Rapid` =  `6`
<sub> `Default, Static` = `25`

### Inverse
`Invert` (`Foreground = Background`/`Background = Foreground`) = `7`
<sub> `Default Color Schema` (`Foreground = Foreground`/`Background = Background`) = `27`

### Hide
`Hide` = `8`
<sub> `Show` = `28`

---