# Recap
In `01_TableOfContents.md`, very `.toc` `tag`, `directive`, and `variable` was discussed.  
Author's `.toc` at the end of `01_TableOfContents.md` is as seen below.  

```
## Interface: 120100
## Title: |cffffffffW|cffe6fff5i|cffccffebn|cffb3ffe2t|cff99ffd8e|cff80ffcer|cff66ffc4g|cff4dffbar|cff33ffb1e|cff19ffa7e|cff00ff9dn|r
## IconTexture: Interface\AddOns\Wintergreen\WintergreenIcon(Letters,BlackSticker)
## Notes: My first AddOn, primarily a learning experience!
## Author: Swift
## Version: |cff00ff9d0|cffffffff.|cff00ffb70|cffffffff.|cff00ffe60|r
```

# <DO SLASH COMMANDS (pt.3) FIRST, FRAMES ARE A TON OF INFO.>
# Printing Time
Now that the `.toc` file is complete, we can begin adding files into it as they're created.  

Begin with creating a `Lua` file to start the AddOn with and add it to the `.toc`,
The `.toc` presumes the same base folder as it is in.  

If an AddOn was named `Wintergreen`, the file path of `*\World of Warcraft\_retail\Interface\AddOns\Wintergreen` is not needed in the `.toc`.  
If that AddOn contained a folder called `Core` that held a file called `Init.lua`, its `.toc` addition would be as seen below.  

```
Core/Init.lua
```

Author decided to name their first `Lua` file, `Basic.lua`.  
Their `.toc` addition is seen below.  

```
Basic.lua
```

A very simple function that provides immediate results is Lua's `print()` function.  
Using `print()` can be a reliable way to assess the status of firing code.  

WoW's chat window is where the output of Lua's `print()` function is... well, printed to.  
For direct text inside the `()`, it must be encased in quotes (`""`) to be recognized as a string.  

On `/reload`, the file listed in the AddOn's `.toc` will be loaded and its code executed.  
Any file containing print statements in the base file will print when a character logs in.  

Author chose to print `This is a test message!`.  
Their file (`Basic.lua`)'s addition would be as follows.  

```lua
print("This is a test message!")
```

<IMAGE SHOWING THAT>

The `print()` function can print more than just direct strings, such as variables and outputs of other functions.  
In the Lua file, create a `local` `variable` and equate it to a string of your choosing.  

`Local` `variable`s are restricted to the scope they're within.  
They're declared through the use of `local` `*` `=` `*`.  

If `local` is absent, the `variable` becomes `global`, meaning it is not restricted if not underneath another scope.  
<is scope the right word? check wording.>

Other AddOns are able to access any AddOn's `global` `variable`s.  
To avoid "polluting" the global field, use `local` `variable`s as much as possible.  

Author chose to declare `local Output = "This is an output string!"`.  
Their declaration and `print()` function is as seen below.  

```lua
local Output = "This is an output string!"
print(Output)
```

<IMAGE SHOWING THAT>
 
The `print()` function, when containing any item(s) to print, typically is referred to as a print statement.  
Inputs of a function are called `arguments`, `args` for short.  

In this case, `print()` receives variable arguments, `vararg` or `...` for short.  
Variable in the sense that the function will work with any number of arguments.  

Typically, arguments are written in lower-case with subsequent proper capitalization (what was the term again?) and without non-literal spaces in the function, only separated by commas (`,`).

Arguments are conjoined by either commas (`,`) or concatenation (`.`). 
There is no real difference between the two.  
 
 Concatenation, when used for variables, is 1 dot (`.`).
 Concatenation, when used for direct strings, is 2 dots (`..`).  

 As a `print()` statement's argument output is a string, its arguments are also strings.  
 As such, concatenation will use `..` for these conjoining strings.

Non-literal spaces may be added if Author desires for legibility of the code itself.  
Coding practices that assist in human legibility such as this, also known as making it more "human friendly", are referred to as "syntactic sugar".  

Author's declaration/combination of their prior `print()` statements, in order, is possible in many ways, as seen below.  

```lua
local Output = "This is an output string!"
print( "This is a test message!",Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!",Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!",Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!",Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" ,Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!" ,Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!" ,Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" ,Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!", Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!", Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!", Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!", Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" , Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!" , Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!" , Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" , Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!"..Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!"..Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!"..Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!"..Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" ..Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!" ..Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!" ..Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" ..Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!".. Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!".. Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!".. Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!".. Output )
```

```lua
local Output = "This is an output string!"
print( "This is a test message!" .. Output)
``` 

```lua
local Output = "This is an output string!"
print("This is a test message!" .. Output)
``` 

```lua
local Output = "This is an output string!"
print("This is a test message!" .. Output )
``` 

```lua
local Output = "This is an output string!"
print( "This is a test message!" .. Output )
``` 

<IMAGE IN GAME>

However, as seen in Author's client above, using any of the above variants of combined print statements will return the message: `This is a test message!This is an output string!`.  
Lua removes non-literal spaces when code is parsed so the only way a literal string of a space can be added is to add it in the statement itself.  

There are multiple ways a literal string of a space can be added into the combined `print()` statement variants from above:  
- At the end of `"This is a test message!"`.
- At the beginning of `Output`'s assigned value.
- Insert a literal string of a space in-between `"This is a test message!"` & `Output` in the `print()` statement.
- Insert a variable in-between `"This is a test message!"` & `Output` in the `print()` statement whose value is assigned to the literal string of a space.

The above list is demonstrated below without non-literal spaces between items in the statement.

```lua
local Output = "This is an output string!"
print("This is a test message! ",Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message! "..Output)
```

```lua
local Output = " This is an output string!"
print("This is a test message!",Output)
```

```lua
local Output = " This is an output string!"
print("This is a test message!"..Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!"," ",Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!"," "..Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!".." ",Output)
```

```lua
local Output = "This is an output string!"
print("This is a test message!".." "..Output)
```

```lua
local Output = "This is an output string!"
local SPACE = " "
print("This is a test message!",SPACE,Output)
```

```lua
local Output = "This is an output string!"
local SPACE = " "
print("This is a test message!",SPACE..Output)
```

```lua
local Output = "This is an output string!"
local SPACE = " "
print("This is a test message!"..SPACE,Output)
```

```lua
local Output = "This is an output string!"
local SPACE = " "
print("This is a test message!"..SPACE..Output)
```

<IMAGE SHOWN HERE>

In regards to future `print()` statements, Author will concatenate to/from strings, without spaces, and use commas when connecting variables to other variables, with spaces.  
See below for an example of Author's use of syntactic sugar in an example of a `print()` statement containing two `local` `variables` where the middle variable has a space at both the beginning and end of its string.  

```lua
local Output = " This is an output string! "
local SecondOutput = "This is another output string!"
print("This is a test message!"..Output, SecondOutput)
```

<IMAGE SHOWN HERE>

Future `print()` statements can be achieved in any proper way listed above.  
Author's syntactic sugar will be applied to future `print()` statements without mention of the other proper avenues.

# Framework

Many AddOns do significantly more than just print statements to the chat window.  
Even more commonly, they have either a frame or many frames that appear in the User Interface.  

Blizzard (and/or AddOns) create the **U**ser **I**nterface (UI) or **G**raphic **U**ser **I**nterface (GUI) through these frames.
Blizzard's Frames can also act as templates or AddOn developers, or they can make new ones.  

The API for Frames in Lua and XML is massive, they will all be covered in their own documents.  
For now, a very small portion of the `CreateFrame()` function will be covered.  

Functions on typical sources of informational websites are shown as seen below.  

```lua
`Variable_FrameName = CreateFrame(frameType[, name[, parent[, template[, id]]]])`
```

<Go over types of arguments, 'string', 'numeric', 'nil', etc.>

Author will utilize the below method to demonstrate functions and their methods as they feel it provides the best context.  
See below for `CreateFrame()`'s syntax, intricacies listed in the separate framework document.  

```lua
Variable_FrameName = -- Assign a variable for Methods to reference.
CreateFrame() -- Base Function
        frameType, -- Argument #1;  STRING; "Frame", "Button", etc.
                [
                name, -- Argument #2 (Optional); STRING; Global Name for reference [or 'nil' for anonymous]
                        [
                        parent, -- Argument #3 (Optional, needs 'name'); VARIABLE;  mirror settings to/hook into [or nil to be parentless]; Can also be set with Region:SetParent()
                                [
                                template, -- Argument #4 (Optional, needs 'parent'); STRING; Based on FrameXML Templates
                                        [
                                        id -- Argument #5 (Optional, needs 'template'); NUMBER; for reference; can also be set with Frame:SetID()
                                        ]
                                ]
                        ]
                ]
```

Author's' `Variable_FrameName` will be `BaseFrame` and their `frameType` will be `"Frame"`.  
Their deconstructed Lua entry is as seen below.

```lua
BaseFrame =
CreateFrame()
        "Frame",
                [
                "BaseFrame",
                        [
                        UIParent,
                                [
                                "BasicFrameTemplateWithInset",
                                        [
                                        1
                                        ]
                                ]
                        ]
                ]
```

Their final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
```

However, creating a frame by itself is not going to be of any help.  
`CreateFrame()` holds functions in a table, known as `methods`, which will allow the frame to have dimensions, positioning, interactibility, etc.  

While the `CreateFrame()`'s Methods are also quite lengthy and will be reserve for their own document, some important ones will be covered.  
They're utilized by connecting the base (in this case, the function which is assigned to a variable) and function with a colon (`:`).

|Factor|CreateFrame():Method|
|Dimensions|SetSize()|
|Positioning|SetPoint()|
|Text|SetText()| <-=-- WRONG
|Visibility|Show()/Hide()|
|Interactibility|EnableMouse()/RegisterForDrag()|
|Moving|StartMoving()/StopMovingOrSizing()|
|Functionality|SetScript()

See below for `SetSize()`'s syntax, intricacies listed in the separate framework document.  

```lua
SetSize() -- Base Function
        width, -- Argument #1; NUMERIC; in pixels (px), the "X"
                height -- Argument #2; NUMERIC; in pixels (px), the "Y"
```

The frame will be `500` px x `350` px, Author's deconstructed Lua entry as seen below.  

```lua
SetSize()
        500,
                350
```

Author's final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
```

See below for `SetPoint()`'s syntax, intricacies listed in the separate framework document.  

```lua
SetPoint() -- Base Function
        point, -- Argument #1;  STRING; "TOPLEFT", "BOTTOM", etc.
                [
                relativeTo, -- Argument #2 (Optional); STRING; Name of defined Frame.
                        [
                        relativePoint, -- Argument #3 (Optional, needs 'relativePoint'); STRING;  "TOPLEFT", "BOTTOM", etc.
                        ]
                ]
                [
                offsetX, -- Argument #4 (required if 'offsetY' is defined); NUMERIC; If positive, offset left; if negative, offset right.
                offSetY -- Argument #5 (required if 'offsetX' is defined; NUMERIC; If positive, offset upwards; If negative, offset downwards.
                ]
```

The frame's center will be the focal point, which is then centered on the base-game (`UIParent`) frame, off-setted 150 px (pixels) right and 200 px (pixels) down.  
Author's deconstructed Lua entry as seen below.  

```lua
SetPoint() -- Base Function
        "CENTER", -- Argument #1;  STRING; "TOPLEFT", "BOTTOM", etc.
                [
                UIParent, -- Argument #2 (Optional); STRING; Name of Frame's Assigned Variable.
                        [
                        "CENTER", -- Argument #3 (Optional, needs 'relativePoint'); STRING;  "TOPLEFT", "BOTTOM", etc.
                        ]
                ]
                [
                150, -- Argument #4 (required if 'offsetY' is defined); NUMERIC; If positive, offset left; if negative, offset right.
                -200 -- Argument #5 (required if 'offsetX' is defined; NUMERIC; If positive, offset upwards; If negative, offset downwards.
                ]
```

Author's final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
BaseFrame:SetPoint("CENTER", UIParent, "CENTER", 150,  -200)
```

<IMAGE SHOWN HERE>

To title the frame in-game, a shorthand method is used below, syntax shown below with intracacies reserved for the Framework document.  

`"BasicFrameTemplateWithInset"` has a region within its table called `TitleBg`.  
As this is not a function, it is simply a concatenated variable and is treated as such, signified by a dot (`.`) as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame.TitleBg -- Inoperable on its own.
```

The dimensions are set by its parent frame.  
While the width is great to copy, the height is not.  

To set an object's individual dimensions, the `SetWidth()` and `SetHeight()` Methods can be used.  
Their syntax is as seen below.

```lua
SetWidth() -- Base Function
        width -- Argument #1;  NUMERIC

SetHeight() -- Base Function
        height -- Argument #1;  NUMERIC
```

Author decided their TitleBg's height will be 30 px (pixels) tall.  
Author's final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
BaseFrame:SetPoint("CENTER", UIParent, "CENTER", 150,  -200)
BaseFrame.TitleBg:SetHeight(30)
```

In this `TitleBg` area, we need to put some text of what we'd like.  
Author decided to put their AddOn's name in its branded colors.  

For this, the `CreateFontString()` method is required.  
See below for `CreateFontString()`'s syntax. 

```lua
Variable_FontStringName = 
CreateFontString() -- Base Function
                [
                name, -- Argument #1 (required if `drawLayer` or `templateName` are defined); STRING; Assign a variable for Methods to reference ('nil' for anonymous).
                drawLayer, -- Argument #2 (required if 'name' or `templateName` are defined); STRING; "BACKGROUND", "BORDER", etc.
                templateName -- Argument #3 (required if 'name' or `drawLayer` are defined); STRING.
                ]
```

Author's deconstructed Lua entry as seen below.  

```lua
WintergreenTitleText = 
CreateFontString() -- Base Function
                [
                nil, 
                "OVERLAY",
                "GameFontHighlight"
                ]
```

Author's final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
BaseFrame:SetPoint("CENTER", UIParent, "CENTER", 150,  -200)
BaseFrame.TitleBg:SetHeight(30)
BaseFrame.WintergreenTitleText = BaseFrame:CreateFontString(nil, "OVERLAY","GameFontHighlight")
```

Note that the FontString was created but still must be positioned.  
This mirrors the exact same thing as needed to be done for the BaseFrame itself.  

For this FontString, it will be in the TitleBg box.  
Author decided its center will be anchored to the top right of the TitleBg box, offset left by 20 px (pixels) and offset up by 15 px (pixels).

Author's final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
BaseFrame:SetPoint("CENTER", UIParent, "CENTER", 150,  -200)
BaseFrame.TitleBg:SetHeight(30)
BaseFrame.WintergreenTitleText = BaseFrame:CreateFontString(nil, "OVERLAY","GameFontHighlight")
BaseFrame.WintergreenTitleText:SetPoint("CENTER", BaseFrame.TitleBg, "TOPRIGHT", -20, 15)
```

Now that the FontString is in place, actual text must be applied to it.  
For that, the `SetText()` Method must be used, see below for its syntax.  

```lua
SetText() -- Base Function
        string -- Argument #1;  STRING; MAX: 30,000 characters, requires pre-determined FONT.
```

<Did I already define my colored branding title? If not, do that in printing for a fun example :D>
Author decided to name their `Variable_FontStringName`, `WintergreenTitleText` and assign it to their variable of branded colors AddOn title.  
Author's final Lua entry is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
BaseFrame:SetPoint("CENTER", UIParent, "CENTER", 150,  -200)
BaseFrame.TitleBg:SetHeight(30)
BaseFrame.WintergreenTitleText = BaseFrame:CreateFontString(nil, "OVERLAY","GameFontHighlight")
BaseFrame.WintergreenTitleText:SetPoint("CENTER", BaseFrame.TitleBg, "TOPRIGHT", -20, 15)
local WintergreenBrandedText = "|cffffffffW|r|cffe6fff5i|r|cffccffebn|r|cffb3ffe2t|r|cff99ffd8e|r|cff80ffcer|r|cff66ffc4g|r|cff4dffbar|r|cff33ffb1e|r|cff19ffa7e|r|cff00ff9dn|r"
BaseFrame.WintergreenTitleText:SetText(WintergreenBrandedText)
```

<IMAGE SHOWN HERE> (& RETROACTIVELY AFTER EACH ADDITION)

The close button does help tremendously, though the window will appear after every loading screen.  
Luckily, its visibility can be change with the `Show()` and `Hide()` method.  

Neither the `Show()` or `Hide()` method have any arguments.  
Frames are shown by default so the `Show()` method is only necessary if the `Hide()` method is used.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:Hide()
BaseFrame:Show()
```

For now, Author is not hiding the BaseFrame.  
Making the frame interactable besides the close button can be done with a plethora of methods.  

To allow dragging the BaseFrame, multiple methods come into play.  

The mouse must be allowed to interact with the Frame.  
The Frame must register dragging motions and be movable.  

Most importantly, the drag must have a specific mouse button trigger its drag features.  
When dragged, it should signal the Frame to move, and to stop moving when no longer being dragged.

The `EnableMouse()`, `RegisterForDrag()`, SetMovable()`, `SetScript()`, and `StartMoving()` Methods have their syntax described below, with intracacies detailed in the Framework document.  
`StopMovingOrSizing()` has no arguments.  

```lua
EnableMouse() -- Base Function
                [
                  enable -- Argument #1; BOOLEAN; `false` by default
                ]
```

```lua
SetMovable() -- Base Function
                [
                  movable-- Argument #1; BOOLEAN; `false` by default
                ]
```

```lua
RegisterForDrag() -- Base Function
                [
                  ... (buttons) -- Argument #1; STRING; "LeftButton", "RightButton", "MiddleButton", "Button4", "Button5"
                ]
```

```lua
SetScript() -- Base Function
        scriptTypeName, -- Argument #1;  STRING; "OnShow", "OnDrag", etc.
                [
                script -- Argument #2 (Optional); FUNCTION; Name of script handler to call (or 'nil' to remove all scripts).
                ]
```

```lua
StartMoving() -- Base Function
                [
                  alwaysStartFromMouse -- Argument #1; BOOLEAN; `false` by default
                ]
```

Author's deconstructed Lua is as seen below.  


```lua
EnableMouse()
                [
                  true
                ]
```

```lua
SetMovable()
                [
                  true
                ]
```

```lua
RegisterForDrag()
                [
                  "LeftButton"
                ]
```

```lua
SetScript()
        "OnDragStart",
                [
                function(self)
                                self:StartMoving()
                ]

SetScript()
        "OnDragStop",
                [
                function(self)
                                self:StopMovingOrSizing()
                ]
```

Author's above `EnableMouse()`, `SetMovable()`, `RegisterForDrag()`, and `SetScript()`'s final Lua is as seen below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:EnableMouse(true)
BaseFrame:SetMovable(true)
BaseFrame:RegisterForDrag("LeftButton")
BaseFrame:SetScript("OnDragStart",function(self);self:StartMoving())
BaseFrame:SetScript("OnDragStop",function(self);self:StopMovingOrSizing()
```

Author's final Lua is as seen below. 

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
BaseFrame:SetSize(500,350)
BaseFrame:SetPoint("CENTER", UIParent, "CENTER", 150,  -200)
BaseFrame.TitleBg:SetHeight(30)
BaseFrame.WintergreenTitleText = BaseFrame:CreateFontString(nil, "OVERLAY","GameFontHighlight")
BaseFrame.WintergreenTitleText:SetPoint("CENTER", BaseFrame.TitleBg, "TOPRIGHT", -20, 15)
local WintergreenBrandedText = "|cffffffffW|r|cffe6fff5i|r|cffccffebn|r|cffb3ffe2t|r|cff99ffd8e|r|cff80ffcer|r|cff66ffc4g|r|cff4dffbar|r|cff33ffb1e|r|cff19ffa7e|r|cff00ff9dn|r"
BaseFrame.WintergreenTitleText:SetText(WintergreenBrandedText)
BaseFrame:EnableMouse(true)
BaseFrame:SetMovable(true)
BaseFrame:RegisterForDrag("LeftButton")
BaseFrame:SetScript("OnDragStart",function(self);self:StartMoving())
BaseFrame:SetScript("OnDragStop",function(self);self:StopMovingOrSizing()
```

To make the above more human friendly, comments and indentation were added.  
See Author's final BaseFrame code below.  

```lua
BaseFrame = CreateFrame("Frame", "BaseFrame", UIParent, "BasicFrameTemplateWithInset", 1)
        BaseFrame:SetSize(
                500, -- pixels (px), Width
                1)   -- pixels (px), Height
        BaseFrame:SetPoint(
                "CENTER", -- of BaseFrame
                        UIParent, "CENTER", -- attached to Center of UIParent (Game Screen)
                                150, -- pixels (px), Offset (Right)
                              -200) -- pixels (px), Offset (Down)
        BaseFrame.TitleBg:SetHeight(
                20)  -- pixels (px)
        BaseFrame.WintergreenTitleText = BaseFrame:CreateFontString(nil, "OVERLAY","GameFontHighlight")
                BaseFrame.WintergreenTitleText:SetPoint(
                        "CENTER", -- of WintergreenTitleText
                        BaseFrame.TitleBg, "TOPRIGHT", -- attached to Top Right of TitleBg
                              -20, -- pixels (px), Offset (Left)
                                 1)  -- pixels (px), Offset (Up)
                local WintergreenBrandedText = "|cffffffffW|r|cffe6fff5i|r|cffccffebn|r|cffb3ffe2t|r|cff99ffd8e|r|cff80ffcer|r|cff66ffc4g|r|cff4dffbar|r|cff33ffb1e|r|cff19ffa7e|r|cff00ff9dn|r"
                BaseFrame.WintergreenTitleText:SetText(WintergreenBrandedText)
BaseFrame:EnableMouse(true)
BaseFrame:SetMovable(true)
        BaseFrame:RegisterForDrag("LeftButton")
                BaseFrame:SetScript("OnDragStart",function(self);self:StartMoving())
                BaseFrame:SetScript("OnDragStop",function(self);self:StopMovingOrSizing())
```

---

<Last Part of #2, Going to Loop Into Slash Commands>

```lua
mainFrame:SetScript("OnShow", function()
        PlaySound(808)
end)

mainFrame:SetScript("OnHide", function()
        PlaySound(808)
end)
```

---

### Additional Resources Referenced

[Wikipedia | Syntactic Sugar](https://en.wikipedia.org/wiki/Syntactic_sugar)
[GitHub | Blizzard Interface Resources [Templates.lua]](https://github.com/Ketho/BlizzardInterfaceResources/blob/live/Resources/Templates.lua)

---

**Source Material**
<sub>**[Creating a WoW Addon - Part 2: Creating a Frame](https://www.reddit.com/r/wowaddondev/comments/1cc2qgj/creating_a_wow_addon_part_2_creating_a_frame/)**</sub>
<sub>**Wednesday, April 24, 2024 @ 12:33:00 PM EDT**</sub>


---

FOR DIFFERENT DOCUMENTS

---
---

FrameStrata!

https://warcraft.wiki.gg/wiki/Frame_Strata
WORLD
BACKGROUND
LOW
MEDIUM
HIGH
DIALOG
FULLSCREEN
FULLSCREEN_DIALOG
TOOLTIP

WORLD is reserved for the world frame and cannot be assigned.
Frames further partition the z axis into Layers when drawing a LayeredRegion (e.g. Texture or FontString).
Every frame defaults to appearing slightly above its parent, sharing the same strata but having one level higher.
Set a frame's strata using:
Frame:SetFrameStrata(frameStrata)
Frame frameStrata.FRAMESTRATA
Set a frame's level using:
Frame:SetFrameLevel(frameLevel) to choose any value
Frame:Raise() or Frame toplevel.true to increase frameLevel to one higher than existing frames which were previously in front but within the same frameStrata
Frame:Lower() for the opposite (no equivalent in XML)
Frame useParentLevel.true to make frameLevel the same as the parent frame (instead of normally being one higher)
When a parent frame changes its level, the descendant frames will change levels respectively (e.g. if a child frame was set 2 levels higher than its parent, it will shift 2 levels higher after the parent moves)
If this effect would cause a frame level to be lower than 0 it will instead be set to 10000


Layers

https://warcraft.wiki.gg/wiki/Layer

BACKGROUND
BORDER
ARTWORK
OVERLAY
HIGHLIGHT (see details)

When one frame is in front of another (according to its Frame Strata), all of its LayeredRegions will also be in front -- in otherwords, layers are part of each frame.
Setting Frame:EnableMouse() causes HIGHLIGHT to show/hide as the cursor hovers the Frame.
Transparent overlapping textures display different results depending on their relative ordering. For consistent results, use a blend mode of ADD or MOD on both textures.

---

Some Methods within the Frames created are `SetSize()`, `SetPoint()`, `SetText()`, `Hide()`, `Show()`, `EnableMouse()`, `SetMovable()`, `RegisterForDrag()`, `PlaySound()`, `StartMoving()`, `StopMovingOrSizing()`, and `SetScript()`.  

-- [Simple Frame API](https://warcraft.wiki.gg/wiki/Category:API_systems/SimpleFrameAPI)
--> Hide, SetMovable, RegisterForDrag, StartMoving, StopMoving, Show

-- [Simple Script Region Resizing API](https://warcraft.wiki.gg/wiki/Category:API_systems/SimpleScriptRegionResizingAPI)
--> SetPoint, SetSize, 

-- [Simple Script Region API](https://warcraft.wiki.gg/wiki/Category:API_systems/SimpleScriptRegionAPI)
--> EnableMouse, 
-- [PlaySound](https://warcraft.wiki.gg/wiki/API:PlaySound)

-- [FontStringSetText](https://warcraft.wiki.gg/wiki/API:FontString_SetText)

[Blizzard_SharedXML/SharedUIPanelTemplates.xml | 437:469](https://www.townlong-yak.com/framexml/latest/Blizzard_SharedXML/SharedUIPanelTemplates.xml#315)

---

https://www.townlong-yak.com/framexml/latest/Blizzard_UIPanelTemplates/UIPanelTemplates.xml#508
508-664
```xml
<!--
*******************************************************************************
    BasicFrameTemplate
  This is an empty frame with a titlebar and a close button.
*******************************************************************************
-->
  <Frame name="BaseBasicFrameTemplate" virtual="true">
    <Layers>
      <Layer level="OVERLAY">
        <Texture parentKey="TopLeftCorner" inherits="UI-Frame-TopLeftCorner">
          <Anchors>
            <Anchor point="TOPLEFT" x="-6" y="1"/>
          </Anchors>
        </Texture>
        <Texture parentKey="TopRightCorner" inherits="UI-Frame-TopCornerRight">
          <Anchors>
            <Anchor point="TOPRIGHT" x="0" y="1"/>
          </Anchors>
        </Texture>
        <Texture parentKey="TopBorder" inherits="_UI-Frame-TitleTile">
          <Anchors>
            <Anchor point="TOPLEFT" relativeKey="$parent.TopLeftCorner" relativePoint="TOPRIGHT"/>
            <Anchor point="TOPRIGHT" relativeKey="$parent.TopRightCorner" relativePoint="TOPLEFT"/>
          </Anchors>
        </Texture>
        <FontString parentKey="TitleText" inherits="GameFontNormal" text="">
          <Anchors>
            <Anchor point="TOP" x="-6" y="-4" />
          </Anchors>
        </FontString>
      </Layer>
      <Layer level="BORDER">
        <Texture parentKey="BotLeftCorner" inherits="UI-Frame-BotCornerLeft">
          <Anchors>
            <Anchor point="BOTTOMLEFT" x="-6" y="-5"/>
          </Anchors>
        </Texture>
        <Texture parentKey="BotRightCorner" inherits="UI-Frame-BotCornerRight">
          <Anchors>
            <Anchor point="BOTTOMRIGHT" x="0" y="-5"/>
          </Anchors>
        </Texture>
        <Texture parentKey="BottomBorder" inherits="_UI-Frame-Bot">
          <Anchors>
            <Anchor point="BOTTOMLEFT" relativeKey="$parent.BotLeftCorner" relativePoint="BOTTOMRIGHT" y="0"/>
            <Anchor point="BOTTOMRIGHT" relativeKey="$parent.BotRightCorner" relativePoint="BOTTOMLEFT" y="0"/>
          </Anchors>
        </Texture>
        <Texture parentKey="LeftBorder" inherits="!UI-Frame-LeftTile">
          <Anchors>
            <Anchor point="TOPLEFT" relativeKey="$parent.TopLeftCorner" relativePoint="BOTTOMLEFT"/>
            <Anchor point="BOTTOMLEFT" relativeKey="$parent.BotLeftCorner" relativePoint="TOPLEFT"/>
          </Anchors>
        </Texture>
        <Texture parentKey="RightBorder" inherits="!UI-Frame-RightTile">
          <Anchors>
            <Anchor point="TOPRIGHT" relativeKey="$parent.TopRightCorner" relativePoint="BOTTOMRIGHT" x="1"/>
            <Anchor point="BOTTOMRIGHT" relativeKey="$parent.BotRightCorner" relativePoint="TOPRIGHT"/>
          </Anchors>
        </Texture>
      </Layer>
    </Layers>
    <Frames>
      <Button parentKey="CloseButton" inherits="UIPanelCloseButtonDefaultAnchors"/>
    </Frames>
  </Frame>
 
  <Frame name="BasicFrameTemplate" inherits="BaseBasicFrameTemplate" virtual="true">
    <Layers>
      <Layer level="BACKGROUND" textureSubLevel="-1">
        <Texture parentKey="Bg" file="Interface\FrameGeneral\UI-Background-Rock" horizTile="true" vertTile="true">
          <Anchors>
            <Anchor point="TOPLEFT" x="2" y="-21"/>
            <Anchor point="BOTTOMRIGHT" x="-2" y="2"/>
          </Anchors>
        </Texture>
        <Texture parentKey="TitleBg" inherits="_UI-Frame-TitleTileBg">
          <Anchors>
            <Anchor point="TOPLEFT" x="2" y="-1"/>
            <Anchor point="TOPRIGHT" x="-25" y="-1"/>
          </Anchors>
        </Texture>
      </Layer>
      <Layer level="BACKGROUND">
        <Texture parentKey="TopTileStreaks" inherits="_UI-Frame-TopTileStreaks">
          <Anchors>
            <Anchor point="TOPLEFT" x="0" y="-21"/>
            <Anchor point="TOPRIGHT" x="-2" y="-21"/>
          </Anchors>
        </Texture>
      </Layer>
    </Layers>
  </Frame>
 
  <Frame name="BasicFrameTemplateWithInset" inherits="BasicFrameTemplate" virtual="true">
    <Layers>
      <Layer level="BACKGROUND" textureSubLevel="1">
        <Texture parentKey="InsetBg" file="Interface\FrameGeneral\UI-Background-Marble" horizTile="true" vertTile="true">
          <Anchors>
            <Anchor point="TOPLEFT" x="4" y="-24" />
            <Anchor point="BOTTOMRIGHT" x="-6" y="4" />
          </Anchors>
        </Texture>
      </Layer>
      <Layer level="BORDER" textureSubLevel="-1">
        <Texture parentKey="InsetBorderTopLeft" inherits="UI-Frame-InnerTopLeft">
          <Anchors>
            <Anchor point="TOPLEFT" relativeKey="$parent.InsetBg"/>
          </Anchors>
        </Texture>
 
        <Texture parentKey="InsetBorderTopRight" inherits="UI-Frame-InnerTopRight">
          <Anchors>
            <Anchor point="TOPRIGHT" relativeKey="$parent.InsetBg"/>
          </Anchors>
        </Texture>
 
        <Texture parentKey="InsetBorderBottomLeft" inherits="UI-Frame-InnerBotLeftCorner">
          <Anchors>
            <Anchor point="BOTTOMLEFT" relativeKey="$parent.InsetBg" y="-1"/>
          </Anchors>
        </Texture>
 
        <Texture parentKey="InsetBorderBottomRight" inherits="UI-Frame-InnerBotRight">
          <Anchors>
            <Anchor point="BOTTOMRIGHT" relativeKey="$parent.InsetBg" y="-1"/>
          </Anchors>
        </Texture>
 
        <Texture parentKey="InsetBorderTop" inherits="_UI-Frame-InnerTopTile">
          <Anchors>
            <Anchor point="TOPLEFT" relativeKey="$parent.InsetBorderTopLeft" relativePoint="TOPRIGHT"/>
            <Anchor point="TOPRIGHT" relativeKey="$parent.InsetBorderTopRight" relativePoint="TOPLEFT"/>
          </Anchors>
        </Texture>
        <Texture parentKey="InsetBorderBottom" inherits="_UI-Frame-InnerBotTile">
          <Anchors>
            <Anchor point="BOTTOMLEFT" relativeKey="$parent.InsetBorderBottomLeft" relativePoint="BOTTOMRIGHT"/>
            <Anchor point="BOTTOMRIGHT" relativeKey="$parent.InsetBorderBottomRight" relativePoint="BOTTOMLEFT"/>
          </Anchors>
        </Texture>
        <Texture parentKey="InsetBorderLeft" inherits="!UI-Frame-InnerLeftTile">
          <Anchors>
            <Anchor point="TOPLEFT" relativeKey="$parent.InsetBorderTopLeft" relativePoint="BOTTOMLEFT" x="0" y="0" />
            <Anchor point="BOTTOMLEFT" relativeKey="$parent.InsetBorderBottomLeft" relativePoint="TOPLEFT"/>
          </Anchors>
        </Texture>
        <Texture parentKey="InsetBorderRight" inherits="!UI-Frame-InnerRightTile">
          <Anchors>
            <Anchor point="TOPRIGHT" relativeKey="$parent.InsetBorderTopRight" relativePoint="BOTTOMRIGHT"/>
            <Anchor point="BOTTOMRIGHT" relativeKey="$parent.InsetBorderBottomRight" relativePoint="TOPRIGHT"/>
          </Anchors>
        </Texture>
      </Layer>
    </Layers>
  </Frame>

```

```lua
["BasicFrameTemplateWithInset"] = {type = "Frame", inherits = "BasicFrameTemplate"},
["BasicFrameTemplate"] = {type = "Frame", inherits = "BaseBasicFrameTemplate"},
```

Template has: Close Button, Title Bar, Background, Border.
---

Blizzard already has set API and templates for specific types of frames, as shown below.  

|API Systems: `Frame`|Example|
|-|-|
|**`CommentatorFrame`**||
|**`CompactUnitFrames`**||
|**`FrameAPIArchaeologyDigSiteFrame`**||
|**`FrameAPIBlob`**||
|**``FrameAPICharacterModelBase**||
|**`FrameAPICinematicModel`**||
|**`FrameAPICooldown`**||
|**`FrameAPIDressUpModel`**||
|**`FrameAPIFogOfWarFrame`**||
|**`FrameAPIModelSceneFrame`**||
|**`FrameAPIModelSceneFrameActor`**||
|**`FrameAPIModelSceneFrameActorBase`**||
|**`FrameAPINamePlate`**||
|**`FrameAPIQuestPOI`**||
|**`FrameAPIScenarioPOI`**||
|**`FrameAPISimpleCheckout`**||
|**`FrameAPITabardModel`**||
|**`FrameAPITabardModelBase`**||
|**`FrameAPITooltip`**||
|**`FrameAPIUnitPositionFrame`**||
|**`FrameScript`**||
|**`LootFrame`**||
|**`HousingFixturePointFrameAPI`**||
|**`HousingLayoutPinFrameAPI`**||


CreateFrame("Frame"), all start with `Frame:`
|`**UIOBJECT_Frame**`|Arguments|
|-|-|
|AbortDrag||
|AddRoleset|roleset|
|CanChangeAttribute|: canChangeAttributes|
|ClearAlphaGradient||
|ClearAttribute|attributeName : cleared|
|ClearAttributes||
|CreateFontString|[name, drawLayer, templateName] : line|
|CreateLine|[name, drawLayer, templateName, subLevel] : line|
|CreateMaskTexture|[name, drawLayer, templateName, subLevel] : maskTexture|
|CreateTexture|[name, drawLayer, templateName, subLevel] : texture|
|CreateVectorGraphics|[name[, drawLayer[, templateName[, subLevel]]]] : vectorGraphics|
|DesaturateHierarchy|desaturation, [, excludeRoot]|
|DisableDrawLayer|layer|
|DoesClipChildren|: clipsChildren|


---

Methods - https://warcraft.wiki.gg/wiki/UIOBJECT_Frame (x3)

Frame:AbortDrag()
Frame:AddRoleset(roleset)
Frame:CanChangeAttribute() : canChangeAttributes
Frame:ClearAlphaGradient()
Frame:ClearAttribute(attributeName) : cleared
Frame:ClearAttributes()
Frame:CreateFontString([name, drawLayer, templateName]) : line - Creates a fontstring.
Frame:CreateLine([name, drawLayer, templateName, subLevel]) : line - Draws a line.
Frame:CreateMaskTexture([name, drawLayer, templateName, subLevel]) : maskTexture - Creates a mask texture.
Frame:CreateTexture([name, drawLayer, templateName, subLevel]) : texture - Creates a texture.
Frame:CreateVectorGraphics([name [, drawLayer [, templateName [, subLevel]]]]) : vectorGraphics
Frame:DesaturateHierarchy(desaturation [, excludeRoot])
Frame:DisableDrawLayer(layer) - Prevents display of the frame on the specified draw layer.
Frame:DoesClipChildren() : clipsChildren
Frame:DoesHyperlinkPropagateToParent() : canPropagate
Frame:EnableDrawLayer(layer) - Allows display of the frame on the specified draw layer.
Frame:EnableGamePadButton([enable]) #secureframe - Allows the receipt of gamepad button inputs for this frame.
Frame:EnableGamePadStick([enable]) #secureframe - Allows the receipt of gamepad stick inputs for this frame.
Frame:EnableKeyboard([enable]) #secureframe - Allows this frame to receive keyboard input.
Frame:ExecuteAttribute(attributeName [, ...arguments]) : success, ...returns
Frame:GetAlpha() : alpha
Frame:GetAttribute(attributeName) : value - Returns the value of a secure frame attribute.
Frame:GetBoundsRect() : left, bottom, width, height - Returns the calculated bounding box of the frame and all of its descendant regions.
Frame:GetChildren() : ...children - Returns a list of child frames belonging to the frame.
Frame:GetClampRectInsets() : left, right, top, bottom - Returns the frame's clamp rectangle offsets.
Frame:GetDontSavePosition() : dontSave
Frame:GetEffectiveAlpha() : effectiveAlpha - Returns the effective alpha after propagating from the parent region.
Frame:GetEffectivelyFlattensRenderLayers() : flatten - Returns true if render layer flattening has been implicitly enabled.
Frame:GetEffectiveScale() : effectiveScale - Returns the effective scale after propagating from the parent region.
Frame:GetFlattensRenderLayers() : flatten - Returns true if render layer flattening has been enabled.
Frame:GetFrameLevel() : frameLevel - Returns the frame level of the frame.
Frame:GetFrameStrata() : strata - Returns the layering strata of the frame.
Frame:GetHighestFrameLevel([iterateAllChildren]) : frameLevel
Frame:GetHitRectInsets() : left, right, top, bottom - Returns the insets of the frame's hit rectangle.
Frame:GetHyperlinksEnabled() : enabled - Returns true if mouse interaction with hyperlinks on the frame is enabled.
Frame:GetID() : id - Returns the frame's numeric identifier.
Frame:GetNumChildren() : numChildren - Returns the number of child frames belonging to the frame.
Frame:GetNumRegions() : numRegions - Returns the number of non-Frame child regions belonging to the frame.
Frame:GetOnUpdateMode() : onUpdateMode
Frame:GetPropagateKeyboardInput() : propagate - Returns whether the frame propagates keyboard events.
Frame:GetRaisedFrameLevel() : frameLevel
Frame:GetRegions() : ...regions - Returns a list of non-Frame child regions belonging to the frame.
Frame:GetResizeBounds() : minWidth, minHeight, maxWidth, maxHeight - Returns the minimum and maximum size of the frame for user resizing.
Frame:GetRolesetNames() : rolesets
Frame:GetScale() : frameScale
Frame:GetWindow() : Functionindow
Frame:HasAlphaGradient() : hasAlphaGradient
Frame:HasFixedFrameLevel() : isFixed
Frame:HasFixedFrameStrata() : isFixed
Frame:Hide() #secureframe
Frame:InterceptStartDrag(delegate)
Frame:IsClampedToScreen() : clampedToScreen - Returns whether a frame is prevented from being moved off-screen.
Frame:IsDrawLayerEnabled(layer) : isEnabled
Frame:IsEventRegistered(eventName) : isRegistered, ...units - Returns whether a frame is registered to an event.
Frame:IsFrameBuffer() : isFrameBuffer
Frame:IsGamePadButtonEnabled() : enabled - Checks if this frame is configured to receive gamepad button inputs.
Frame:IsGamePadStickEnabled() : enabled - Checks if this frame is configured to receive gamepad stick inputs.
Frame:IsHighlightLocked() : locked
Frame:IsIgnoringChildrenForBounds() : ignore
Frame:IsIgnoringParentAlpha() : ignore
Frame:IsIgnoringParentScale() : ignore
Frame:IsKeyboardEnabled() : enabled - Returns true if keyboard interactivity is enabled for the frame.
Frame:IsMovable() : isMovable - Returns true if the frame is movable.
Frame:IsObjectLoaded() : isLoaded
Frame:IsResizable() : resizable - Returns true if the frame can be resized by the user.
Frame:IsRolesetFiltered() : isRolesetFiltered
Frame:IsShown() : isShown
Frame:IsToplevel() : isTopLevel - Returns whether this frame should raise its frame level on mouse interaction.
Frame:IsUserPlaced() : isUserPlaced - Returns whether the frame has been moved by the user.
Frame:IsUsingParentLevel() : usingParentLevel
Frame:IsVisible() : isVisible
Frame:LockHighlight() - Sets the frame or button to always be drawn highlighted.
Frame:Lower() #secureframe - Reduces the frame's frame level below all other frames in its strata.
Frame:Raise() #secureframe - Increases the frame's frame level above all other frames in its strata.
Frame:RegisterAllEvents() - Flags the frame to receive all events.
Frame:RegisterEvent(eventName) : registered - Registers the frame to an event.
Frame:RegisterEventCallback(eventName, cb) : registered
Frame:RegisterForDrag(...buttons) - Registers the frame for dragging with a mouse button.
Frame:RegisterUnitEvent(eventName, ...units) : registered - Registers the frame for a specific event, triggering only for the specified units.
Frame:RegisterUnitEventCallback(eventName, cb, ...units) : registered
Frame:RemoveRoleset(roleset)
Frame:ResizeToBoundsRect()
Frame:RotateTextures(radians [, x, y])
Frame:SetAlpha(alpha)
Frame:SetAlphaGradient(index, gradient)
Frame:SetAttribute(attributeName, value) #secureframe - Sets an attribute on the frame.
Frame:SetAttributeNoHandler(attributeName, value) #secureframe - Sets an attribute on the frame without triggering the OnAttributeChanged script handler.
Frame:SetClampedToScreen(clampedToScreen) #secureframe - Prevents the frame from moving off-screen.
Frame:SetClampRectInsets(left, right, top, bottom) #secureframe - Controls how much of the frame may be moved off-screen.
Frame:SetClipsChildren(clipsChildren)
Frame:SetDontSavePosition(dontSave)
Frame:SetDrawLayerEnabled(layer [, isEnabled])
Frame:SetFixedFrameLevel(isFixed) #secureframe
Frame:SetFixedFrameStrata(isFixed) #secureframe
Frame:SetFlattensRenderLayers(flatten) - Controls whether all subregions are composited into a single render layer.
Frame:SetFrameLevel(frameLevel) #secureframe - Sets the level at which the frame is layered relative to others in its strata.
Frame:SetFrameStrata(strata) #secureframe - Sets the layering strata of the frame.
Frame:SetHighlightLocked(locked)
Frame:SetHitRectInsets(left, right, top, bottom) #secureframe - Returns the insets of the frame's hit rectangle.
Frame:SetHyperlinkPropagateToParent(canPropagate)
Frame:SetHyperlinksEnabled([enabled]) #secureframe - Allows mouse interaction with hyperlinks on the frame.
Frame:SetID(id) #secureframe - Returns the frame's numeric identifier.
Frame:SetIgnoreParentAlpha(ignore)
Frame:SetIgnoreParentScale(ignore) #secureframe
Frame:SetIgnoringChildrenForBounds(ignore)
Frame:SetIsFrameBuffer(isFrameBuffer) - Controls whether or not a frame is rendered to its own framebuffer prior to being composited atop the UI.
Frame:SetMovable(movable) - Sets whether the frame can be moved.
Frame:SetOnUpdateMode(onUpdateMode)
Frame:SetPropagateKeyboardInput(propagate) #nocombat - Sets whether keyboard input is consumed by this frame or propagates to further frames.
Frame:SetResizable(resizable) - Sets whether the frame can be resized by the user.
Frame:SetResizeBounds(minWidth, minHeight [, maxWidth, maxHeight]) - Sets the minimum and maximum size of the frame for user resizing.
Frame:SetRolesets([rolesetsString])
Frame:SetScale(scale) #secureframe
Frame:SetShown([shown]) #secureframe
Frame:SetToplevel(topLevel) #secureframe - Controls whether or not a frame should raise its frame level on mouse interaction.
Frame:SetUserPlaced(userPlaced) - Sets whether a frame has been moved by the user and will be saved in the layout cache.
Frame:SetUsingParentLevel(usingParentLevel) #secureframe
Frame:SetWindow([window])
Frame:Show() #secureframe
Frame:StartMoving([alwaysStartFromMouse]) #secureframe - Begins repositioning the frame via mouse movement.
Frame:StartSizing([resizePoint, alwaysStartFromMouse]) #secureframe - Begins resizing the frame via mouse movement.
Frame:StopMovingOrSizing() #secureframe - Stops moving or resizing the frame.
Frame:UnlockHighlight() - Sets the frame or button to not always be drawn highlighted.
Frame:UnregisterAllEvents() - Unregisters all events from the frame.
Frame:UnregisterEvent(eventName) : registered - Unregisters an event from the frame.

---


---
ScriptRegion

ScriptRegion:CanChangeProtectedState() : canChange - Returns true if protected properties of the region can be changed by non-secure scripts.
ScriptRegion:CanPropagateMouseClicks() : canPropagate
ScriptRegion:CanPropagateMouseMotion() : canPropagate
ScriptRegion:ClearScripts()
ScriptRegion:CollapsesLayout() : collapsesLayout
ScriptRegion:EnableMouse([enable]) #secureframe - Sets whether the region should receive mouse input.
ScriptRegion:EnableMouseMotion([enable]) #secureframe - Sets whether the region should receive mouse hover events.
ScriptRegion:EnableMouseWheel([enable]) #secureframe - Sets whether the region should receive mouse wheel input.
ScriptRegion:GetBottom() : bottom #restrictedframe - Returns the offset to the bottom edge of the region.
ScriptRegion:GetCenter() : x, y #restrictedframe - Returns the offset to the center of the region.
ScriptRegion:GetHeight([ignoreRect]) : height - Returns the height of the region.
ScriptRegion:GetLeft() : left #restrictedframe - Returns the offset to the left edge of the region.
ScriptRegion:GetRect() : left, bottom, width, height #restrictedframe - Returns the coords and size of the region.
ScriptRegion:GetRight() : right #restrictedframe - Returns the offset to the right edge of the region.
ScriptRegion:GetRoundLayoutToNearestPixel() : enabled
ScriptRegion:GetScaledRect() : left, bottom, width, height - Returns the scaled coords and size of the region.
ScriptRegion:GetScript(scriptTypeName [, bindingType]) : script - Returns the widget script handler.
ScriptRegion:GetSize([ignoreRect]) : Functionidth, height - Returns the width and height of the region.
ScriptRegion:GetSourceLocation() : location - Returns the script name and line number where the region was created.
ScriptRegion:GetTop() : top #restrictedframe - Returns the offset to the top edge of the region.
ScriptRegion:GetWidth([ignoreRect]) : Functionidth - Returns the width of the region.
ScriptRegion:HasScript(scriptName) : hasScript - Returns true if the region supports the given script type.
ScriptRegion:Hide() #secureframe - Hides the region.
ScriptRegion:HookScript(scriptTypeName, script [, bindingType]) : success - Securely post-hooks a widget script handler.
ScriptRegion:Intersects(region) : intersects
ScriptRegion:IsAnchoringRestricted() : isRestricted - Returns true if the region has cross-region anchoring restrictions applied.
ScriptRegion:IsAnchoringSecret() : isSecret
ScriptRegion:IsCollapsed() : isCollapsed
ScriptRegion:IsDragging() : isDragging - Returns true if the region is being dragged.
ScriptRegion:IsMouseClickEnabled() : enabled - Returns true if the region can receive mouse clicks.
ScriptRegion:IsMouseEnabled() : enabled - Returns true if the region can receive mouse input.
ScriptRegion:IsMouseMotionEnabled() : enabled - Returns true if the region can receive mouse hover events.
ScriptRegion:IsMouseMotionFocus() : isMouseMotionFocus - Returns true if the mouse cursor is hovering over the region.
ScriptRegion:IsMouseOver([offsetTop [, offsetBottom [, offsetLeft [, offsetRight]]]]) : isMouseOver - Returns true if the mouse cursor is hovering over the region.
ScriptRegion:IsMouseWheelEnabled() : enabled - Returns true if the region can receive mouse wheel input.
ScriptRegion:IsProtected() : isProtected, isProtectedExplicitly - Returns whether the region is currently protected.
ScriptRegion:IsRectValid() : isValid - Returns true if the region can be positioned on the screen.
ScriptRegion:IsShown() : isShown - Returns true if the region should be shown; it depends on the parents if it's visible.
ScriptRegion:IsVisible() : isVisible - Returns true if the region and its parents are shown.
ScriptRegion:SetCollapsesLayout(collapsesLayout) #secureframe
ScriptRegion:SetMouseClickEnabled([enabled]) #secureframe - Sets whether the region should receive mouse clicks.
ScriptRegion:SetMouseMotionEnabled([enabled]) #secureframe - Sets whether the region should receive mouse hover events.
ScriptRegion:SetParent([parent]) #secureframe - Sets the parent of the region.
ScriptRegion:SetPassThroughButtons(...buttons) #nocombat - Allows the region to propagate mouse clicks to underlying regions or the world frame.
ScriptRegion:SetPropagateMouseClicks(propagate) #nocombat
ScriptRegion:SetPropagateMouseMotion(propagate) #nocombat
ScriptRegion:SetRoundLayoutToNearestPixel(enabled)
ScriptRegion:SetScript(scriptTypeName [, script]) - Sets the widget script handler.
ScriptRegion:SetShown([show]) #secureframe - Shows or hides the region.
ScriptRegion:ShouldButtonPassThrough(button) : shouldPassThrough
ScriptRegion:Show() #secureframe - Shows the region.
ScriptRegionResizing:AdjustPointsOffset(x, y) #secureframe - Adjusts the x and y offset of the region.
ScriptRegionResizing:ClearAllPoints() #secureframe - Removes all anchor points from the region.
ScriptRegionResizing:ClearPoint(point) #secureframe - Removes an anchor point from the region by name.
ScriptRegionResizing:ClearPointsOffset() #secureframe - Resets the x and y offset on the region to zero.
ScriptRegionResizing:GetNumPoints() : numPoints - Returns the number of anchor points for the region.
ScriptRegionResizing:GetPoint([anchorIndex [, resolveCollapsed]]) : point, relativeTo, relativePoint, offsetX, offsetY #restrictedframe - Returns an anchor point for the region.
ScriptRegionResizing:GetPointByName(point [, resolveCollapsed]) : point, relativeTo, relativePoint, offsetX, offsetY - Returns an anchor point by name for the region.
ScriptRegionResizing:SetAllPoints(relativeTo [, doResize]) #secureframe - Positions the region the same as another region.
ScriptRegionResizing:SetHeight(height) #secureframe - Sets the height of the region.
ScriptRegionResizing:SetPoint(point [, relativeTo [, relativePoint]] [, offsetX, offsetY]) #anchorfamily #secureframe - Sets an anchor point for the region.
ScriptRegionResizing:SetPointsOffset(x, y)
ScriptRegionResizing:SetSize(x, y) #secureframe - Sets the width and height of the region.
ScriptRegionResizing:SetWidth(width) #secureframe - Sets the width of the region.
AnimatableObject:CreateAnimationGroup([name [, templateName]]) : group - Creates an animation group.
AnimatableObject:GetAnimationGroups() : ...groups - Returns the animation groups of this region.
AnimatableObject:StopAnimating() - Stops any active animations on this region.
Object:ClearParentKey() - Clears the parent key.
Object:GetDebugName([preferParentKey]) : debugName - Returns the object's debug name.
Object:GetParent() : parent - Returns the parent object.
Object:GetParentKey() : parentKey - Returns the key on the parent that references this object.
Object:SetParentKey(parentKey [, clearOtherKeys]) - Sets a key on the parent to the child object.
FrameScriptObject:AddAccessRestrictions(restrictions)
FrameScriptObject:AddForbiddenAspects(aspects)
FrameScriptObject:AddSecretAspect(aspect)
FrameScriptObject:CanBeAccessedInContext() : canAccess
FrameScriptObject:GetAccessRestrictions() : restrictions
FrameScriptObject:GetForbiddenAspects() : aspects
FrameScriptObject:GetInheritableForbiddenAspects(path) : aspects
FrameScriptObject:GetName() : name - Returns the object's global name.
FrameScriptObject:GetObjectTable() : objectTable
FrameScriptObject:GetObjectType() : objectType - Returns the object's widget type.
FrameScriptObject:HasAccessConstraints() : hasAccessConstraints
FrameScriptObject:HasAnyAccessRestrictions([restrictions]) : hasAnyAccessRestriction
FrameScriptObject:HasAnyForbiddenAspects([aspects]) : hasAnyForbiddenAspect
FrameScriptObject:HasAnySecretAspect() : hasSecretAspect
FrameScriptObject:HasSecretAspect(aspect) : hasSecretAspect
FrameScriptObject:HasSecretValues() : hasSecretValues
FrameScriptObject:IsForbidden() : isForbidden - Returns whether this object has been explicitly marked as forbidden.
FrameScriptObject:IsObjectType(objectType) : isType - Returns true if the object belongs to a given widget type or its subtypes.
FrameScriptObject:IsPreventingSecretValues() : isPreventingSecretValues
FrameScriptObject:SetForbidden() #protected - Sets the object to be forbidden from an insecure execution path.
FrameScriptObject:SetToDefaults()

---

---
Script Types

OnAttributeChanged(self, key, value) - Invoked when a secure frame attribute is changed.
OnChar(self, text) - Invoked for each text character typed in the frame.
OnDisable(self) - Invoked when the frame is disabled.
OnDragStart(self, button) - Invoked when the mouse is dragged starting in the frame
OnDragStop(self) - Invoked when the mouse button is released after a drag started in the frame,
OnEnable(self) - Invoked when the frame is enabled.
OnEvent(self, event, ...) - Invoked whenever an event fires for which the frame is registered.
OnGamePadButtonDown(self, button) - Invoked when a gamepad button is pressed.
OnGamePadButtonUp(self, button) - Invoked when a gamepad button is released.
OnGamePadStick(self, stick, x, y, len) - Invoked when a gamepad stick is moved.
OnHyperlinkClick(self, link, text, button, region, left, bottom, width, height) - Invoked when the mouse clicks a hyperlink on the FontInstance object.
OnHyperlinkEnter(self, link, text, region, left, bottom, width, height) - Invoked when the mouse moves over a hyperlink on the FontInstance object.
OnHyperlinkLeave(self) - Invoked when the mouse moves away from a hyperlink on the FontInstance object.
OnKeyDown(self, key) - Invoked when a keyboard key is pressed if the frame is keyboard enabled.
OnKeyUp(self, key) - Invoked when a keyboard key is released if the frame is keyboard enabled.
OnReceiveDrag(self) - Invoked when the mouse button is released after dragging into the frame.
OnSizeChanged(self, width, height) - Invoked when a frame's size changes.
OnUpdate(self, elapsed) - Invoked on every frame.
OnShow(self) - Invoked when the widget is shown.
OnHide(self) - Invoked when the widget is hidden.
OnEnter(self, motion) - Invoked when the cursor enters the widget's interactive area.
OnLeave(self, motion) - Invoked when the mouse cursor leaves the widget's interactive area.
OnMouseDown(self, button) - Invoked when a mouse button is pressed while the cursor is over the widget.
OnMouseUp(self, button, upInside) - Invoked when the mouse button is released following a mouse down action in the widget.
OnMouseWheel(self, delta) - Invoked when the widget receives a mouse wheel scrolling action.
OnLoad(self) - Invoked when the widget is created.

---

Regardless of using a template or a creating a new frame entirely, they are comprised of  `XML` and arguments to the `CreateFrame()` function from the WoW API.  

---
XML IS GOING TO BE ITS OWN SECTION. 
https://warcraft.wiki.gg/wiki/XML/LayoutFrame
Frames - <LayoutFrame> (<Frame> inherited from <LayoutFrame>)

```xml
<LayoutFrame>
	<Size />
	<Anchors />
	<KeyValues />
	<Mixins />
	<ForbiddenAspects />
	<Animations />
</LayoutFrame>
```

name	xs:string?			Adds a reference to _G, substituting $parent with a parent's name
parentKey	xs:string?		Object:SetParentKey	Adds a reference to the widget's parent
parentArray	xs:string?			Inserts a reference to an array in the widget's parent
inherits	xs:string?			Inherits a comma-separated list of XML virtual templates
mixin	xs:string?			Inherits a comma-separated list of Lua mixins
secureMixin	xs:string?			Inherits a comma-separated list of Lua mixins, wrapping inherited functions to force secure execution
virtual	xs:boolean?	false		Creates an XML virtual template instead of a widget (requires name)
setAllPoints	xs:boolean?	false	ScriptRegionResizing:SetAllPoints	Sets the top-left and bottom-right anchors to match the parent widget
collapsesLayout	xs:boolean?	false	ScriptRegion:SetCollapsesLayout	
hidden	xs:boolean?	false	ScriptRegion:Hide
ScriptRegion:Show
ScriptRegion:SetShown	Controls the frame's initial visibility
alpha	xs:float?	1.0	Region:SetAlpha	
scale	xs:float?	1.0	Region:SetScale	
ignoreParentAlpha	xs:boolean?	false		
ignoreParentScale	xs:boolean?	false		
enableMouse	xs:boolean?	false	ScriptRegion:EnableMouse	Enables all mouse input
enableMouseClicks	xs:boolean?	false	ScriptRegion:SetMouseClickEnabled	Enables mouse clicks only
enableMouseMotion	xs:boolean?	false	ScriptRegion:EnableMouseMotion	Enables mouse motion only
registerForDrag	xs:string?		Frame:RegisterForDrag	
passThroughButtons	xs:string?		ScriptRegion:SetPassThroughButtons	
protected	xs:boolean?	false		Declares the frame protected for secure code execution
secureReferenceKey	xs:string?			
retainClickThroughOverride	xs:boolean?	false		
propagateMouseInput	ui:PROPAGATE_MOUSE?		ScriptRegion:SetPropagateMouseClicks	
propagateMouseInputMask	ui:PROPAGATE_MOUSE?		ScriptRegion:SetPropagateMouseClicks	
preventSecretValues	xs:boolean?	false		
parentPartition	Enum.ScriptObjectPartition?			Not used for addon devs. See 12.1.0 changes

Children
Name	Type	Default	Description
point	ui:FRAMEPOINT		Point to align
relativePoint	ui:FRAMEPOINT?		Point on the other widget to align against (defaults to the same as point)
relativeKey	xs:string?		Another widget to align against (sibling)
relativeTo	xs:string?		Another widget to align against (in _G)
x	xs:float?		Horizontal offset
y	xs:float?		Vertical offset


KeyValue
Name	Type	Default	Comment
key	xs:string		Key in the widget's table
value	xs:string		Value to be assigned
keyType	ui:KEYVALUETYPE?	string	Type of the key. Using 'nil' will cause an error
type	ui:KEYVALUETYPE?	string	Type of the value
targetPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes


Mixins
Name	Type	Default	Comment
key	xs:string		Key to the mixin table
inboundPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes
secureDelegates	boolean	false	
source	ui:TABLESOURCE?	auto	
targetPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes

-- <Frame> -- 
https://warcraft.wiki.gg/wiki/XML/Frame

```xml
<Frame>
 	<Frames />
	<HitRectInsets />
	<Layers />
	<Mixins />
	<ResizeBounds />
	<Scripts />
</Frame>
```

Name	Type	Default	Lua equivalent	Description
parent	xs:string?		ScriptRegion:SetParent	Make this frame a child of another
toplevel	xs:boolean?	false	Frame:SetToplevel	Renders in front
flattenRenderLayers	xs:boolean?	false	Frame:SetFlattensRenderLayers	Flattens child regions
useParentLevel	xs:boolean?	false	Frame:SetUsingParentLevel	Prevents incrementing the frame level above its parent
movable	xs:boolean?	false	Frame:SetMovable	Enables dragging
resizable	xs:boolean?	false	Frame:SetResizable	Enables resizing
frameStrata	ui:FRAMESTRATA?		Frame:SetFrameStrata	Sequences overlapping frames
frameLevel	xs:int?		Frame:SetFrameLevel	Further sequences overlapping frames in the same frameStrata
id	xs:int?	0	Frame:SetID	Assigns an id
enableKeyboard	xs:boolean?	false	Frame:EnableKeyboard	Enables keyboard input
clampedToScreen	xs:boolean?	false	Frame:SetClampedToScreen	Prevents dragging off screen
depth	xs:float?	0.0		
dontSavePosition	xs:boolean?	false	Frame:SetDontSavePosition	Prevents saving the position of a movable frame
propagateKeyboardInput	xs:boolean?	false	Frame:SetPropagateKeyboardInput	Propagates keyboard input to the parent frame
roundLayoutToNearestPixel	xs:boolean?	false	ScriptRegion:SetRoundLayoutToNearestPixel	When enabled, layout changes are automatically rounded to the nearest pixel
intrinsic	xs:boolean?	false		Creates an intrinsic frame
clipChildren	xs:boolean?	false	Frame:SetClipsChildren	Clips overflowing children
propagateHyperlinksToParent	xs:boolean?	false		Propagates hyperlink interaction to the parent frame
hyperlinksEnabled	xs:boolean?	false	Frame:SetHyperlinksEnabled	Enables interactive hyperlinks
fixedFrameStrata	xs:boolean?	false	Frame:SetFixedFrameStrata	
fixedFrameLevel	xs:boolean?	false	Frame:SetFixedFrameLevel	
frameBuffer	xs:boolean?	false	Frame:SetIsFrameBuffer	
jumpNavigateEnabled	xs:boolean?	false		
jumpNavigateStart	xs:string?	false		
ignoreChildrenForBounds	xs:boolean?	false	Frame:SetIgnoringChildrenForBounds	
onUpdateMode	Enum.OnUpdateMode?	visible	Frame:SetOnUpdateMode	
roleset	xs:string?		Frame:AddRoleset	

Attributes
name	xs:string?			Adds a reference to _G, substituting $parent with a parent's name
parentKey	xs:string?		Object:SetParentKey	Adds a reference to the widget's parent
parentArray	xs:string?			Inserts a reference to an array in the widget's parent
inherits	xs:string?			Inherits a comma-separated list of XML virtual templates
mixin	xs:string?			Inherits a comma-separated list of Lua mixins
secureMixin	xs:string?			Inherits a comma-separated list of Lua mixins, wrapping inherited functions to force secure execution
virtual	xs:boolean?	false		Creates an XML virtual template instead of a widget (requires name)
setAllPoints	xs:boolean?	false	ScriptRegionResizing:SetAllPoints	Sets the top-left and bottom-right anchors to match the parent widget
collapsesLayout	xs:boolean?	false	ScriptRegion:SetCollapsesLayout	
hidden	xs:boolean?	false	ScriptRegion:Hide
ScriptRegion:Show
ScriptRegion:SetShown	Controls the frame's initial visibility
alpha	xs:float?	1.0	Region:SetAlpha	
scale	xs:float?	1.0	Region:SetScale	
ignoreParentAlpha	xs:boolean?	false		
ignoreParentScale	xs:boolean?	false		
enableMouse	xs:boolean?	false	ScriptRegion:EnableMouse	Enables all mouse input
enableMouseClicks	xs:boolean?	false	ScriptRegion:SetMouseClickEnabled	Enables mouse clicks only
enableMouseMotion	xs:boolean?	false	ScriptRegion:EnableMouseMotion	Enables mouse motion only
registerForDrag	xs:string?		Frame:RegisterForDrag	
passThroughButtons	xs:string?		ScriptRegion:SetPassThroughButtons	
protected	xs:boolean?	false		Declares the frame protected for secure code execution
secureReferenceKey	xs:string?			
retainClickThroughOverride	xs:boolean?	false		
propagateMouseInput	ui:PROPAGATE_MOUSE?		ScriptRegion:SetPropagateMouseClicks	
propagateMouseInputMask	ui:PROPAGATE_MOUSE?		ScriptRegion:SetPropagateMouseClicks	
preventSecretValues	xs:boolean?	false		
parentPartition	Enum.ScriptObjectPartition?			Not used for addon devs. See 12.1.0 changes

Insets
Name	Type	Default	Comment
left	xs:int?		(+) padding or (-) overflow from the left edge, scaling dependent
right	xs:int?		(+) padding or (-) overflow from the right edge, scaling dependent
top	xs:int?		(+) padding or (-) overflow from the top edge, scaling dependent
bottom	xs:int?		(+) padding or (-) overflow from the bottom edge, scaling dependent

Layer
Name	Type	Default	Comment
level	ui:DRAWLAYER?	ARTWORK	Sequences graphical regions as "BACKGROUND", "BORDER", "ARTWORK", etc.
textureSubLevel	xs:int? [-8, 7]	0	Further sequences overlapping Texture widgets inside the same level

ScriptHandlers
Name	Type	Default	Comment
function	xs:string?		Name of a function instead of Lua code between the XML tags
method	xs:string?		Name of a widget method instead of Lua code between the XML tags
inherit	ui:SCRIPTINHERITTYPE?	none	Hooks (prepend, append) other scripts inherited through an XML virtual template
intrinsicOrder	ui:SCRIPTINTRINSICORDERTYPE?	none	Hooks (precall, postcall) other scripts when copied as an intrinsic frame
autoEnableInput	xs:boolean?	true	
targetPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes

Anchors
Name	Type	Default	Description
point	ui:FRAMEPOINT		Point to align
relativePoint	ui:FRAMEPOINT?		Point on the other widget to align against (defaults to the same as point)
relativeKey	xs:string?		Another widget to align against (sibling)
relativeTo	xs:string?		Another widget to align against (in _G)
x	xs:float?		Horizontal offset
y	xs:float?		Vertical offset

KeyValues
Name	Type	Default	Comment
key	xs:string		Key in the widget's table
value	xs:string		Value to be assigned
keyType	ui:KEYVALUETYPE?	string	Type of the key. Using 'nil' will cause an error
type	ui:KEYVALUETYPE?	string	Type of the value
targetPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes

Mixins
Name	Type	Default	Comment
key	xs:string		Key to the mixin table
inboundPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes
secureDelegates	boolean	false	
source	ui:TABLESOURCE?	auto	
targetPartition	Enum.ScriptObjectPartition?		Not used for addon devs. See 12.1.0 changes

<INTRINSIC FRAMES>
https://warcraft.wiki.gg/wiki/Intrinsic_frame

FrameXML Functions: https://warcraft.wiki.gg/wiki/FrameXML_functions
ShowUIPanel(frame, force)
PVEFrame_ToggleFrame() - Toggles the Group Finder.
ToggleAchievementFrame() - Shows the Achievements frame.
ToggleCharacter(index) - Toggles the character pane to the specified frame.
ToggleCollectionsJournal(index) - Toggles the Collections window.
ToggleEncounterJournal() - Toggles the Adventure Guide.
ToggleFriendsFrame([tabNumber]) - Opens/closes the friends pane, optionally on a specific tab.
ToggleGameMenu() - Opens/closes the game menu.
ToggleGuildFrame() - Toggles the Guild & Communites frame.
ToggleHelpFrame() - Opens the Help Request frame.
ToggleMinimap() - Turns the minimap display on/off.
TogglePVPUI() - Opens/closes the PvP frame.
ToggleSpellBook(bookType) - Shows the spellbook. Can show your spells or your pet's.
ToggleTalentFrame() - Opens the Talent frame.
AbbreviateLargeNumbers(value)
AbbreviateNumbers(value)

Mixins
CreateColor(r, g, b, a) - Returns a ColorMixin object.
CreateRectangle(left, right, top, bottom) - Returns a RectangleMixin object.
CreateVector2D(x, y) - Returns a Vector2DMixin object.
CreateVector3D(x, y, z) - Returns a Vector3DMixin object.
SpellMixin:CreateFromSpellID(spellID) - Returns a SpellMixin object.
Item:CreateFromItemID(itemID) - Returns an ItemMixin object.
ItemLocation:CreateFromBagAndSlot() - Returns an ItemLocationMixin object.
PlayerLocation:CreateFromGUID(guid) - Returns a PlayerLocationMixin object.
TransmogUtil.CreateTransmogLocation(slotDescriptor, transmogType, modification) - Returns a TransmogLocationMixin object.
CallbackRegistryMixin
AnchorMixin
AnimatedNumericFontStringMixin
DoublyLinkedListMixin
GridLayoutMixin
LineMixin
MapCanvasMixin
SecondsFormatterMixin
SparseGridMixin
TextureLoadingGroupMixin
CreateObjectPool(creationFunc, resetterFunc) - Creates a ObjectPoolMixin object for widgets.
CreateFramePool(frameType [, parent, frameTemplate, resetterFunc, forbidden]) - Creates a FramePoolMixin for Frames.
CreateTexturePool(parent [, layer, subLayer, textureTemplate, resetterFunc]) - Creates a TexturePoolMixin for Textures.
CreateFontStringPool(parent [, layer, subLayer, fontStringTemplate, resetterFunc]) - Creates a FontStringPoolMixin for FontStrings.
CreateActorPool(parent [, actorTemplate, resetterFunc]) - Creates an ActorPoolMixin for Actors.
CreateFramePoolCollection() - Creates a FramePoolCollectionMixin object for frame pools.

ChatFrameBase
ChatFrame
ChatFrame_AddChannel(chatFrame, channelName) - Activates channel in chatFrame.
ChatFrame_AddMessageEventFilter(event, filterFunc) - Adds a chat message filtering function.
ChatFrame_GetMessageEventFilters(event) - Retrieves the list of chat message filtering functions.
ChatFrame_OnHyperlinkShow(reference, link, button) - Called when the user clicks on a chatlink.
ChatFrame_RemoveMessageEventFilter(event, filterFunc) - Unregisters a chat message filtering function.

EquipmentManager
EquipmentManager
EquipmentManager_UnpackLocation() - Unpacks a location integer to determine the actual inventory location.
SharedXMLBase

FrameUtil
FrameUtil
UIFrameFadeIn(frame, timeToFade, startAlpha, endAlpha) - Fades a frame in.
UIFrameFadeOut(frame, timeToFade, startAlpha, endAlpha) - Fades a frame out.

TextureUtil
TextureUtil
CreateAtlasMarkup(atlasName [, height, width, offsetX, offsetY]) - Returns a texture fontstring for an atlas.
CreateTextureMarkup(file, fileWidth, fileHeight, width, height, left, right, top, bottom [, xOffset, yOffset]) - Returns a texture fontstring.
GetTextureInfo(obj) - Returns the type and info of a texture.

ContainerFrame
CloseAllBags(callingFrame, forceUpdate)
CloseBackpack()
CloseBag(bagID)
IsBagOpen(bagID)
OpenAllBags(callingFrame, forceUpdate)
OpenBackpack()
OpenBag(bagID, force)
ToggleAllBags()
ToggleBackpack() - Toggles your backpack open/closed.
ToggleBag(bagID) - Opens or closes the specified bag.

DressUpFrames
DressUpItemLink(itemLink) - Shows the Dressing Room with the given item equipped.
DressUpMountLink(itemLink | spellLink) - Shows the Dressing Room for the mount.
DressUpTransmogLink(transmogLink) - Shows the Dressing Room for transmog appearance or illusion.
SetDressUpBackground(frame, fileName, atlasPostfix)

TooltipUtil
TooltipUtil.ShouldDoItemComparison()
TooltipUtil.GetDisplayedItem(tooltip)
TooltipUtil.GetDisplayedSpell(tooltip)
TooltipUtil.GetDisplayedUnit(tooltip)
TooltipUtil.FindLinesFromGetter(lineTypeTable, getterName, ...)
TooltipUtil.FindLinesFromData(lineTypeTable, tooltipData)
TooltipUtil.DebugCopyGameTooltip()

UIParent
MouseIsOver(region, topOffset, bottomOffset, leftOffset, rightOffset) - Checks whether the mouse is over the frame (or within specified offsets).

AccountUtil
GameLimitedMode_IsActive()
GetClampedCurrentExpansionLevel()

AnchorUtil
AnchorUtil.CreateAnchor(point, relativeTo, relativePoint, x, y)
AnchorUtil.CreateGridLayout(direction, rowSize, spacingX, spacingY)
AnchorUtil.CreateAnchorFromPoint(region, pointIndex)
AnchorUtil.GridLayout(frames, initialAnchor, layout)
AnchorUtil.GridLayoutFactoryByCount(factoryFunction, count, initialAnchor, layout)
AnchorUtil.GridLayoutFactory(factoryFunction, initialAnchor, totalWidth, totalHeight, overrideDirection, overridePaddingX, overridePaddingY)
AnchorUtil.MirrorRegionsAlongVerticalAxis(mirrorDescriptions)
AnchorUtil.MirrorRegionsAlongHorizontalAxis(mirrorDescriptions)

AuraUtil
AuraUtil.FindAura(predicate, unit, filter, predicateArg1, predicateArg2, predicateArg3)
AuraUtil.FindAuraByName(auraName, unit, filter) - Finds the first aura that matches the name.
AuraUtil.ForEachAura(unit, filter, maxCount, func)
AuraUtil.ShouldSkipAuraUpdate(isFullUpdate, updatedAuraInfos, isRelevantFunc, ...)

ColorUtil
CreateColorFromHexString(hexColor)
CreateColorFromBytes(r, g, b, a)
AreColorsEqual(left, right)
GetClassColor(classFilename)
GetClassColorObj(classFilename)
GetClassColoredTextForUnit(unit, text)
GetFactionColor(factionGroupTag)

CVarUtil
RegisterCVar(name, value)
ResetTestCvars()
SetCVar(name, value, eventName) : success
GetCVar(name) : value
SetCVarBitfield(name, index, value, scriptCVar) : success
SetCVarToDefault(name) - Resets a CVar to default.
GetCVarBitfield(name, index) : boolean
GetCVarBool(name) : boolean
GetCVarDefault(name) : value

EasingUtil
EasingUtil.InQuadratic(percent)
EasingUtil.OutQuadratic(percent)
EasingUtil.InOutQuadratic(percent)
EasingUtil.InCubic(percent)
EasingUtil.OutCubic(percent)
EasingUtil.InOutCubic(percent)
EasingUtil.InQuartic(percent)
EasingUtil.OutQuartic(percent)
EasingUtil.InOutQuartic(percent)
EasingUtil.InQuintic(percent)
EasingUtil.OutQuintic(percent)
EasingUtil.InOutQuintic(percent)

ErrorUtil
CallErrorHandler(...)

EventRegistry
CallbackRegistryMixin:RegisterCallback(event, func, ...)
CallbackRegistryMixin:TriggerEvent(event, ...)
EventRegistry:RegisterFrameEventAndCallback(event, func, ...)

EventUtil
EventUtil.ContinueAfterAllEvents(callback, ...)
EventUtil.ContinueOnVariablesLoaded(callback)
EventUtil.ContinueOnAddOnLoaded(addOnName, callback)
EventUtil.RegisterOnceFrameEventAndCallback(frameEvent, callback, ...)
EventUtil.CreateCallbackHandleContainer()

Flags
Flags_CreateMask(...) - Creates a bitmask.
Flags_CreateMaskFromTable(flagsTable)
FlagsUtil.IsSet(bitMask, flagOrMask)

FormattingUtil
SplitTextIntoLines(text, delimiter)
SplitTextIntoHeaderAndNonHeader(text)
FormatValueWithSign(value)
FormatLargeNumber(amount) - Formats a number with dot or comma number seperators.
GetMoneyString(money, separateThousands)
FormatPercentage(percentage, roundToNearestInteger)
FormatFraction(numerator, denominator)
GetHighlightedNumberDifferenceString(baseString, newString)
FormatUnreadMailTooltip(tooltip, headerText, senders)
GetCurrencyString(currencyID, overrideAmount, colorCode, abbreviate)
GetCurrenciesString(currencies)
ReplaceGenderTokens(string, gender)

FrameUtil
FrameUtil.RegisterFrameForEvents(frame, events)
FrameUtil.UnregisterFrameForEvents(frame, events)
FrameUtil.RegisterFrameForUnitEvents(frame, events, ...)
DoesAncestryInclude(ancestry, frame)
GetUnscaledFrameRect(frame, scale)
ApplyDefaultScale(frame, minScale, maxScale)
UpdateScaleForFit(frame)

FunctionUtil
ExecuteFrameScript(frame, scriptName, ...) - Manually calls the handler for a frame script.
CallMethodOnNearestAncestor(self, methodName, ...)
GetValueOrCallFunction(tbl, key, ...)
GenerateClosure(f, ...)
RunNextFrame(callback)

GameTooltipTemplate
GameTooltip_AddBlankLineToTooltip(tooltip)
GameTooltip_AddBlankLinesToTooltip(tooltip, numLines)
GameTooltip_AddBodyLine(...)
GameTooltip_AddColoredLine(tooltip, text, color, wrap, leftOffset)
GameTooltip_AddColoredDoubleLine(tooltip, leftText, rightText, leftColor, rightColor, wrap, leftOffset)
GameTooltip_AddDisabledLine(tooltip, text, wrap, leftOffset)
GameTooltip_AddErrorLine(tooltip, text, wrap, leftOffset)
GameTooltip_AddHighlightLine(tooltip, text, wrap, leftOffset)
GameTooltip_AddInstructionLine(tooltip, text, wrap, leftOffset)
GameTooltip_AddNewbieTip(frame, normalText, r, g, b, newbieText, noNormalText)
GameTooltip_AddNormalLine(tooltip, text, wrap, leftOffset)
GameTooltip_InsertFrame(tooltipFrame, frame, verticalPadding)
GameTooltip_SetTitle(tooltip, text, overrideColor, wrap)
GameTooltip_ShowDisabledTooltip(tooltip, owner, text, tooltipAnchor)
GameTooltip_ShowSimpleTooltip(tooltip, text, overrideColor, wrap, owner, point, offsetX, offsetY)

InterfaceUtil
ReloadUI()
StoreInterfaceUtil.OpenToSubscriptionProduct()

LinkUtil
ExtractHyperlinkString(linkString) - Gets the contents from a hyperlink.
ExtractQuestRewardID(linkString)
GetItemInfoFromHyperlink(link)
GetAchievementInfoFromHyperlink(link)
GetURLIndexAndLoadURL(self, link)

MathUtil
Lerp(startValue, endValue, amount) : number - Linearly interpolates between two values for a parameter amount in the closed unit interval [0, 1]
Clamp(value, min, max) : number
Saturate(value) : number
Wrap(value, max) : number
ClampDegrees(value) : number
ClampMod(value, mod) : number
NegateIf(value, condition) : number
PercentageBetween(value, startValue, endValue) : number
ClampedPercentageBetween(value, startValue, endValue) : number
DeltaLerp(startValue, endValue, amount, timeSec) : number
FrameDeltaLerp(startValue, endValue, amount) : number
RandomFloatInRange(minValue, maxValue) : number
Round(value) : number - Rounds a value.
Square(value) : number - Squares a value.
CalculateDistanceSq(x1, y1, x2, y2) : number
CalculateDistance(x1, y1, x2, y2) : number
CalculateAngleBetween(x1, y1, x2, y2) : number

NineSlice
NineSliceUtil.ApplyUniqueCornersLayout(self, textureKit)
NineSliceUtil.ApplyIdenticalCornersLayout(self, textureKit)
NineSliceUtil.ApplyLayout(container, userLayout, textureKit)
NineSliceUtil.DisableSharpening(container)
NineSliceUtil.ApplyLayoutByName(container, userLayoutName, textureKit)
NineSliceUtil.GetLayout(layoutName)
NineSliceUtil.AddLayout(layoutName, layout)

PixelUtil
PixelUtil.GetPixelToUIUnitFactor()
PixelUtil.GetNearestPixelSize(uiUnitSize, layoutScale, minPixels)
PixelUtil.SetWidth(region, width, minPixels)
PixelUtil.SetHeight(region, height, minPixels)
PixelUtil.SetSize(region, width, height, minWidthPixels, minHeightPixels)
PixelUtil.SetPoint(region, point, relativeTo, relativePoint, offsetX, offsetY, minOffsetXPixels, minOffsetYPixels)
PixelUtil.SetStatusBarValue(statusBar, value)

RegionUtil
RegionUtil.IsDescendantOf(potentialDescendant, potentialAncestor)
RegionUtil.IsDescendantOfOrSame(potentialDescendant, potentialAncestorOrSame)
RegionUtil.CalculateDistanceSqBetween(region1, region2)
RegionUtil.CalculateDistanceBetween(region1, region2)
RegionUtil.CalculateAngleBetween(region1, region2)

RestrictedInfrastructure
tostringall(...)
IsFrameHandle(handle, protected)
GetFrameHandleFrame(handle, protected, onlyProtected)
GetFrameHandle(frame, protected)

ScriptAnimationUtil
ScriptAnimationUtil.GetScriptAnimationLock(region)
ScriptAnimationUtil.ReleaseScriptAnimationLock(region)
ScriptAnimationUtil.IsScriptAnimationLockActive(region)
ScriptAnimationUtil.ShakeFrameRandom(region, magnitude, duration, frequency)
ScriptAnimationUtil.ShakeFrame(region, shake, maximumDuration, frequency)
ScriptAnimationUtil.GenerateEasedVariationCallback(easingFunction, distanceX, distanceY, alpha, scale)
ScriptAnimationUtil.StartScriptAnimation(region, variationCallback, duration, onFinish)

ScriptedAnimationEffects
ScriptedAnimationEffectsUtil.GetEffectByID(effectID)
ScriptedAnimationEffectsUtil.ReloadDB()

TableUtil
ripairs(tbl) : iter, invariant, init - Reverse iterates over a sequential table.
tDeleteItem(tbl, item) - Removes a value from a sequential table.
tIndexOf(tbl, item) : index - Returns the index for a value in a table.
tContains(tbl, item) : boolean - Returns true if a sequential table contains a value.
tCompare(lhsTable, rhsTable [, depth]) : boolean - Does a deep compare on the values of the table.
tInvert(tbl) : table - Returns an inverted table.
tFilter(tbl, pred, isIndexTable) : table
tAppendAll(table, addedArray) - Appends the contents of a sequential table to another table.
tUnorderedRemove(tbl, index)
CopyTable(settings [, shallow]) : table - Returns a copy of a table, defaulting to a deep copy.
AccumulateIf(tbl, pred) : count
ContainsIf(tbl, pred) : boolean
FindInTableIf(tbl, pred) : key, value
SafePack(...) : table
SafeUnpack(tbl) : ...

TextureUtil
GetTextureInfo(obj)
SetClampedTextureRotation(texture, rotationDegrees)
ClearClampedTextureRotation(texture)
GetTexCoordsByGrid(xOffset, yOffset, textureWidth, textureHeight, gridWidth, gridHeight)
GetTexCoordsForRole(role)
CreateTextureMarkup(file, fileWidth, fileHeight, width, height, left, right, top, bottom, xOffset, yOffset)
CreateSimpleTextureMarkup(file, width, height, xOffset, yOffset)
CreateAtlasMarkup(atlasName, width, height, offsetX, offsetY)
SetupAtlasesOnRegions(frame, regionsToAtlases, useAtlasSize)
GetFinalNameFromTextureKit(fmt, textureKits)
SetupTextureKitOnFrame(textureKit, frame, fmt, setVisibility, useAtlasSize)
SetupTextureKitOnFrames(textureKit, frames, setVisibilityOfRegions, useAtlasSize)
SetupTextureKitOnRegions(textureKit, frame, regions, setVisibilityOfRegions, useAtlasSize)
SetupTextureKitsFromRegionInfo(textureKit, frame, regionInfoList)

TimeUtil
SecondsToMinutes(seconds)
MinutesToSeconds(minutes)
HasTimePassed(testTime, amountOfTime)
SecondsToClock(seconds, displayZeroHours)
SecondsToTime(seconds, noSeconds, notAbbreviated, maxCount, roundUp) - Converts a number of seconds into a readable formatted string.
SecondsToTimeAbbrev(seconds) - Converts a number of seconds into a readable and abbreviated formatted string.
FormatShortDate(day, month, year)

UnitUtil
GetPlayerGuid()
IsPlayerGuid(guid)
IsPlayerInitialSpec()

AchievementUtil
AchievementUtil.IsCriteriaAchievementEarned(achievementID, criteriaIndex)
AchievementUtil.IsCriteriaReputationGained(achievementID, criteriaIndex, checkCriteriaAchievement, countHiddenCriteria)
AchievementUtil.IsCategoryFeatOfStrength(category)
AchievementUtil.IsFeatOfStrength(achievementID)

ActionButtonUtil
ActionButtonUtil.ShowAllActionButtonGrids()
ActionButtonUtil.HideAllActionButtonGrids()
ActionButtonUtil.SetAllQuickKeybindButtonHighlights(show)
ActionButtonUtil.ShowAllQuickKeybindButtonHighlights()
ActionButtonUtil.HideAllQuickKeybindButtonHighlights()

AzeriteEssenceUtil
AzeriteEssenceUtil.HasAnyUnlockableMilestones()
AzeriteEssenceUtil.GetMilestoneAtPowerLevel(powerLevel)
AzeriteEssenceUtil.GetMilestoneSpellInfo(milestoneID)

AzeriteUtil
AzeriteUtil.EnumerateEquipedAzeriteEmpoweredItems()
AzeriteUtil.AreAnyAzeriteEmpoweredItemsEquipped()
AzeriteUtil.DoEquippedItemsHaveUnselectedPowers()
AzeriteUtil.GetEquippedItemsUnselectedPowersCount()
AzeriteUtil.GenerateRequiredSpecTooltipLine(powerID)
AzeriteUtil.FindAzeritePowerTier(azeriteEmpoweredItemSource, powerID)
AzeriteUtil.GetSelectedAzeritePowerInTier(azeriteEmpoweredItemSource, tierIndex)
AzeriteUtil.HasSelectedAnyAzeritePower(azeriteEmpoweredItemSource)
AzeriteUtil.DoesBagContainAnyAzeriteEmpoweredItems(bagID)
AzeriteUtil.IsAzeriteItemLocationBankBag(azeriteItemLocation)

CalendarUtil
CalendarUtil.GetCalendarInviteStatusInfo(inviteStatus)
CalendarUtil.GetEventBroadcastText(event)
CalendarUtil.GetOngoingEventBroadcastText(event)
CalendarUtil.FormatCalendarTimeWeekday(messageDate)
CalendarUtil.AreDatesEqual(firstCalendarTime, secondCalendarTime)

CampaignUtil
CampaignUtil.BuildChapterProgressText(campaign, formatString)
CampaignUtil.GetSingleChapterText(chapterID, lineSpacing)
CampaignUtil.BuildAllChaptersText(campaign, lineSpacing)

CommunitiesUtil
CommunitiesUtil.GetMemberRGB(memberInfo)
CommunitiesUtil.SortClubs(clubs)
CommunitiesUtil.SortStreams(streams)
CommunitiesUtil.SortMemberInfo(clubId, memberInfoArray)
CommunitiesUtil.GetMemberIdsSortedByName(clubId, streamId)
CommunitiesUtil.GetMemberInfo(clubId, memberIds)
CommunitiesUtil.GetMemberInfoLookup(memberInfoArray)
CommunitiesUtil.GetOnlineMembers(memberInfoArray)
CommunitiesUtil.SortMembersByList(memberInfoLookup, memberIds)
CommunitiesUtil.GetAndSortMemberInfo(clubId, streamId, filterOffline)
CommunitiesUtil.DoesAnyCommunityHaveUnreadMessages()
CommunitiesUtil.DoesOtherCommunityHaveUnreadMessages(ignoreClubId)
CommunitiesUtil.DoesCommunityHaveUnreadMessages(clubId)
CommunitiesUtil.DoesCommunityHaveOtherUnreadMessages(clubId, ignoreStreamId)
CommunitiesUtil.GetStreamNotificationSettingsLookup(clubId)
CommunitiesUtil.DoesCommunityStreamHaveUnreadMessages(clubId, streamId)
CommunitiesUtil.CanKickClubMember(clubPrivileges, memberInfo)
CommunitiesUtil.ClearAllUnreadNotifications(clubId)
CommunitiesUtil.OpenInviteDialog(clubId, streamId)
CommunitiesUtil.FindCommunityAndStreamByName(communityName, streamName)
CommunitiesUtil.FindGuildStreamByType(clubStreamType)
CommunitiesUtil.GetRoleSpecClassLine(classID, specID)
CommunitiesUtil.AddLookingForLines(tooltip, recruitingSpecIds, recruitingSpecIdMap, playerSpecs)

CovenantUtil
CovenantUtil.GetRenownRewardDisplayData(rewardInfo, onItemUpdateCallback)
CovenantUtil.GetUnformattedRenownRewardInfo(rewardInfo, onItemUpdateCallback)
CovenantUtil.GetRenownRewardInfo(rewardInfo, onItemUpdateCallback)

CurrencyContainer
CurrencyContainerUtil.GetCurrencyContainerInfo(currencyID, numItems, name, texture, quality)
CurrencyContainerUtil.GetCurrencyContainerInfoForAlert(currencyID, quantity, name, texture, quality)

DifficultyUtil
DifficultyUtil.GetDifficultyName(difficultyID)
DifficultyUtil.IsPrimaryRaid(difficultyID)
DifficultyUtil.GetNextPrimaryRaidDifficultyID(difficultyID)
DifficultyUtil.GetMaxPlayers(difficultyID)

ItemRef
SetItemRef(link, text, button, chatFrame) - Handles item link tooltips in chat.
GetFixedLink(text, quality)
GetBattlePetAbilityHyperlink(abilityID, maxHealth, power, speed)
GetPlayerLink(characterName, linkDisplayText, lineID, chatType, chatTarget)
GetBNPlayerLink(name, linkDisplayText, bnetIDAccount, lineID, chatType, chatTarget)
GetGMLink(gmName, linkDisplayText, lineID)
GetBNPlayerCommunityLink(playerName, linkDisplayText, bnetIDAccount, clubId, streamId, epoch, position)
GetPlayerCommunityLink(playerName, linkDisplayText, clubId, streamId, epoch, position)
GetClubTicketLink(ticketId, clubName, clubType)
GetClubFinderLink(clubFinderId, clubName)
GetCalendarEventLink(monthOffset, monthDay, index)
GetCommunityLink(clubId)
LinkUtil.SplitLink(link)
LinkUtil.ExtractLink(text)
LinkUtil.IsLinkType(link, matchLinkType)

ItemUtil
ItemButtonUtil.RegisterCallback(...)
ItemButtonUtil.UnregisterCallback(...)
ItemButtonUtil.TriggerEvent(...)
ItemButtonUtil.GetItemContext()
ItemButtonUtil.HasItemContext()
ItemButtonUtil.GetItemContextMatchResultForItem(itemLocation)
ItemButtonUtil.GetItemContextMatchResultForContainer(bagID)
ItemUtil.GetItemDetails(itemLink, quantity, isCurrency, lootSource)
ItemUtil.PickupBagItem(itemLocation)
ItemUtil.GetOptionalReagentCount(itemID)

MapUtil
MapUtil.IsMapTypeZone(mapID)
MapUtil.GetMapParentInfo(mapID, mapType, topMost)
MapUtil.ShouldMapTypeShowQuests(mapType)
MapUtil.ShouldShowTask(mapID, info)
MapUtil.MapHasUnlockedBounties(mapID)
MapUtil.MapHasEmissaries(mapID)
MapUtil.FindBestAreaNameAtMouse(mapID, normalizedCursorX, normalizedCursorY)
MapUtil.GetDisplayableMapForPlayer()
MapUtil.GetBountySetMaps(bountySetID)
MapUtil.GetMapCenterOnMap(mapID, topMapID)
MapUtil.IsChildMap(mapID, ancestorMapID)
MapUtil.IsOribosMap(mapID)
MapUtil.IsShadowlandsZoneMap(mapID)
MapUtil.MapShouldShowWorldQuestFilters(mapID)

PvPUtil
PVPUtil.GetTierName(tierEnum)
PVPUtil.ShouldShowLegacyRewards()

PartyUtil
PartyUtil.GetMinLevel()
PartyUtil.GetPhasedReasonString(phaseReason, unitToken)
GetGroupMemberCountsForDisplay()

PlayerUtil
PlayerUtil.GetCurrentSpecID()
PlayerUtil.GetSpecName()
PlayerUtil.GetSpecNameBySpecID()
PlayerUtil.GetSpecIconBySpecID()
PlayerUtil.ShouldUseNativeFormInModelScene()
PlayerUtil.GetClassID()
PlayerUtil.GetClassName()
PlayerUtil.GetClassInfo()
PlayerUtil.GetClassFile()
PlayerUtil.GetClassColor()
PlayerUtil.CanUseClassTalents()
PlayerUtil.HasFriendlyReaction()

QuestUtils
QuestUtil.GetWorldQuestAtlasInfo(worldQuestType, inProgress, tradeskillLineID)
QuestUtil.GetQuestIconOffer(isLegendary, frequency, isRepeatable, isCampaign, isCovenantCalling)
QuestUtil.ApplyQuestIconOfferToTexture(texture, ...)
QuestUtil.GetQuestIconActive(isComplete, isLegendary, frequency, isRepeatable, isCampaign, isCovenantCalling)
QuestUtil.ApplyQuestIconActiveToTexture(texture, ...)
QuestUtil.ShouldQuestIconsUseCampaignAppearance(questID)
QuestUtil.GetQuestIconOfferForQuestID(questID)
QuestUtil.ApplyQuestIconOfferToTextureForQuestID(texture, ...)
QuestUtil.GetQuestIconActiveForQuestID(questID)
QuestUtil.ApplyQuestIconActiveToTextureForQuestID(texture, ...)
QuestUtil.SetupWorldQuestButton(button, info, inProgress, selected, isCriteria, isSpellTarget, isEffectivelyTracked)

RuneforgeUtil
RuneforgeUtil.GetCostsString(costs)
RuneforgeUtil.IsUpgradeableRuneforgeLegendary(itemLocation)
RuneforgeUtil.GetRuneforgeFilterText(filter)
RuneforgeUtil.GetPreviewClassAndSpec()

TitleUtil
TitleUtil.GetNameFromTitleMaskID(titleMaskID)

TransmogUtil
TransmogUtil.GetInfoForEquippedSlot(transmogLocation)
TransmogUtil.CanEnchantSource(sourceID)
TransmogUtil.GetWeaponInfoForEnchant(transmogLocation)
TransmogUtil.GetBestWeaponInfoForIllusionDressup()
TransmogUtil.GetSlotID(slotName)
TransmogUtil.GetSlotName(slotID)
TransmogUtil.CreateTransmogLocation(slotDescriptor, transmogType, modification)
TransmogUtil.GetTransmogLocation(slotDescriptor, transmogType, modification)
TransmogUtil.GetTransmogLocationLookupKey(slotID, transmogType, modification)
TransmogUtil.GetSetIcon(setID)

Mixins: https://github.com/Ketho/BlizzardInterfaceResources/blob/live/Resources/Mixins.lua
(3290)

CreateFramePoolCollection

Pools
FramePoolCollectionMixin:CreatePool(frameType, parent, template [, resetterFunc, forbidden]) - Creates a new pool to generate frames with a template.
FramePoolCollectionMixin:GetOrCreatePool(frameType, parent, template [, resetterFunc, forbidden]) - Returns a pool that generates frames with a template, creating one if necessary.
FramePoolCollectionMixin:CreatePoolIfNeeded(frameType, parent, template [, resetterFunc, forbidden]) - Creates a pool to generate frames with a template, if necessary.
FramePoolCollectionMixin:GetPool(template) - Returns the pool that generates frames with a template (or nil if it has not been created).

Frames
FramePoolCollectionMixin:Acquire(template) - Furnishes a frame from the pool in this collection that is responsible for this template.
FramePoolCollectionMixin:Release(frame) - Releases a frame back to the pool which furnished it.
FramePoolCollectionMixin:ReleaseAllByTemplate(template) - Releases all frames furnished by a pool.
FramePoolCollectionMixin:ReleaseAll() - Releases all frames furnished by any pool in the collection.
FramePoolCollectionMixin:EnumerateActiveByTemplate() - Returns an iterator to cycle through frames sourced from one pool.
FramePoolCollectionMixin:EnumerateActive() - Returns an iterator to cycle through widgets sourced from any pool in the collection.

---

---

WidgetAPI: https://warcraft.wiki.gg/wiki/Widget_API
/FSTACK, /TINSPECT

FrameScriptObject
FrameScriptObject:AddAccessRestrictions(restrictions)
FrameScriptObject:AddForbiddenAspects(aspects)
FrameScriptObject:AddSecretAspect(aspect)
FrameScriptObject:CanBeAccessedInContext() : canAccess
FrameScriptObject:GetAccessRestrictions() : restrictions
FrameScriptObject:GetForbiddenAspects() : aspects
FrameScriptObject:GetInheritableForbiddenAspects(path) : aspects
FrameScriptObject:GetName() : name - Returns the object's global name.
FrameScriptObject:GetObjectTable() : objectTable
FrameScriptObject:GetObjectType() : objectType - Returns the object's widget type.
FrameScriptObject:HasAccessConstraints() : hasAccessConstraints
FrameScriptObject:HasAnyAccessRestrictions([restrictions]) : hasAnyAccessRestriction
FrameScriptObject:HasAnyForbiddenAspects([aspects]) : hasAnyForbiddenAspect
FrameScriptObject:HasAnySecretAspect() : hasSecretAspect
FrameScriptObject:HasSecretAspect(aspect) : hasSecretAspect
FrameScriptObject:HasSecretValues() : hasSecretValues
FrameScriptObject:IsForbidden() : isForbidden - Returns whether this object has been explicitly marked as forbidden.
FrameScriptObject:IsObjectType(objectType) : isType - Returns true if the object belongs to a given widget type or its subtypes.
FrameScriptObject:IsPreventingSecretValues() : isPreventingSecretValues
FrameScriptObject:SetForbidden() #protected - Sets the object to be forbidden from an insecure execution path.
FrameScriptObject:SetToDefaults()

Object
Object:ClearParentKey() - Clears the parent key.
Object:GetDebugName([preferParentKey]) : debugName - Returns the object's debug name.
Object:GetParent() : parent - Returns the parent object.
Object:GetParentKey() : parentKey - Returns the key on the parent that references this object.
Object:SetParentKey(parentKey [, clearOtherKeys]) - Sets a key on the parent to the child object.

ScriptRegion
ScriptRegion:CanChangeProtectedState() : canChange - Returns true if protected properties of the region can be changed by non-secure scripts.
ScriptRegion:CanPropagateMouseClicks() : canPropagate
ScriptRegion:CanPropagateMouseMotion() : canPropagate
ScriptRegion:ClearScripts()
ScriptRegion:CollapsesLayout() : collapsesLayout
ScriptRegion:EnableMouse([enable]) #secureframe - Sets whether the region should receive mouse input.
ScriptRegion:EnableMouseMotion([enable]) #secureframe - Sets whether the region should receive mouse hover events.
ScriptRegion:EnableMouseWheel([enable]) #secureframe - Sets whether the region should receive mouse wheel input.
ScriptRegion:GetBottom() : bottom #restrictedframe - Returns the offset to the bottom edge of the region.
ScriptRegion:GetCenter() : x, y #restrictedframe - Returns the offset to the center of the region.
ScriptRegion:GetHeight([ignoreRect]) : height - Returns the height of the region.
ScriptRegion:GetLeft() : left #restrictedframe - Returns the offset to the left edge of the region.
ScriptRegion:GetRect() : left, bottom, width, height #restrictedframe - Returns the coords and size of the region.
ScriptRegion:GetRight() : right #restrictedframe - Returns the offset to the right edge of the region.
ScriptRegion:GetRoundLayoutToNearestPixel() : enabled
ScriptRegion:GetScaledRect() : left, bottom, width, height - Returns the scaled coords and size of the region.
ScriptRegion:GetScript(scriptTypeName [, bindingType]) : script - Returns the widget script handler.
ScriptRegion:GetSize([ignoreRect]) : Functionidth, height - Returns the width and height of the region.
ScriptRegion:GetSourceLocation() : location - Returns the script name and line number where the region was created.
ScriptRegion:GetTop() : top #restrictedframe - Returns the offset to the top edge of the region.
ScriptRegion:GetWidth([ignoreRect]) : Functionidth - Returns the width of the region.
ScriptRegion:HasScript(scriptName) : hasScript - Returns true if the region supports the given script type.
ScriptRegion:Hide() #secureframe - Hides the region.
ScriptRegion:HookScript(scriptTypeName, script [, bindingType]) : success - Securely post-hooks a widget script handler.
ScriptRegion:Intersects(region) : intersects
ScriptRegion:IsAnchoringRestricted() : isRestricted - Returns true if the region has cross-region anchoring restrictions applied.
ScriptRegion:IsAnchoringSecret() : isSecret
ScriptRegion:IsCollapsed() : isCollapsed
ScriptRegion:IsDragging() : isDragging - Returns true if the region is being dragged.
ScriptRegion:IsMouseClickEnabled() : enabled - Returns true if the region can receive mouse clicks.
ScriptRegion:IsMouseEnabled() : enabled - Returns true if the region can receive mouse input.
ScriptRegion:IsMouseMotionEnabled() : enabled - Returns true if the region can receive mouse hover events.
ScriptRegion:IsMouseMotionFocus() : isMouseMotionFocus - Returns true if the mouse cursor is hovering over the region.
ScriptRegion:IsMouseOver([offsetTop [, offsetBottom [, offsetLeft [, offsetRight]]]]) : isMouseOver - Returns true if the mouse cursor is hovering over the region.
ScriptRegion:IsMouseWheelEnabled() : enabled - Returns true if the region can receive mouse wheel input.
ScriptRegion:IsProtected() : isProtected, isProtectedExplicitly - Returns whether the region is currently protected.
ScriptRegion:IsRectValid() : isValid - Returns true if the region can be positioned on the screen.
ScriptRegion:IsShown() : isShown - Returns true if the region should be shown; it depends on the parents if it's visible.
ScriptRegion:IsVisible() : isVisible - Returns true if the region and its parents are shown.
ScriptRegion:SetCollapsesLayout(collapsesLayout) #secureframe
ScriptRegion:SetMouseClickEnabled([enabled]) #secureframe - Sets whether the region should receive mouse clicks.
ScriptRegion:SetMouseMotionEnabled([enabled]) #secureframe - Sets whether the region should receive mouse hover events.
ScriptRegion:SetParent([parent]) #secureframe - Sets the parent of the region.
ScriptRegion:SetPassThroughButtons(...buttons) #nocombat - Allows the region to propagate mouse clicks to underlying regions or the world frame.
ScriptRegion:SetPropagateMouseClicks(propagate) #nocombat
ScriptRegion:SetPropagateMouseMotion(propagate) #nocombat
ScriptRegion:SetRoundLayoutToNearestPixel(enabled)
ScriptRegion:SetScript(scriptTypeName [, script]) - Sets the widget script handler.
ScriptRegion:SetShown([show]) #secureframe - Shows or hides the region.
ScriptRegion:ShouldButtonPassThrough(button) : shouldPassThrough
ScriptRegion:Show() #secureframe - Shows the region.
ScriptRegionResizing
ScriptRegionResizing:AdjustPointsOffset(x, y) #secureframe - Adjusts the x and y offset of the region.
ScriptRegionResizing:ClearAllPoints() #secureframe - Removes all anchor points from the region.
ScriptRegionResizing:ClearPoint(point) #secureframe - Removes an anchor point from the region by name.
ScriptRegionResizing:ClearPointsOffset() #secureframe - Resets the x and y offset on the region to zero.
ScriptRegionResizing:GetNumPoints() : numPoints - Returns the number of anchor points for the region.
ScriptRegionResizing:GetPoint([anchorIndex [, resolveCollapsed]]) : point, relativeTo, relativePoint, offsetX, offsetY #restrictedframe - Returns an anchor point for the region.
ScriptRegionResizing:GetPointByName(point [, resolveCollapsed]) : point, relativeTo, relativePoint, offsetX, offsetY - Returns an anchor point by name for the region.
ScriptRegionResizing:SetAllPoints(relativeTo [, doResize]) #secureframe - Positions the region the same as another region.
ScriptRegionResizing:SetHeight(height) #secureframe - Sets the height of the region.
ScriptRegionResizing:SetPoint(point [, relativeTo [, relativePoint]] [, offsetX, offsetY]) #anchorfamily #secureframe - Sets an anchor point for the region.
ScriptRegionResizing:SetPointsOffset(x, y)
ScriptRegionResizing:SetSize(x, y) #secureframe - Sets the width and height of the region.
ScriptRegionResizing:SetWidth(width) #secureframe - Sets the width of the region.
AnimatableObject
AnimatableObject:CreateAnimationGroup([name [, templateName]]) : group - Creates an animation group.
AnimatableObject:GetAnimationGroups() : ...groups - Returns the animation groups of this region.
AnimatableObject:StopAnimating() - Stops any active animations on this region.

Region
Region:GetAlpha() : alpha - Returns the region's opacity.
Region:GetDrawLayer() : layer, sublayer - Returns the layer in which the region is drawn.
Region:GetEffectiveScale() : effectiveScale - Returns the scale of the region after propagating from its parents.
Region:GetScale() : scale - Returns the scale of the region.
Region:GetVertexColor() : colorR, colorG, colorB, colorA - Returns the vertex color shading of the region.
Region:IsIgnoringParentAlpha() : isIgnoring - Returns true if the region is ignoring parent alpha.
Region:IsIgnoringParentScale() : isIgnoring - Returns true if the region is ignoring parent scale.
Region:IsObjectLoaded() : isLoaded - Returns true if the region is fully loaded.
Region:SetAlpha(alpha) - Sets the opacity of the region.
Region:SetAlphaFromBoolean(value [, alphaIfTrue [, alphaIfFalse]])
Region:SetDrawLayer(layer [, sublevel]) - Sets the layer in which the region is drawn.
Region:SetIgnoreParentAlpha(ignore) - Sets whether the region should ignore its parent's alpha.
Region:SetIgnoreParentScale(ignore) #secureframe - Sets whether the region should ignore its parent's scale.
Region:SetScale(scale) #secureframe - Sets the size scaling of the region.
Region:SetVertexColor(colorR, colorG, colorB [, a]) - Sets the vertex shading color of the region.
Region:SetVertexColorFromBoolean(value, colorIfTrue, colorIfFalse)

TextureBase
TextureBase:ClearRadialProgressBar()
TextureBase:ClearSVG()
TextureBase:ClearTextureSlice()
TextureBase:ClearVertexOffsets()
TextureBase:GetAtlas() : atlas - Returns the atlas for the texture.
TextureBase:GetBlendMode() : blendMode - Returns the blend mode of the texture.
TextureBase:GetDesaturation() : desaturation - Returns the desaturation level of the texture.
TextureBase:GetHorizTile() : tiling - Returns true if the texture is tiling horizontally.
TextureBase:GetRadialProgressBarEndOffset() : offset
TextureBase:GetRadialProgressBarFeather() : feather
TextureBase:GetRadialProgressBarPercent() : percent
TextureBase:GetRadialProgressBarReverse() : reverse
TextureBase:GetRadialProgressBarStartOffset() : offset
TextureBase:GetRotation() : radians, normalizedRotationPoint - Returns the rotation of the texture.
TextureBase:GetTexCoord() : ulX, ulY, llX, llY, urX, urY, lrX, lrY - Returns the texture space coordinates of the texture.
TextureBase:GetTexelSnappingBias() : bias - Returns the texel snapping bias for the texture.
TextureBase:GetTexture() : textureFile - Returns the FileID for the texture.
TextureBase:GetTextureFileID() : textureFile - Returns the FileID for the texture.
TextureBase:GetTextureFilePath() : textureFile - Returns the FileID for the texture.
TextureBase:GetTextureSliceMargins() : left, top, right, bottom
TextureBase:GetTextureSliceMode() : sliceMode
TextureBase:GetVertTile() : tiling - Returns true if the texture is tiling vertically.
TextureBase:GetVertexOffset(vertexIndex) : offsetX, offsetY - Returns a vertex offset for the texture.
TextureBase:IsBlockingLoadRequested() : blocking
TextureBase:IsDesaturated() : desaturated - Returns true if the texture is desaturated.
TextureBase:IsSnappingToPixelGrid() : snap - Returns true if the texture is snapping to the pixel grid.
TextureBase:ResetTexCoord()
TextureBase:SetAtlas(atlas [, useAtlasSize [, filterMode [, resetTexCoords [, wrapModeHorizontal [, wrapModeVertical]]]]]) - Sets the texture to an atlas.
TextureBase:SetBlendMode(blendMode) - Sets the blend mode of the texture.
TextureBase:SetBlockingLoadsRequested([blocking])
TextureBase:SetColorTexture(colorR, colorG, colorB [, a]) - Sets the texture to a solid color.
TextureBase:SetDesaturated([desaturated]) - Sets the texture to be desaturated.
TextureBase:SetDesaturation(desaturation) - Sets the desaturation level of the texture.
TextureBase:SetGradient(orientation, minColor, maxColor) - Sets a gradient color shading for the texture.
TextureBase:SetHorizTile([tiling]) - Sets whether the texture should tile horizontally.
TextureBase:SetMask(file) - Applies a mask to the texture.
TextureBase:SetRadialProgressBarEndOffset(offset)
TextureBase:SetRadialProgressBarFeather(feather)
TextureBase:SetRadialProgressBarPercent(percent)
TextureBase:SetRadialProgressBarReverse(reverse)
TextureBase:SetRadialProgressBarStartOffset(offset)
TextureBase:SetRotation(radians [, normalizedRotationPoint]) - Applies a rotation to the texture.
TextureBase:SetSVG(svgAsset) : success
TextureBase:SetSnapToPixelGrid([snap]) - Sets the texture to snap to the pixel grid.
TextureBase:SetSpriteSheetCell(cell, numRows, numColumns [, cellWidth, cellHeight])
TextureBase:SetTexCoord(left, right, top, bottom) - Sets the coordinates for cropping or transforming the texture.
TextureBase:SetTexelSnappingBias(bias) - Returns the texel snapping bias for the texture.
TextureBase:SetTexture([textureAsset [, wrapModeHorizontal [, wrapModeVertical [, filterMode]]]]) : success - Sets the texture to an image.
TextureBase:SetTextureSliceMargins(left, top, right, bottom)
TextureBase:SetTextureSliceMode(sliceMode)
TextureBase:SetVertTile([tiling]) - Sets whether the texture should tile vertically.
TextureBase:SetVertexOffset(vertexIndex, offsetX, offsetY) - Sets a vertex offset for the texture.

Texture
Texture:AddMaskTexture(mask)
Texture:GetMaskTexture(index) : mask
Texture:GetNumMaskTextures() : count
Texture:RemoveMaskTexture(mask)

MaskTexture

Line
Line:ClearAllPoints()
Line:GetEndPoint() : relativePoint, relativeTo, offsetX, offsetY
Line:GetHitRectThickness() : thickness
Line:GetStartPoint() : relativePoint, relativeTo, offsetX, offsetY
Line:GetThickness() : thickness
Line:SetEndPoint(relativePoint, relativeTo [, offsetX, offsetY])
Line:SetHitRectThickness(thickness)
Line:SetStartPoint(relativePoint, relativeTo [, offsetX, offsetY])
Line:SetThickness(thickness)

VectorGraphics
VectorGraphics:ClearSVG()
VectorGraphics:GetSVGFileID() : svgFile
VectorGraphics:HasSVG() : hasSVG
VectorGraphics:SetSVG(svgAsset) : success

FontInstance
FontInstance:GetFont() : fontFile, height, flags - Returns the font path, height, and flags.
FontInstance:GetFontObject() : font - Returns the "parent" font object.
FontInstance:GetIndentedWordWrap() : wordWrap - Returns the indentation when text wraps beyond the first line.
FontInstance:GetJustifyH() : justifyH - Returns the horizontal text justification.
FontInstance:GetJustifyV() : justifyV - Returns the vertical text justification.
FontInstance:GetShadowColor() : colorR, colorG, colorB, colorA - Returns the text shadow color.
FontInstance:GetShadowOffset() : offsetX, offsetY - Returns the text shadow offset.
FontInstance:GetSpacing() : spacing - Returns the line spacing.
FontInstance:GetTextColor() : colorR, colorG, colorB, colorA - Returns the default text color.
FontInstance:SetFont(fontFile, height, flags) - Sets the basic font properties.
FontInstance:SetFontObject(font) - Sets the "parent" font object from which this object inherits properties.
FontInstance:SetIndentedWordWrap(wordWrap) - Sets the indentation when text wraps beyond the first line.
FontInstance:SetJustifyH(justifyH) - Sets the horizontal text justification
FontInstance:SetJustifyV(justifyV) - Sets the vertical text justification.
FontInstance:SetShadowColor(colorR, colorG, colorB [, a]) - Sets the text shadow color.
FontInstance:SetShadowOffset(offsetX, offsetY) - Sets the text shadow offset.
FontInstance:SetSpacing(spacing) - Sets the spacing between lines of text in the object.
FontInstance:SetTextColor(colorR, colorG, colorB [, a]) - Sets the default text color.

Font
Font:CopyFontObject(sourceFont)
Font:GetAlpha() : alpha
Font:GetFontHeight() : height
Font:GetFontObjectForAlphabet(alphabet) : font
Font:SetAlpha(alpha)
Font:SetFontHeight(height)

FontString
FontString:CalculateScreenAreaFromCharacterSpan(leftIndex, rightIndex) : areas
FontString:CanNonSpaceWrap() : Functionrap
FontString:CanWordWrap() : Functionrap
FontString:ClearAlphaGradient()
FontString:ClearText()
FontString:FindCharacterIndexAtCoordinate(x, y) : characterIndex, inside
FontString:GetAlphaGradient() : start, length
FontString:GetFieldSize() : fieldSize
FontString:GetFontHeight([calculated]) : height
FontString:GetLineHeight() : lineHeight
FontString:GetMaxLines() : maxLines
FontString:GetNumLines() : numLines
FontString:GetRotation() : radians
FontString:GetScaleAnimationMode() : scaleAnimationMode
FontString:GetSmoothScaling() : smoothScaling
FontString:GetStringHeight() : height
FontString:GetStringWidth() : Functionidth
FontString:GetText() : text
FontString:GetTextScale() : textScale
FontString:GetUnboundedStringWidth() : Functionidth
FontString:GetUnboundedStringWidthForText(text) : Functionidth
FontString:GetWrappedWidth() : Functionidth
FontString:IsTruncated() : isTruncated
FontString:OnColorsUpdated()
FontString:SetAlphaGradient(start, length) : isWithinText
FontString:SetDesaturateEmbeddedTextures(desaturate)
FontString:SetFixedColor(fixedColor)
FontString:SetFontHeight(height)
FontString:SetFormattedText(text)
FontString:SetMaxLines(maxLines)
FontString:SetNonSpaceWrap(wrap)
FontString:SetRotation(radians)
FontString:SetScaleAnimationMode(scaleAnimationMode)
FontString:SetSmoothScaling(smoothScaling)
FontString:SetText([text])
FontString:SetTextHeight(height)
FontString:SetTextScale(textScale)
FontString:SetTextToFit([text])
FontString:SetWordWrap(wrap)

AnimationGroup
AnimationGroup:CreateAnimation([animationType, name, templateName]) : anim - Returns an animation as a child of this group.
AnimationGroup:Finish() - Notifies the animationgroup to stop playing once the current loop cycle is done.
AnimationGroup:GetAnimations() : ...anims
AnimationGroup:GetAnimationSpeedMultiplier() : animationSpeedMultiplier
AnimationGroup:GetDuration() : durationSec - Returns the total duration across all child animations that the group will take to complete one loop cycle.
AnimationGroup:GetElapsed() : elapsedSec
AnimationGroup:GetLooping() : loopType) - Returns the type of looping for the group.
AnimationGroup:GetLoopState() : loopState - Returns the current loop state of the group.
AnimationGroup:GetProgress() : progress - Returns the progress of this animation.
AnimationGroup:GetScript(scriptTypeName [, bindingType]) : script
AnimationGroup:HasScript(scriptName) : hasScript
AnimationGroup:HookScript(scriptTypeName, script [, bindingType]) : success
AnimationGroup:IsDone() : isDone - Returns true if the group has finished playing.
AnimationGroup:IsPaused() : isPaused - Returns true if the group is paused.
AnimationGroup:IsPendingFinish() : isPendingFinish
AnimationGroup:IsPlaying() : isPlaying - Returns true if the group is playing.
AnimationGroup:IsReverse() : isReverse
AnimationGroup:IsSetToFinalAlpha() : isSetToFinalAlpha
AnimationGroup:Pause() - Pauses the animations in this group.
AnimationGroup:Play([reverse, offset]) - Starts playing the animations in this group.
AnimationGroup:RemoveAnimations()
AnimationGroup:Restart([reverse, offset])
AnimationGroup:SetAnimationSpeedMultiplier(animationSpeedMultiplier)
AnimationGroup:SetLooping(loopType) - Sets the type of looping for the group.
AnimationGroup:SetPlaying(play)
AnimationGroup:SetScript(scriptTypeName [, script])
AnimationGroup:SetToFinalAlpha(setToFinalAlpha)
AnimationGroup:Stop() - Stops all animations in this group.

Animation
Animation:GetDuration() : durationSec - Returns the number of seconds it takes for the animation to progress from start to finish.
Animation:GetElapsed() : elapsedSec - Returns the amount of time in seconds that the animation has been playing for.
Animation:GetEndDelay() : delaySec - Returns the number of seconds the animation delays after finishing.
Animation:GetOrder() : order - Returns the order of the animation within its parent group.
Animation:GetProgress() : progress - Returns the progress of the animation.
Animation:GetRegionParent() : region - Returns the Region object that the animation operates on.
Animation:GetScript(scriptTypeName [, bindingType]) : script
Animation:GetSmoothing() : Functioneights - Returns the smoothing type for the animation.
Animation:GetSmoothProgress() : progress - Returns a smoothed progress value for the animation.
Animation:GetStartDelay() : delaySec - Sets the number of seconds that the animation delays before it starts to progress.
Animation:GetTarget() : target
Animation:HasScript(scriptName) : hasScript
Animation:HookScript(scriptTypeName, script [, bindingType]) : success
Animation:IsDelaying() : isDelaying - Returns true if the animation is in the middle of a start or end delay.
Animation:IsDone() : isDone - Returns true if the animation has finished playing.
Animation:IsPaused() : isPaused - Returns true if the animation is paused.
Animation:IsPlaying() : isPlaying
Animation:IsStopped() : isStopped - Returns true if the animation is stopped.
Animation:Pause() - Pauses the animation.
Animation:Play() - Plays the animation.
Animation:Restart()
Animation:SetChildKey(childKey) : success
Animation:SetDuration(durationSec [, recomputeGroupDuration]) - Sets the number of seconds it takes for the animation to progress from start to finish.
Animation:SetEndDelay(delaySec [, recomputeGroupDuration]) - Sets the number of seconds the animation delays after finishing.
Animation:SetOrder(newOrder) - Sets the order that the animation plays within its parent group.
Animation:SetParent(parent [, order]) - Sets the parent for the animation.
Animation:SetPlaying(play)
Animation:SetScript(scriptTypeName [, script])
Animation:SetSmoothing(weights)
Animation:SetSmoothProgress(durationSec) - Sets the smoothing type for the animation.
Animation:SetStartDelay(delaySec [, recomputeGroupDuration]) - Returns the number of seconds that the animation delays before it starts to progress.
Animation:SetTarget(target) : success
Animation:SetTargetKey(key) : success
Animation:SetTargetName(name) : success
Animation:SetTargetParent() : success
Animation:Stop() - Stops the animation.

Alpha
Alpha:GetFromAlpha() : normalizedAlpha
Alpha:GetToAlpha() : normalizedAlpha
Alpha:SetFromAlpha(normalizedAlpha)
Alpha:SetToAlpha(normalizedAlpha)

FlipBook
FlipBook:GetFlipBookColumns() : columns
FlipBook:GetFlipBookFrameHeight() : height
FlipBook:GetFlipBookFrameWidth() : width
FlipBook:GetFlipBookFrames() : frames
FlipBook:GetFlipBookRows() : rows
FlipBook:SetFlipBookColumns(columns)
FlipBook:SetFlipBookFrameHeight(height)
FlipBook:SetFlipBookFrameWidth(width)
FlipBook:SetFlipBookFrames(frames)
FlipBook:SetFlipBookRows(rows)

Path
Path:CreateControlPoint([name [, templateName [, order]]]) : point
Path:GetControlPoints() : ...points
Path:GetCurveType() : curveType
Path:GetMaxControlPointOrder() : maxOrder
Path:SetCurveType(curveType)

ControlPoint
ControlPoint:GetOffset() : offsetX, offsetY
ControlPoint:GetOrder() : order
ControlPoint:SetOffset(offsetX, offsetY)
ControlPoint:SetOrder(order)
ControlPoint:SetParent(parent [, order])

RadialProgress
RadialProgress:GetFromPercent() : percent
RadialProgress:GetToPercent() : percent
RadialProgress:SetFromPercent(percent)
RadialProgress:SetToPercent(percent)

Rotation
Rotation:GetDegrees() : angle
Rotation:GetOrigin() : point, originX, originY
Rotation:GetRadians() : angle
Rotation:SetDegrees(angle)
Rotation:SetOrigin(point, originX, originY)
Rotation:SetRadians(angle)

Scale
Scale:GetOrigin() : point, originX, originY
Scale:GetScale() : scaleX, scaleY
Scale:GetScaleFrom() : scaleX, scaleY
Scale:GetScaleTo() : scaleX, scaleY
Scale:SetOrigin(point, originX, originY)
Scale:SetScale(scaleX, scaleY)
Scale:SetScaleFrom(scaleX, scaleY)
Scale:SetScaleTo(scaleX, scaleY)

TextureCoordTranslation
TextureCoordTranslation:GetOffset() : offsetU, offsetV
TextureCoordTranslation:SetOffset(offsetU, offsetV)

Translation
Translation:GetOffset() : offsetX, offsetY
Translation:SetOffset(offsetX, offsetY)

VertexColor
VertexColor:GetEndColor() : color
VertexColor:GetStartColor() : color
VertexColor:SetEndColor(color)
VertexColor:SetStartColor(color)

Frame
Frame:AbortDrag()
Frame:AddRoleset(roleset)
Frame:CanChangeAttribute() : canChangeAttributes
Frame:ClearAlphaGradient()
Frame:ClearAttribute(attributeName) : cleared
Frame:ClearAttributes()
Frame:CreateFontString([name, drawLayer, templateName]) : line - Creates a fontstring.
Frame:CreateLine([name, drawLayer, templateName, subLevel]) : line - Draws a line.
Frame:CreateMaskTexture([name, drawLayer, templateName, subLevel]) : maskTexture - Creates a mask texture.
Frame:CreateTexture([name, drawLayer, templateName, subLevel]) : texture - Creates a texture.
Frame:CreateVectorGraphics([name [, drawLayer [, templateName [, subLevel]]]]) : vectorGraphics
Frame:DesaturateHierarchy(desaturation [, excludeRoot])
Frame:DisableDrawLayer(layer) - Prevents display of the frame on the specified draw layer.
Frame:DoesClipChildren() : clipsChildren
Frame:DoesHyperlinkPropagateToParent() : canPropagate
Frame:EnableDrawLayer(layer) - Allows display of the frame on the specified draw layer.
Frame:EnableGamePadButton([enable]) #secureframe - Allows the receipt of gamepad button inputs for this frame.
Frame:EnableGamePadStick([enable]) #secureframe - Allows the receipt of gamepad stick inputs for this frame.
Frame:EnableKeyboard([enable]) #secureframe - Allows this frame to receive keyboard input.
Frame:ExecuteAttribute(attributeName [, ...arguments]) : success, ...returns
Frame:GetAlpha() : alpha
Frame:GetAttribute(attributeName) : value - Returns the value of a secure frame attribute.
Frame:GetBoundsRect() : left, bottom, width, height - Returns the calculated bounding box of the frame and all of its descendant regions.
Frame:GetChildren() : ...children - Returns a list of child frames belonging to the frame.
Frame:GetClampRectInsets() : left, right, top, bottom - Returns the frame's clamp rectangle offsets.
Frame:GetDontSavePosition() : dontSave
Frame:GetEffectiveAlpha() : effectiveAlpha - Returns the effective alpha after propagating from the parent region.
Frame:GetEffectivelyFlattensRenderLayers() : flatten - Returns true if render layer flattening has been implicitly enabled.
Frame:GetEffectiveScale() : effectiveScale - Returns the effective scale after propagating from the parent region.
Frame:GetFlattensRenderLayers() : flatten - Returns true if render layer flattening has been enabled.
Frame:GetFrameLevel() : frameLevel - Returns the frame level of the frame.
Frame:GetFrameStrata() : strata - Returns the layering strata of the frame.
Frame:GetHighestFrameLevel([iterateAllChildren]) : frameLevel
Frame:GetHitRectInsets() : left, right, top, bottom - Returns the insets of the frame's hit rectangle.
Frame:GetHyperlinksEnabled() : enabled - Returns true if mouse interaction with hyperlinks on the frame is enabled.
Frame:GetID() : id - Returns the frame's numeric identifier.
Frame:GetNumChildren() : numChildren - Returns the number of child frames belonging to the frame.
Frame:GetNumRegions() : numRegions - Returns the number of non-Frame child regions belonging to the frame.
Frame:GetOnUpdateMode() : onUpdateMode
Frame:GetPropagateKeyboardInput() : propagate - Returns whether the frame propagates keyboard events.
Frame:GetRaisedFrameLevel() : frameLevel
Frame:GetRegions() : ...regions - Returns a list of non-Frame child regions belonging to the frame.
Frame:GetResizeBounds() : minWidth, minHeight, maxWidth, maxHeight - Returns the minimum and maximum size of the frame for user resizing.
Frame:GetRolesetNames() : rolesets
Frame:GetScale() : frameScale
Frame:GetWindow() : Functionindow
Frame:HasAlphaGradient() : hasAlphaGradient
Frame:HasFixedFrameLevel() : isFixed
Frame:HasFixedFrameStrata() : isFixed
Frame:Hide() #secureframe
Frame:InterceptStartDrag(delegate)
Frame:IsClampedToScreen() : clampedToScreen - Returns whether a frame is prevented from being moved off-screen.
Frame:IsDrawLayerEnabled(layer) : isEnabled
Frame:IsEventRegistered(eventName) : isRegistered, ...units - Returns whether a frame is registered to an event.
Frame:IsFrameBuffer() : isFrameBuffer
Frame:IsGamePadButtonEnabled() : enabled - Checks if this frame is configured to receive gamepad button inputs.
Frame:IsGamePadStickEnabled() : enabled - Checks if this frame is configured to receive gamepad stick inputs.
Frame:IsHighlightLocked() : locked
Frame:IsIgnoringChildrenForBounds() : ignore
Frame:IsIgnoringParentAlpha() : ignore
Frame:IsIgnoringParentScale() : ignore
Frame:IsKeyboardEnabled() : enabled - Returns true if keyboard interactivity is enabled for the frame.
Frame:IsMovable() : isMovable - Returns true if the frame is movable.
Frame:IsObjectLoaded() : isLoaded
Frame:IsResizable() : resizable - Returns true if the frame can be resized by the user.
Frame:IsRolesetFiltered() : isRolesetFiltered
Frame:IsShown() : isShown
Frame:IsToplevel() : isTopLevel - Returns whether this frame should raise its frame level on mouse interaction.
Frame:IsUserPlaced() : isUserPlaced - Returns whether the frame has been moved by the user.
Frame:IsUsingParentLevel() : usingParentLevel
Frame:IsVisible() : isVisible
Frame:LockHighlight() - Sets the frame or button to always be drawn highlighted.
Frame:Lower() #secureframe - Reduces the frame's frame level below all other frames in its strata.
Frame:Raise() #secureframe - Increases the frame's frame level above all other frames in its strata.
Frame:RegisterAllEvents() - Flags the frame to receive all events.
Frame:RegisterEvent(eventName) : registered - Registers the frame to an event.
Frame:RegisterEventCallback(eventName, cb) : registered
Frame:RegisterForDrag(...buttons) - Registers the frame for dragging with a mouse button.
Frame:RegisterUnitEvent(eventName, ...units) : registered - Registers the frame for a specific event, triggering only for the specified units.
Frame:RegisterUnitEventCallback(eventName, cb, ...units) : registered
Frame:RemoveRoleset(roleset)
Frame:ResizeToBoundsRect()
Frame:RotateTextures(radians [, x, y])
Frame:SetAlpha(alpha)
Frame:SetAlphaGradient(index, gradient)
Frame:SetAttribute(attributeName, value) #secureframe - Sets an attribute on the frame.
Frame:SetAttributeNoHandler(attributeName, value) #secureframe - Sets an attribute on the frame without triggering the OnAttributeChanged script handler.
Frame:SetClampedToScreen(clampedToScreen) #secureframe - Prevents the frame from moving off-screen.
Frame:SetClampRectInsets(left, right, top, bottom) #secureframe - Controls how much of the frame may be moved off-screen.
Frame:SetClipsChildren(clipsChildren)
Frame:SetDontSavePosition(dontSave)
Frame:SetDrawLayerEnabled(layer [, isEnabled])
Frame:SetFixedFrameLevel(isFixed) #secureframe
Frame:SetFixedFrameStrata(isFixed) #secureframe
Frame:SetFlattensRenderLayers(flatten) - Controls whether all subregions are composited into a single render layer.
Frame:SetFrameLevel(frameLevel) #secureframe - Sets the level at which the frame is layered relative to others in its strata.
Frame:SetFrameStrata(strata) #secureframe - Sets the layering strata of the frame.
Frame:SetHighlightLocked(locked)
Frame:SetHitRectInsets(left, right, top, bottom) #secureframe - Returns the insets of the frame's hit rectangle.
Frame:SetHyperlinkPropagateToParent(canPropagate)
Frame:SetHyperlinksEnabled([enabled]) #secureframe - Allows mouse interaction with hyperlinks on the frame.
Frame:SetID(id) #secureframe - Returns the frame's numeric identifier.
Frame:SetIgnoreParentAlpha(ignore)
Frame:SetIgnoreParentScale(ignore) #secureframe
Frame:SetIgnoringChildrenForBounds(ignore)
Frame:SetIsFrameBuffer(isFrameBuffer) - Controls whether or not a frame is rendered to its own framebuffer prior to being composited atop the UI.
Frame:SetMovable(movable) - Sets whether the frame can be moved.
Frame:SetOnUpdateMode(onUpdateMode)
Frame:SetPropagateKeyboardInput(propagate) #nocombat - Sets whether keyboard input is consumed by this frame or propagates to further frames.
Frame:SetResizable(resizable) - Sets whether the frame can be resized by the user.
Frame:SetResizeBounds(minWidth, minHeight [, maxWidth, maxHeight]) - Sets the minimum and maximum size of the frame for user resizing.
Frame:SetRolesets([rolesetsString])
Frame:SetScale(scale) #secureframe
Frame:SetShown([shown]) #secureframe
Frame:SetToplevel(topLevel) #secureframe - Controls whether or not a frame should raise its frame level on mouse interaction.
Frame:SetUserPlaced(userPlaced) - Sets whether a frame has been moved by the user and will be saved in the layout cache.
Frame:SetUsingParentLevel(usingParentLevel) #secureframe
Frame:SetWindow([window])
Frame:Show() #secureframe
Frame:StartMoving([alwaysStartFromMouse]) #secureframe - Begins repositioning the frame via mouse movement.
Frame:StartSizing([resizePoint, alwaysStartFromMouse]) #secureframe - Begins resizing the frame via mouse movement.
Frame:StopMovingOrSizing() #secureframe - Stops moving or resizing the frame.
Frame:UnlockHighlight() - Sets the frame or button to not always be drawn highlighted.
Frame:UnregisterAllEvents() - Unregisters all events from the frame.
Frame:UnregisterEvent(eventName) : registered - Unregisters an event from the frame.

Button
Button:ClearDisabledTexture()
Button:ClearHighlightTexture()
Button:ClearNormalTexture()
Button:ClearPushedTexture()
Button:Click([button, isDown]) - Performs a virtual mouse click on the button.
Button:Disable() #secureframe
Button:Enable() #secureframe
Button:GetButtonState() : buttonState
Button:GetDisabledFontObject() : font
Button:GetDisabledTexture() : texture
Button:GetFontString() : fontString
Button:GetHighlightFontObject() : font
Button:GetHighlightTexture() : texture - Returns the highlight texture for the button.
Button:GetMotionScriptsWhileDisabled() : motionScriptsWhileDisabled
Button:GetNormalFontObject() : font - Returns the font object for the button's normal state.
Button:GetNormalTexture() : texture
Button:GetPushedTextOffset() : offsetX, offsetY
Button:GetPushedTexture() : texture
Button:GetText() : text - Returns the text on the button.
Button:GetTextHeight() : height
Button:GetTextWidth() : Functionidth
Button:IsEnabled() : isEnabled - Returns true if the button is enabled.
Button:RegisterForClicks(...buttons) #secureframe - Registers the button widget to receive OnClick script events.
Button:RegisterForMouse(...buttons) #secureframe - Registers the button widget to receive OnMouse script events.
Button:SetButtonState(buttonState [, lock])
Button:SetDisabledAtlas(atlas)
Button:SetDisabledFontObject(font)
Button:SetDisabledTexture(asset)
Button:SetEnabled([enabled]) #secureframe
Button:SetFontString(fontString)
Button:SetFormattedText(text)
Button:SetHighlightAtlas(atlas [, blendMode])
Button:SetHighlightFontObject(font)
Button:SetHighlightTexture(asset [, blendMode])
Button:SetMotionScriptsWhileDisabled(motionScriptsWhileDisabled)
Button:SetNormalAtlas(atlas)
Button:SetNormalFontObject(font) - Sets the font object used for the button's normal state.
Button:SetNormalTexture(asset) - Sets the normal texture for a button.
Button:SetPushedAtlas(atlas)
Button:SetPushedTextOffset(offsetX, offsetY)
Button:SetPushedTexture(asset)
Button:SetText([text]) - Sets the text of the button.

CheckButton
CheckButton:GetChecked() : checked - Returns true if the checkbutton is checked.
CheckButton:GetCheckedTexture() : texture
CheckButton:GetDisabledCheckedTexture() : texture
CheckButton:SetChecked([checked]) - Sets whether the checkbutton is checked.
CheckButton:SetCheckedTexture(asset)
CheckButton:SetDisabledCheckedTexture(asset)

Model
Model:AdvanceTime()
Model:ClearFog()
Model:ClearModel()
Model:ClearTransform()
Model:GetCameraDistance() : distance
Model:GetCameraFacing() : radians
Model:GetCameraPosition() : positionX, positionY, positionZ
Model:GetCameraRoll() : radians
Model:GetCameraTarget() : targetX, targetY, targetZ
Model:GetDesaturation() : strength
Model:GetFacing() : facing - Returns the offset of the rotation angle.
Model:GetFogColor() : colorR, colorG, colorB, colorA
Model:GetFogFar() : fogFar
Model:GetFogNear() : fogNear
Model:GetLight() : enabled, light
Model:GetModelAlpha() : alpha
Model:GetModelDrawLayer() : layer, sublayer
Model:GetModelFileID() : modelFileID - Returns the file ID associated with the currently displayed model.
Model:GetModelScale() : scale
Model:GetPaused() : paused
Model:GetPitch() : pitch
Model:GetPosition() : positionX, positionY, positionZ
Model:GetRoll() : roll
Model:GetShadowEffect() : strength
Model:GetViewInsets() : left, right, top, bottom
Model:GetViewTranslation() : x, y
Model:GetWorldScale() : worldScale
Model:HasAttachmentPoints() : hasAttachmentPoints
Model:HasCustomCamera() : hasCustomCamera
Model:IsUsingModelCenterToTransform() : useCenter
Model:MakeCurrentCameraCustom()
Model:ReplaceIconTexture(asset)
Model:SetCamera(cameraIndex) - Selects a predefined camera.
Model:SetCameraDistance(distance)
Model:SetCameraFacing(radians)
Model:SetCameraPosition(positionX, positionY, positionZ)
Model:SetCameraRoll(radians)
Model:SetCameraTarget(targetX, targetY, targetZ)
Model:SetCustomCamera(cameraIndex)
Model:SetDesaturation(strength)
Model:SetFacing(facing) - Rotates the displayed model for the given angle in counter-clockwise direction.
Model:SetFogColor(colorR, colorG, colorB [, a]) - Sets the color used for the fogging in the model frame.
Model:SetFogFar(fogFar) - Sets the far clipping plane for fogging.
Model:SetFogNear(fogNear) - Sets the near clipping plane for fogging.
Model:SetGlow(glow)
Model:SetGradientMask(grad0, grad1, grad2, grad3)
Model:SetLight(enabled, light) - Specifies model lighting.
Model:SetModel(asset [, noMip]) - Sets the model to display a certain mesh.
Model:SetModelAlpha(alpha)
Model:SetModelDrawLayer(layer)
Model:SetModelScale(scale)
Model:SetParticlesEnabled(enabled)
Model:SetPaused(paused)
Model:SetPitch(pitch)
Model:SetPosition(positionX, positionY, positionZ) - Positions a model relative to the bottom-left corner.
Model:SetRoll(roll)
Model:SetSequence(sequence) - Sets the animation-sequence to be played.
Model:SetSequenceTime(sequence, timeOffset)
Model:SetShadowEffect(strength)
Model:SetTransform([translation, rotation, scale])
Model:SetUseGBuffer(useGBuffer)
Model:SetViewInsets(left, right, top, bottom)
Model:SetViewTranslation(x, y)
Model:TransformCameraSpaceToModelSpace(cameraPosition) : modelPosition
Model:UseModelCenterToTransform(useCenter)

PlayerModel
PlayerModel:ApplySpellVisualKit(spellVisualKitID [, oneShot])
PlayerModel:CanSetUnit(unit)
PlayerModel:FreezeAnimation(anim, variation, frame) - Freezes an animation at a specific animation frame on the model.
PlayerModel:GetDisplayInfo() : displayID
PlayerModel:GetDoBlend() : doBlend
PlayerModel:GetKeepModelOnHide() : keepModelOnHide
PlayerModel:HasAnimation(anim) : hasAnimation - Returns true if the currently displayed model supports the given animation ID.
PlayerModel:PlayAnimKit(animKit [, loop])
PlayerModel:RefreshCamera()
PlayerModel:RefreshUnit()
PlayerModel:SetAnimation(anim [, variation]) - Sets the animation to be played by the model.
PlayerModel:SetBarberShopAlternateForm()
PlayerModel:SetCamDistanceScale(scale)
PlayerModel:SetCreature(creatureID [, displayID])
PlayerModel:SetDisplayInfo(displayID [, mountDisplayID])
PlayerModel:SetDoBlend([doBlend])
PlayerModel:SetItem(itemID [, appearanceModID, itemVisualID])
PlayerModel:SetItemAppearance(itemAppearanceID [, itemVisualID, itemSubclass])
PlayerModel:SetKeepModelOnHide(keepModelOnHide)
PlayerModel:SetPortraitZoom(zoom)
PlayerModel:SetRotation(radians [, animate])
PlayerModel:SetUnit(unit [, blend, useNativeForm]) : success - Sets the model to display the specified unit.
PlayerModel:StopAnimKit()
PlayerModel:ZeroCachedCenterXY()

CinematicModel
CinematicModel:EquipItem(itemID)
CinematicModel:InitializeCamera([scaleFactor])
CinematicModel:InitializePanCamera([scaleFactor])
CinematicModel:RefreshCamera()
CinematicModel:SetAnimOffset(offset)
CinematicModel:SetCameraPosition(positionX, positionY, positionZ)
CinematicModel:SetCameraTarget(positionX, positionY, positionZ)
CinematicModel:SetCreatureData(creatureID)
CinematicModel:SetFacingLeft([isFacingLeft])
CinematicModel:SetFadeTimes(fadeInSeconds, fadeOutSeconds)
CinematicModel:SetHeightFactor(factor)
CinematicModel:SetJumpInfo(jumpLength, jumpHeight)
CinematicModel:SetPanDistance(scale)
CinematicModel:SetSpellVisualKit(visualKitID)
CinematicModel:SetTargetDistance(scale)
CinematicModel:StartPan(panType, durationSeconds [, doFade, visKitID, startPositionScale, speedMultiplier])
CinematicModel:StopPan()
CinematicModel:UnequipItems()

DressUpModel
DressUpModel:Dress()
DressUpModel:GetAutoDress() : enabled
DressUpModel:GetItemTransmogInfo(inventorySlot) : itemTransmogInfo
DressUpModel:GetItemTransmogInfoList() : infoList
DressUpModel:GetObeyHideInTransmogFlag() : enabled
DressUpModel:GetSheathed() : sheathed
DressUpModel:GetUseTransmogChoices() : enabled
DressUpModel:GetUseTransmogSkin() : enabled
DressUpModel:IsGeoReady() : ready
DressUpModel:IsSlotAllowed(slot) : allowed
DressUpModel:IsSlotVisible(slot) : visible
DressUpModel:SetAutoDress([enabled])
DressUpModel:SetItemTransmogInfo(itemTransmogInfo [, inventorySlot, ignoreChildItems]) : result
DressUpModel:SetObeyHideInTransmogFlag([enabled])
DressUpModel:SetSheathed([sheathed, hideWeapons])
DressUpModel:SetUseTransmogChoices([enabled])
DressUpModel:SetUseTransmogSkin([enabled])
DressUpModel:TryOn(linkOrItemModifiedAppearanceID [, handSlotName, spellEnchantID]) : result - Previews an item on the model.
DressUpModel:Undress()
DressUpModel:UndressSlot(inventorySlot)

TabardModel
TabardModel:GetLowerBackgroundFileName() : file
TabardModel:GetLowerBorderFile() : file
TabardModel:GetLowerEmblemFile() : file
TabardModel:GetUpperBackgroundFileName() : file
TabardModel:GetUpperBorderFile() : file
TabardModel:GetUpperEmblemFile() : file
TabardModelBase:CanSaveTabardNow() : canSave
TabardModelBase:CycleVariation(variationIndex, delta)
TabardModelBase:GetLowerEmblemTexture(texture)
TabardModelBase:GetUpperEmblemTexture(texture)
TabardModelBase:InitializeTabardColors()
TabardModelBase:IsGuildTabard() : isGuildTabard
TabardModelBase:Save()

ModelScene
ModelScene:CreateActor([name, template]) : actor
ModelScene:GetActorAtIndex(index) : actor
ModelScene:GetAllowOverlappedModels() : allowOverlappedModels
ModelScene:GetCameraFarClip() : farClip
ModelScene:GetCameraFieldOfView() : fov
ModelScene:GetCameraForward() : forwardX, forwardY, forwardZ
ModelScene:GetCameraNearClip() : nearClip
ModelScene:GetCameraRight() : rightX, rightY, rightZ
ModelScene:GetCameraUp() : upX, upY, upZ
ModelScene:GetDrawLayer() : layer, sublevel
ModelScene:GetLightAmbientColor() : colorR, colorG, colorB
ModelScene:GetLightDiffuseColor() : colorR, colorG, colorB
ModelScene:GetLightDirection() : directionX, directionY, directionZ
ModelScene:GetLightPosition() : positionX, positionY, positionZ
ModelScene:GetLightType() : lightType
ModelScene:GetNumActors() : numActors
ModelScene:IsLightVisible() : isVisible
ModelScene:Project3DPointTo2D(pointX, pointY, pointZ) : point2DX, point2DY, depth - Converts a 3 dimensional point into clip space using the model scene camera properties.
ModelScene:SetAllowOverlappedModels(allowOverlappedModels)
ModelScene:SetCameraFarClip(farClip)
ModelScene:SetCameraFieldOfView(fov)
ModelScene:SetCameraNearClip(nearClip)
ModelScene:SetCameraOrientationByAxisVectors(forwardX, forwardY, forwardZ, rightX, rightY, rightZ, upX, upY, upZ)
ModelScene:SetCameraOrientationByYawPitchRoll(yaw, pitch, roll)
ModelScene:SetDrawLayer(layer)
ModelScene:SetLightAmbientColor(colorR, colorG, colorB)
ModelScene:SetLightDiffuseColor(colorR, colorG, colorB)
ModelScene:SetLightDirection(directionX, directionY, directionZ)
ModelScene:SetLightPosition(positionX, positionY, positionZ)
ModelScene:SetLightType(lightType)
ModelScene:SetLightVisible([visible])
ModelScene:SetPaused(paused [, affectsGlobalPause])
ModelScene:TakeActor()

ModelSceneActor
ModelSceneActor:AttachToMount(rider, animation [, spellKitVisualID]) : success
ModelSceneActor:CalculateMountScale(rider) : scale
ModelSceneActor:DetachFromMount(rider) : success
ModelSceneActor:DressPlayerSlot(invSlot)
ModelSceneActor:GetPaused() : paused, globalPaused
ModelSceneActor:ReleaseFrontEndCharacterDisplays() : success
ModelSceneActor:ResetNextHandSlot()
ModelSceneActor:SetFrontEndLobbyModelFromDefaultCharacterDisplay(characterIndex) : success
ModelSceneActor:SetModelByHyperlink(link) : success
ModelSceneActor:SetSheathedCategory(inventorySlots, category)
ModelSceneActor:SetPaused(paused [, affectsGlobalPause])
ModelSceneActor:UseUnitSheatheCategory(useCategory)

ModelSceneActorBase:GetActiveBoundingBox() : boxBottom, boxTop
ModelSceneActorBase:GetAnimation() : animation
ModelSceneActorBase:GetAnimationBlendOperation() : blendOp
ModelSceneActorBase:GetAnimationVariation() : variation
ModelSceneActorBase:GetMaxBoundingBox() : boxBottom, boxTop
ModelSceneActorBase:GetModelPath() : path
ModelSceneActorBase:GetModelUnitGUID() : guid
ModelSceneActorBase:GetParticleOverrideScale() : scale
ModelSceneActorBase:GetSpellVisualKit() : spellVisualKitID
ModelSceneActorBase:GetYaw() : yaw
ModelSceneActorBase:IsLoaded() : isLoaded
ModelSceneActorBase:IsPreferringModelCollisionBounds() : preferringCollisionBounds
ModelSceneActorBase:IsUsingCenterForOrigin() : x, y, z
ModelSceneActorBase:PlayAnimationKit(animationKit [, isLooping])
ModelSceneActorBase:SetAnimation(animation [, variation, animSpeed, animOffsetSeconds])
ModelSceneActorBase:SetAnimationBlendOperation(blendOp)
ModelSceneActorBase:SetGradientMask(gradientIndex0, gradientIndex1, gradientIndex2, gradientIndex3)
ModelSceneActorBase:SetGradientMaskWithDyes([grad0DyeColorID [, grad1DyeColorID [, grad2DyeColorID]]])
ModelSceneActorBase:SetModelByCreatureDisplayID(creatureDisplayID [, useActivePlayerCustomizations]) : success
ModelSceneActorBase:SetModelByFileID(asset [, useMips]) : success
ModelSceneActorBase:SetModelByPath(asset [, useMips]) : success
ModelSceneActorBase:SetModelByUnit(unit [, sheatheWeapons [, autoDress [, hideWeapons [, usePlayerNativeForm [, holdBowString [, customRaceID]]]]]]) : success
ModelSceneActorBase:SetParticleOverrideScale([scale])
ModelSceneActorBase:SetPlayerModelFromGlues([characterIndex [, sheatheWeapons [, autoDress [, hideWeapons [, usePlayerNativeForm [, customRaceID]]]]]]) : success
ModelSceneActorBase:SetPreferModelCollisionBounds(preferCollisionBounds)
ModelSceneActorBase:SetSpellVisualKit([spellVisualKitID, oneShot])
ModelSceneActorBase:SetUseCenterForOrigin([x, y, z])
ModelSceneActorBase:SetYaw(yaw)
ModelSceneActorBase:StopAnimationKit()

EditBox
EditBox:AddHistoryLine(text) - Adds text to the edit history.
EditBox:ClearFocus() - Removes text input focus from this editbox element.
EditBox:ClearHighlightText()
EditBox:ClearHistory()
EditBox:Disable()
EditBox:Enable()
EditBox:GetAltArrowKeyMode() : altMode
EditBox:GetBlinkSpeed() : cursorBlinkSpeedSec - Returns the blink speed.
EditBox:GetCursorPosition() : cursorPosition - Returns the cursor position in the editbox.
EditBox:GetDisplayText() : displayText
EditBox:GetHighlightColor() : colorR, colorG, colorB, colorA
EditBox:GetHistoryLines() : numHistoryLines - Returns the number of history lines for this editbox.
EditBox:GetInputLanguage() : language - Returns the input language (locale based not in-game).
EditBox:GetMaxBytes() : maxBytes
EditBox:GetMaxLetters() : maxLetters
EditBox:GetNumLetters() : numLetters - Returns the number of letters in the editbox.
EditBox:GetNumLines() : lines
EditBox:GetNumber() : number - Returns the number entered in the editbox, or 0 if editbox text is not a number.
EditBox:GetText() : text - Returns the current text contained in the edit box.
EditBox:GetTextInsets() : left, right, top, bottom - Returns a list of left,right,top,bottom text insets.
EditBox:GetUTF8CursorPosition() : cursorPosition
EditBox:GetVisibleTextByteLimit() : maxVisibleBytes
EditBox:HasFocus() : hasFocus - Returns true if the edit box has the focus.
EditBox:HasText() : hasText
EditBox:HighlightText([start, stop]) - Highlights all or some of the edit box text.
EditBox:Insert(text) - Insert text into the editbox.
EditBox:IsAlphabeticOnly() : enabled
EditBox:IsAutoFocus() : autoFocus
EditBox:IsCountInvisibleLetters() : countInvisibleLetters
EditBox:IsEnabled() : isEnabled
EditBox:IsInIMECompositionMode() : isInIMECompositionMode
EditBox:IsMultiLine() : multiline
EditBox:IsNumeric() : isNumeric
EditBox:IsNumericFullRange() : isNumeric
EditBox:IsPassword() : isPassword
EditBox:IsSecureText() : isSecure
EditBox:ResetInputMode()
EditBox:SetAlphabeticOnly([enabled])
EditBox:SetAltArrowKeyMode([altMode])
EditBox:SetAutoFocus([autoFocus])
EditBox:SetBlinkSpeed(cursorBlinkSpeedSec)
EditBox:SetCountInvisibleLetters([countInvisibleLetters])
EditBox:SetCursorPosition(cursorPosition) - Sets the cursor position in the editbox.
EditBox:SetEnabled([enabled])
EditBox:SetFocus()
EditBox:SetHighlightColor(colorR, colorG, colorB [, a])
EditBox:SetHistoryLines(numHistoryLines) - Sets the number of history lines to remember.
EditBox:SetMaxBytes(maxBytes) - Sets the maximum byte size for entered text.
EditBox:SetMaxLetters(maxLetters) - Sets the maximum number of letters for entered text.
EditBox:SetMultiLine([multiline])
EditBox:SetNumber(number)
EditBox:SetNumeric([isNumeric])
EditBox:SetNumericFullRange([isNumeric])
EditBox:SetPassword([isPassword])
EditBox:SetSecureText([isSecure])
EditBox:SetSecurityDisablePaste()
EditBox:SetSecurityDisableSetText()
EditBox:SetText(text) - Sets the text contained in the edit box.
EditBox:SetTextInsets(left, right, top, bottom)
EditBox:SetVisibleTextByteLimit(maxVisibleBytes)
EditBox:ToggleInputLanguage()

MessageFrame
MessageFrame:AddMessage(text [, colorR, colorG, colorB [, a [, messageID]]]))
MessageFrame:Clear()
MessageFrame:GetFadeDuration() : fadeDurationSeconds
MessageFrame:GetFadePower() : fadePower
MessageFrame:GetFading() : isFading
MessageFrame:GetFontStringByID(messageID) : fontString
MessageFrame:GetInsertMode() : mode
MessageFrame:GetTimeVisible() : timeVisibleSeconds
MessageFrame:HasMessageByID(messageID) : hasMessage
MessageFrame:ResetMessageFadeByID(messageID)
MessageFrame:SetFadeDuration(fadeDurationSeconds)
MessageFrame:SetFadePower(fadePower)
MessageFrame:SetFading(fading)
MessageFrame:SetInsertMode(mode)
MessageFrame:SetTimeVisible(timeVisibleSeconds)

SimpleHTML
SimpleHTML:GetContentHeight() : height
SimpleHTML:GetHyperlinkFormat() : format
SimpleHTML:GetTextData() : content
SimpleHTML:SetHyperlinkFormat(format)
SimpleHTML:SetText(text [, ignoreMarkup])

GameTooltip
GameTooltip:AddAtlas(atlas [, textureInfoTable])
GameTooltip:AddDoubleLine(leftText, rightText [, leftR, leftG, leftB [, rightR, rightG, rightB]])
GameTooltip:AddFontStrings(leftstring, rightstring)
GameTooltip:AddLine(tooltipText [, r, g, b, wrapText])
GameTooltip:AddTexture(texture)
GameTooltip:AppendText(text)
GameTooltip:ClearLines()
GameTooltip:ClearPadding()
GameTooltip:CopyTooltip()
GameTooltip:FadeOut()
GameTooltip:GetAnchorType() : anchorType
GameTooltip:GetCustomLineSpacing() : spacing
GameTooltip:GetLeftLine(line) : leftFontString
GameTooltip:GetMinimumWidth() : width, force
GameTooltip:GetOwner() : owner
GameTooltip:GetPadding() : right, bottom, left, top
GameTooltip:GetRightLine(line) : rightFontString
GameTooltip:IsOwned(frame) : bool
GameTooltip:NumLines() : lines
GameTooltip:SetAllowShowWithNoLines([bool])
GameTooltip:SetAnchorType(anchorType [, Xoffset, Yoffset])
GameTooltip:SetCustomLineSpacing([spacing])
GameTooltip:SetCustomWordWrapMinWidth([width)
GameTooltip:SetFrameStack([showHidden, showRegion, highlightIndexChanged])
GameTooltip:SetMinimumWidth(width [, force])
GameTooltip:SetObjectTooltipPosition()
GameTooltip:SetOwner(owner, anchor [, ofsX, ofsY])
GameTooltip:SetPadding(right, bottom [, left, top])
GameTooltip:SetShrinkToFitWrapped()
GameTooltip:SetText(text [, r, g, b, alpha, textWrap])
GameTooltip:SetAchievementByID(achievementID)
GameTooltip:SetAction(actionID)
GameTooltip:SetArtifactItem()
GameTooltip:SetArtifactPowerByID(powerID)
GameTooltip:SetAzeriteEssence(essenceID [, rank])
GameTooltip:SetAzeriteEssenceSlot(slot)
GameTooltip:SetAzeritePower(itemID, itemLevel, powerID [, owningItemLink])
GameTooltip:SetBackpackToken(index)
GameTooltip:SetBagItem(bagIndex, slotIndex)
GameTooltip:SetBagItemChild(bagIndex, slotIndex, equipSlotIndex)
GameTooltip:SetBuybackItem(index)
GameTooltip:SetCompanionPet(petGUID)
GameTooltip:SetConduit(conduitID, conduitRank)
GameTooltip:SetCurrencyByID(currencyID [, amount])
GameTooltip:SetCurrencyToken(tokenIndex)
GameTooltip:SetEnhancedConduit(conduitID, rank)
GameTooltip:SetEquipmentSet(setID)
GameTooltip:SetExistingSocketGem(index [, toDestroy])
GameTooltip:SetGuildBankItem(tab, slot)
GameTooltip:SetHeirloomByItemID(itemID)
GameTooltip:SetHyperlink(hyperlink [, optionalArg1, optionalArg2, hideVendorPrice])
GameTooltip:SetInboxItem(messageIndex [, attachmentIndex])
GameTooltip:SetInstanceLockEncountersComplete(index)
GameTooltip:SetInventoryItem(unit, slot [, hideUselessStats])
GameTooltip:SetInventoryItemByID(itemID)
GameTooltip:SetItemByGUID(guid)
GameTooltip:SetItemByID(itemID [, quality])
GameTooltip:SetItemInteractionItem()
GameTooltip:SetItemKey(itemID, itemLevel, itemSuffix [, requiredLevel])
GameTooltip:SetLFGDungeonReward(dungeonID, lootIndex)
GameTooltip:SetLFGDungeonShortageReward(dungeonID, shortageSeverity, lootIndex)
GameTooltip:SetLootCurrency(slot)
GameTooltip:SetLootItem(slot)
GameTooltip:SetLootRollItem(id)
GameTooltip:SetMerchantCostItem(slot, costIndex)
GameTooltip:SetMerchantItem(slot)
GameTooltip:SetMinimapMouseover()
GameTooltip:SetMountBySpellID(spellID [, checkIndoors])
GameTooltip:SetOwnedItemByID(itemID)
GameTooltip:SetPetAction(slot)
GameTooltip:SetPossession(slot)
GameTooltip:SetPvpBrawl([isSpecial])
GameTooltip:SetPvpTalent(talentID [, isInspect, groupIndex, talentIndex])
GameTooltip:SetQuestCurrency(type, currencyIndex)
GameTooltip:SetQuestItem(type, itemIndex [, allowCollectionText])
GameTooltip:SetQuestLogCurrency(type, currencyIndex [, questID])
GameTooltip:SetQuestLogItem(type, itemIndex [, questID, allowCollectionText])
GameTooltip:SetQuestLogSpecialItem(questIndex)
GameTooltip:SetQuestPartyProgress(questID [, omitTitle, ignoreActivePlayer])
GameTooltip:SetRecipeRankInfo(recipeID, rank)
GameTooltip:SetRecipeReagentItem(recipeSpellID, dataSlotIndex)
GameTooltip:SetRecipeResultItem(recipeID [, craftingReagents, recraftItemGUID, recipeLevel, overrideQualityID])
GameTooltip:SetRecipeResultItemForOrder(recipeID [, craftingReagents, orderID, recipeLevel, overrideQualityID])
GameTooltip:SetRuneforgeResultItem(itemGUID, itemLevel [, powerID, modifiers])
GameTooltip:SetSendMailItem([attachmentIndex])
GameTooltip:SetShapeshift(slot)
GameTooltip:SetSlottedKeystone()
GameTooltip:SetSocketedItem()
GameTooltip:SetSocketedRelic(slotIndex)
GameTooltip:SetSocketGem(index)
GameTooltip:SetSpellBookItem(index, spellBank)
GameTooltip:SetSpellByID(spellID [, isPet, showSubtext, dontOverride, difficultyID, isLink])
GameTooltip:SetTalent(talentID [, isInspect, groupIndex])
GameTooltip:SetTotem(slot)
GameTooltip:SetToyByItemID(itemID)
GameTooltip:SetTradePlayerItem(slot)
GameTooltip:SetTradeTargetItem(slot)
GameTooltip:SetTrainerService(serviceIndex)
GameTooltip:SetTraitEntry(entryID [, rank])
GameTooltip:SetTransmogrifyItem(transmogLocation)
GameTooltip:SetUnit(unit [, hideStatus])
GameTooltip:SetUnitAura(unitToken, index [, filter])
GameTooltip:SetUnitBuff(unitToken, index [, filter])
GameTooltip:SetUnitBuffByAuraInstanceID(unitTokenString, auraInstanceID [, filter])
GameTooltip:SetUnitDebuff(unitToken, index [, filter])
GameTooltip:SetUnitDebuffByAuraInstanceID(unitTokenString, auraInstanceID [, filter])
GameTooltip:SetUpgradeItem()
GameTooltip:SetVoidDepositItem(slot)
GameTooltip:SetVoidItem(tab, slot)
GameTooltip:SetVoidWithdrawalItem(slot)
GameTooltip:SetWeeklyReward(itemDBID)
GameTooltip:SetWorldCursor()
GameTooltip:SetWorldLootObject(unitTokenString)

ColorSelect
ColorSelect:ClearColorWheelTexture()
ColorSelect:GetColorAlpha() : alpha
ColorSelect:GetColorAlphaTexture() : texture
ColorSelect:GetColorAlphaThumbTexture() : texture
ColorSelect:GetColorHSV() : hsvX, hsvY, hsvZ - Returns the HSV values of the selected color.
ColorSelect:GetColorRGB() : rgbR, rgbG, rgbB - Returns the RGB values of the selected color.
ColorSelect:GetColorValueTexture() : texture - Returns the texture for the color picker's value slider background.
ColorSelect:GetColorValueThumbTexture() : texture - Returns the texture for the color picker's value slider thumb.
ColorSelect:GetColorWheelTexture() : texture - Returns the texture for the color picker's hue/saturation wheel.
ColorSelect:GetColorWheelThumbTexture() : texture - Returns the texture for the selection indicator on the color picker's hue/saturation wheel.
ColorSelect:SetColorAlpha(alpha)
ColorSelect:SetColorAlphaTexture(texture)
ColorSelect:SetColorAlphaThumbTexture(texture)
ColorSelect:SetColorHSV(hsvX, hsvY, hsvZ) - Selects this HSV color in the color picker.
ColorSelect:SetColorRGB(rgbR, rgbG, rgbB) - Selects this RGB color in the color picker.
ColorSelect:SetColorValueTexture(texture) - Sets the texture used to display the color picker's value slider.
ColorSelect:SetColorValueThumbTexture(texture) - Sets the texture for the color picker's value slider thumb.
ColorSelect:SetColorWheelTexture(texture) - Sets the texture used to display the color picker's hue/saturation wheel.
ColorSelect:SetColorWheelThumbTexture(texture) - Sets the texture for the selection indicator on the color picker's hue/saturation wheel.

Cooldown
Cooldown:Clear() - Clears the currently active cooldown of the widget.
Cooldown:GetCooldownDisplayDuration() : duration
Cooldown:GetCooldownDuration() : duration - Returns the duration currently shown by the cooldown frame in milliseconds.
Cooldown:GetCooldownTimes() : start, duration - Returns the starting time and duration of the cooldown frame in milliseconds.
Cooldown:GetCountdownAbbrevThreshold() : seconds
Cooldown:GetCountdownFontString() : countdownString
Cooldown:GetCountdownFormatter() : formatter
Cooldown:GetCountdownMillisecondsThreshold() : seconds
Cooldown:GetDrawBling() : drawBling
Cooldown:GetDrawEdge() : drawEdge - Returns true if a bright line should be drawn on the moving edge of the cooldown animation.
Cooldown:GetDrawSwipe() : drawSwipe
Cooldown:GetEdgeScale() : edgeScale
Cooldown:GetHideCountdownNumbers() : hideNumbers
Cooldown:GetMinimumCountdownDuration(milliseconds)
Cooldown:GetReverse() : reverse - Returns true if the bright and dark portions of the cooldown animation should be inverted.
Cooldown:GetRotation() : rotationRadians - Get the current rotation of the cooldown in radians.
Cooldown:GetUseAuraDisplayTime() : useAuraDisplayTime
Cooldown:IsPaused() : isPaused - Returns true if the cooldown is currently paused.
Cooldown:Pause() - Pauses the cooldown.
Cooldown:Resume() - Resumes the cooldown after being paused.
Cooldown:SetBlingTexture(texture [, colorR, colorG, colorB, colorA])
Cooldown:SetCooldown(start, duration [, modRate]) - Shows a cooldown animation.
Cooldown:SetCooldownDuration(duration [, modRate])
Cooldown:SetCooldownFromDurationObject(duration [, clearIfZero])
Cooldown:SetCooldownFromExpirationTime(expirationTime, duration [, modRate])
Cooldown:SetCooldownUNIX(start, duration [, modRate])
Cooldown:SetCountdownAbbrevThreshold(seconds)
Cooldown:SetCountdownFont(fontName)
Cooldown:SetCountdownFormatter([formatter])
Cooldown:SetCountdownMillisecondsThreshold(seconds)
Cooldown:SetDrawBling([drawBling])
Cooldown:SetDrawEdge([drawEdge]) - Sets whether a bright line should be drawn on the moving edge of the cooldown animation.
Cooldown:SetDrawSwipe([drawSwipe])
Cooldown:SetEdgeColor(colorR, colorG, colorB [, a])
Cooldown:SetEdgeScale(scale)
Cooldown:SetEdgeTexture(texture [, colorR, colorG, colorB, colorA]) - Sets the texture which 'follows' the moving edge of the cooldown.
Cooldown:SetHideCountdownNumbers([hideNumbers]) - Show or hide text cooldown timer.
Cooldown:SetMinimumCountdownDuration() : milliseconds
Cooldown:SetPaused(paused)
Cooldown:SetReverse([reverse]) - Controls the direction of the cooldown animation.
Cooldown:SetRotation(rotationRadians) - Rotate the entire cooldown a certain radians clockwise.
Cooldown:SetSwipeColor(colorR, colorG, colorB [, a]) - Sets the color of the swipe
Cooldown:SetSwipeTexture(texture [, colorR, colorG, colorB, colorA]) - Sets the swipe texture used for the cooldown
Cooldown:SetTexCoordRange(low, high)
Cooldown:SetUseAuraDisplayTime([useAuraDisplayTime])
Cooldown:SetUseCircularEdge([useCircularEdge]) - Sets whether the edge texture should follow a circular pattern instead of square.

Minimap
Minimap:GetPingPosition() : positionX, positionY - Get the last ping location.
Minimap:GetZoom() : zoomFactor - Get the current zoom level.
Minimap:GetZoomLevels() : zoomLevels - Get the maximum zoom level.
Minimap:PingLocation([locationX, locationY]) - Perform a ping at the specified location.
Minimap:SetArchBlobInsideAlpha(alpha)
Minimap:SetArchBlobInsideTexture(asset)
Minimap:SetArchBlobOutsideAlpha(alpha)
Minimap:SetArchBlobOutsideTexture(asset)
Minimap:SetArchBlobRingAlpha(alpha)
Minimap:SetArchBlobRingScalar(scalar)
Minimap:SetArchBlobRingTexture(asset)
Minimap:SetIconScale(scale)
Minimap:SetMaskTexture(asset)
Minimap:SetQuestBlobInsideAlpha(alpha)
Minimap:SetQuestBlobInsideTexture(asset)
Minimap:SetQuestBlobOutsideAlpha(alpha)
Minimap:SetQuestBlobOutsideTexture(asset)
Minimap:SetQuestBlobRingAlpha(alpha)
Minimap:SetQuestBlobRingScalar(scalar)
Minimap:SetQuestBlobRingTexture(asset)
Minimap:SetTaskBlobInsideAlpha(alpha)
Minimap:SetTaskBlobInsideTexture(asset)
Minimap:SetTaskBlobOutsideAlpha(alpha)
Minimap:SetTaskBlobOutsideTexture(asset)
Minimap:SetTaskBlobRingAlpha(alpha)
Minimap:SetTaskBlobRingScalar(scalar)
Minimap:SetTaskBlobRingTexture(asset)
Minimap:SetZoom(zoomFactor) - Set the current zoom level.
Minimap:UpdateBlips()

MovieFrame
MovieFrame:EnableSubtitles(enable) - Enables or disables subtitles for movies played in the frame.
MovieFrame:StartMovie(movieID [, looping]) : success, returnCode - Plays a specified movie in the frame.
MovieFrame:StartMovieByName(movieName [, looping [, resolution]]) : success, returnCode - This method is deprecated and does nothing.
MovieFrame:StopMovie() - Stops the movie currently playing in the frame.

NamePlate
NamePlate:CanChangeHitTestPoints() : canChangeHitTestPoints
NamePlate:ClearAllHitTestPoints()
NamePlate:GetHitTestPoints() : anchors
NamePlate:SetAllHitTestPoints(relativeTo)
NamePlate:SetHitTestPoints(anchors)
NamePlate:SetStackingBoundsFrame(frame)

ScrollFrame
ScrollFrame:GetHorizontalScroll() : offset
ScrollFrame:GetHorizontalScrollRange() : range
ScrollFrame:GetScrollChild() : scrollChild - Returns the frame that scrolls when moving the scroll bar.
ScrollFrame:GetVerticalScroll() : offset
ScrollFrame:GetVerticalScrollRange() : range
ScrollFrame:SetHorizontalScroll(offset)
ScrollFrame:SetScrollChild(scrollChild) - Assigns the frame to scroll when moving the scroll bar.
ScrollFrame:SetVerticalScroll(offset)
ScrollFrame:UpdateScrollChildRect()

Slider
Slider:Disable() - Disables the slider.
Slider:Enable() - Enables the slider
Slider:GetMinMaxValues() : minValue, maxValue - Returns the current bounds of the slider.
Slider:GetObeyStepOnDrag() : isObeyStepOnDrag - Returns whether the slider constrains values to value steps when dragged.
Slider:GetOrientation() : orientation - Returns the slider orientation.
Slider:GetStepsPerPage() : stepsPerPage - Returns the number of steps the slider's value changes by when the slider is clicked.
Slider:GetThumbTexture() : texture - Returns the texture for this slider's thumb,
Slider:GetValue() : value - Returns the current value of the slider.
Slider:GetValueStep() : valueStep - Returns the current step size of the slider.
Slider:IsDraggingThumb() : isDraggingThumb
Slider:IsEnabled() : enabled - Returns the enabled status of the slider.
Slider:SetEnabled(enabled)
Slider:SetMinMaxValues(minValue, maxValue) - Sets the bounds of the slider.
Slider:SetObeyStepOnDrag(obeyStepOnDrag) - Sets whether the slider constrains values to to value steps when dragged.
Slider:SetOrientation(orientation) - Sets the orientation of the slider.
Slider:SetStepsPerPage(stepsPerPage) - Controls slider behavior when the user clicks within the slider's tracking area.
Slider:SetThumbTexture(asset)
Slider:SetValue(value [, treatAsMouseEvent]) - Sets the value of the slider.
Slider:SetValueStep(valueStep) - Sets the step size of the slider.

StatusBar
StatusBar:GetFillStyle() : fillStyle
StatusBar:GetInterpolatedValue() : value
StatusBar:GetMinMaxValues() : minValue, maxValue - Returns the current bounds of the statusbar.
StatusBar:GetOrientation() : orientation
StatusBar:GetRenderMode() : renderMode
StatusBar:GetReverseFill() : isReverseFill
StatusBar:GetRotatesTexture() : rotatesTexture
StatusBar:GetStatusBarColor() : colorR, colorG, colorB, colorA
StatusBar:GetStatusBarDesaturation() : desaturation
StatusBar:GetStatusBarTexture() : texture - Returns the texture object for the statusbar.
StatusBar:GetTimerDuration() : duration
StatusBar:GetValue() : value - Returns the current value of the statusbar.
StatusBar:IsInterpolating() : isInterpolating
StatusBar:IsStatusBarDesaturated() : desaturated
StatusBar:SetColorFill(colorR, colorG, colorB [, a])
StatusBar:SetFillStyle(fillStyle) - Set the style in which the statusbar will be filled.
StatusBar:SetMinMaxValues(minValue, maxValue [, interpolation]) - Set the bounds of the statusbar.
StatusBar:SetOrientation(orientation) - Sets the orientation of the statusbar.
StatusBar:SetRenderMode(renderMode)
StatusBar:SetReverseFill(isReverseFill) - Sets the fill direction of the statusbar.
StatusBar:SetRotatesTexture(rotatesTexture)
StatusBar:SetStatusBarColor(colorR, colorG, colorB [, a]) - Set the color of the statusbar.
StatusBar:SetStatusBarDesaturated([desaturated])
StatusBar:SetStatusBarDesaturation(desaturation)
StatusBar:SetStatusBarTexture(asset) : success - Sets the texture of the statusbar.
StatusBar:SetTimerDuration(duration [, interpolation, direction])
StatusBar:SetToTargetValue()
StatusBar:SetValue(value [, interpolation]) - Set the value of the statusbar.

FogOfWarFrame
FogOfWarFrame:GetFogOfWarBackgroundAtlas() : atlas
FogOfWarFrame:GetFogOfWarBackgroundTexture() : asset
FogOfWarFrame:GetFogOfWarMaskAtlas() : atlas
FogOfWarFrame:GetFogOfWarMaskTexture() : asset
FogOfWarFrame:GetMaskScalar() : scalar
FogOfWarFrame:GetUiMapID() : uiMapID
FogOfWarFrame:SetFogOfWarBackgroundAtlas(atlas)
FogOfWarFrame:SetFogOfWarBackgroundTexture(asset, horizontalTile, verticalTile)
FogOfWarFrame:SetFogOfWarMaskAtlas(atlas)
FogOfWarFrame:SetFogOfWarMaskTexture(asset)
FogOfWarFrame:SetMaskScalar(scalar)
FogOfWarFrame:SetUiMapID(uiMapID)

UnitPositionFrame
UnitPositionFrame:AddUnit(unitTokenString, asset [, width, height, r, g, b, a, sublayer, showFacing])
UnitPositionFrame:ClearUnits()
UnitPositionFrame:FinalizeUnits()
UnitPositionFrame:GetMouseOverUnits() : ...units
UnitPositionFrame:GetPlayerPingScale() : scale
UnitPositionFrame:GetUiMapID() : mapID
UnitPositionFrame:SetPlayerPingScale(scale)
UnitPositionFrame:SetPlayerPingTexture(textureType, asset [, width, height])
UnitPositionFrame:SetUiMapID(mapID)
UnitPositionFrame:SetUnitColor(unit, colorR, colorG, colorB, colorA)
UnitPositionFrame:StartPlayerPing([duration, fadeDuration])
UnitPositionFrame:StopPlayerPing()

HousingFixturePointFrame
HousingFixturePointFrame:HasAttachedFixture() : hasAttachedFixture
HousingFixturePointFrame:IsSelected() : isSelected
HousingFixturePointFrame:IsValid() : isValid
HousingFixturePointFrame:Select()
HousingFixturePointFrame:SetUpdateCallback(cb)

HousingLayoutPinFrame
HousingLayoutPinFrame:CanMove() : moveRestriction
HousingLayoutPinFrame:CanRemove() : removalRestriction
HousingLayoutPinFrame:CanRotate() : rotateRestriction
HousingLayoutPinFrame:Drag(isAccessible)
HousingLayoutPinFrame:GetDoorConnectionInfo() : connectionInfo
HousingLayoutPinFrame:GetPinType() : type
HousingLayoutPinFrame:GetRoomGUID() : roomGUID
HousingLayoutPinFrame:GetRoomName() : name
HousingLayoutPinFrame:IsAnyPartOfRoomSelected() : isSelected
HousingLayoutPinFrame:IsConnectedToDraggingRoom() : isConnectedToDraggingRoom
HousingLayoutPinFrame:IsOccupiedDoor() : isOccupied
HousingLayoutPinFrame:IsPartOfDraggingRoom() : isPartOfDraggingRoom
HousingLayoutPinFrame:IsSelected() : isSelected
HousingLayoutPinFrame:IsValid() : isValid
HousingLayoutPinFrame:IsValidForSelectedFloorplan() : isValid
HousingLayoutPinFrame:Select()
HousingLayoutPinFrame:SetUpdateCallback(cb)

Blob
Blob:DrawAll()
Blob:DrawBlob(questID [, draw])
Blob:DrawNone()
Blob:EnableMerging([enable])
Blob:EnableSmoothing([enable])
Blob:GetMapID() : uiMapID
Blob:SetBorderAlpha(alpha)
Blob:SetBorderScalar(scalar)
Blob:SetBorderTexture(asset)
Blob:SetFillAlpha(alpha)
Blob:SetFillTexture(asset)
Blob:SetMapID(uiMapID)
Blob:SetMergeThreshold(threshold)
Blob:SetNumSplinePoints(numSplinePoints)

ArchaeologyDigSiteFrame <inherits Blob>

QuestPOIFrame
QuestPOIFrame:GetNumTooltips() : numObjectives
QuestPOIFrame:GetTooltipIndex(index) : objectiveIndex
QuestPOIFrame:UpdateMouseOverTooltip(x, y) : questID, numObjectives

ScenarioPOIFrame
ScenarioPOIFrame:GetScenarioTooltipText() : tooltipText
ScenarioPOIFrame:UpdateMouseOverTooltip(x, y) : hasTooltip

Intrinsics

AuraButton
AuraButton:GetTooltipAnchorPoint() : tooltipAnchorPoint, tooltipOffsetX, tooltipOffsetY
AuraButton:SetCancelAuraButtons(cancelAuraButtons)
AuraButton:SetHideTooltipInCombat(hideInCombat)
AuraButton:SetTooltipAnchorPoint(point, offsetX, offsetY)
AuraButton:ShouldHideTooltipInCombat() : tooltipHideInCombat

AuraContainer
AuraContainer:GetUnit() : unitToken
AuraContainer:IsEnabled() : isEnabled
AuraContainer:SetEnabled(enabled)
AuraContainer:SetUnit(unitToken)
AuraContainer:UpdateAllAuras()

ContainedAlertFrame
ContainedAlertFrame:GetAlertContainer() : alertContainer
ContainedAlertFrame:ManagesOwnOutroAnimation() : unknown
ContainedAlertFrame:OnManagedAlertFrameVisibilityChanged()
ContainedAlertFrame:SetAlertContainer(container)
ContainedAlertFrame:SetExternallyManagedOutroAnimation(externallyManagedAnimation)

DropdownButton
DropdownButton:ClearMenuState()
DropdownButton:CloseMenu()
DropdownButton:CollectSelectionData() : unknown
DropdownButton:CopyDeferredCallbacks(callbackType, event, target)
DropdownButton:CreateDefaultRootMenuDescription() : unknown
DropdownButton:CreateRootDescription(menuMixin) : unknown
DropdownButton:Decrement()
DropdownButton:EnableRegenerateOnResponse()
DropdownButton:GenerateCallbackEvents(eventTable)
DropdownButton:GenerateMenu()
DropdownButton:GetCallbacksByEvent(callbackType, event) : event
DropdownButton:GetCallbackTable(callbackType) : unknown
DropdownButton:GetCallbackTables() : callbackTables
DropdownButton:GetMenuDescription() : menuDescription
DropdownButton:GetMutableCallbacksByEvent(callbackType, event) : mutableCallbacksByEvent
DropdownButton:GetSelectionData() : selectionData
DropdownButton:HandlesGlobalMouseEvent(buttonName, event) : unknown
DropdownButton:HasAnyRadioDescriptions() : hasAnyRadioDescriptions
DropdownButton:HasElements() : hasElements
DropdownButton:HasRegistrantsForEvent(event) : hasRegistrantsForEvent
DropdownButton:HasStickyFocus() : hasStickyFocus
DropdownButton:Increment()
DropdownButton:IsMenuOpen() : isMenuOpen
DropdownButton:OnLoad()
DropdownButton:OnMenuAssigned()
DropdownButton:OnMenuChanged()
DropdownButton:OnMenuClosed(menu, closeReason)
DropdownButton:OnMenuOpened(menu)
DropdownButton:OnMenuResponse(menu, description)
DropdownButton:OpenMenu()
DropdownButton:Pick(description, menuInputContext, menuInputButtonName) : unknown
DropdownButton:ReconcileDeferredCallbacks(event, closures, funcs)
DropdownButton:RegisterCallback(event, func, owner, ...) : owner
DropdownButton:RegisterCallbackWithHandle(event, func, owner, ...) : unknown
DropdownButton:RegisterMenu(menuDescription)
DropdownButton:Rotate(forward)
DropdownButton:SecureInsertEvent(event)
DropdownButton:SetMenuAnchor(anchor)
DropdownButton:SetMenuOpen(open)
DropdownButton:SetUndefinedEventsAllowed(allowed)
DropdownButton:SetupMenu(generator)
DropdownButton:SignalUpdate()
DropdownButton:TriggerEvent(event, ...)
DropdownButton:UnregisterCallback(event, owner)
DropdownButton:UnregisterEvents()
DropdownButton:UnregisterEventsByEventTable(eventTable)
DropdownButton:Update()
DropdownButton:UpdateSelections(selections)
DropdownButton:UpdateToMenuSelections(menuDescription, selections)

DropDownToggleButton
DropDownToggleButton:HandlesGlobalMouseEvent(buttonName, event) : unknown

EventButton
EventButton:CopyDeferredCallbacks(callbackType, event, target)
EventButton:GenerateCallbackEvents(eventTable)
EventButton:GetCallbacksByEvent(callbackType, event) : event
EventButton:GetCallbackTable(callbackType) : unknown
EventButton:GetCallbackTables() : callbackTables
EventButton:GetMutableCallbacksByEvent(callbackType, event) : mutableCallbacksByEvent
EventButton:HasRegistrantsForEvent(event) : hasRegistrantsForEvent
EventButton:OnLoad()
EventButton:ReconcileDeferredCallbacks(event, closures, funcs)
EventButton:RegisterCallback(event, func, owner, ...) : owner
EventButton:RegisterCallbackWithHandle(event, func, owner, ...) : unknown
EventButton:SecureInsertEvent(event)
EventButton:SetUndefinedEventsAllowed(allowed)
EventButton:TriggerEvent(event, ...)
EventButton:UnregisterCallback(event, owner)
EventButton:UnregisterEvents()
EventButton:UnregisterEventsByEventTable(eventTable)

EventEditBox
EventEditBox:ApplyDefaultText(defaultText)
EventEditBox:ApplyDefaultTextColor(color)
EventEditBox:ApplyText(text)
EventEditBox:ApplyTextColor(color)
EventEditBox:CopyDeferredCallbacks(callbackType, event, target)
EventEditBox:ExpectedHasFocus() : unknown
EventEditBox:GenerateCallbackEvents(eventTable)
EventEditBox:GetCallbacksByEvent(callbackType, event) : event
EventEditBox:GetCallbackTable(callbackType) : unknown
EventEditBox:GetCallbackTables() : callbackTables
EventEditBox:GetCursorHeight() : cursorHeight
EventEditBox:GetCursorOffset() : cursorOffset
EventEditBox:GetFontHeight() : fontHeight
EventEditBox:GetInputText() : inputText
EventEditBox:GetMutableCallbacksByEvent(callbackType, event) : mutableCallbacksByEvent
EventEditBox:HasRegistrantsForEvent(event) : hasRegistrantsForEvent
EventEditBox:IsDefaultTextDisplayed() : isDefaultTextDisplayed
EventEditBox:IsDefaultTextEnabled() : isDefaultTextEnabled
EventEditBox:OnLoad()
EventEditBox:ReconcileDeferredCallbacks(event, closures, funcs)
EventEditBox:RegisterCallback(event, func, owner, ...) : owner
EventEditBox:RegisterCallbackWithHandle(event, func, owner, ...) : unknown
EventEditBox:SecureInsertEvent(event)
EventEditBox:SetDefaultTextEnabled(enabled)
EventEditBox:SetUndefinedEventsAllowed(allowed)
EventEditBox:ShouldDefault(text) : shouldDefault
EventEditBox:TriggerEvent(event, ...)
EventEditBox:TryApplyDefaultText()
EventEditBox:UnregisterCallback(event, owner)
EventEditBox:UnregisterEvents()
EventEditBox:UnregisterEventsByEventTable(eventTable)

EventFrame
EventFrame:CopyDeferredCallbacks(callbackType, event, target)
EventFrame:GenerateCallbackEvents(eventTable)
EventFrame:GetCallbacksByEvent(callbackType, event) : event
EventFrame:GetCallbackTable(callbackType) : unknown
EventFrame:GetCallbackTables() : callbackTables
EventFrame:GetMutableCallbacksByEvent(callbackType, event) : mutableCallbacksByEvent
EventFrame:HasRegistrantsForEvent(event) : hasRegistrantsForEvent
EventFrame:OnLoad()
EventFrame:ReconcileDeferredCallbacks(event, closures, funcs)
EventFrame:RegisterCallback(event, func, owner, ...) : owner
EventFrame:RegisterCallbackWithHandle(event, func, owner, ...) : unknown
EventFrame:SecureInsertEvent(event)
EventFrame:SetUndefinedEventsAllowed(allowed)
EventFrame:TriggerEvent(event, ...)
EventFrame:UnregisterCallback(event, owner)
EventFrame:UnregisterEvents()
EventFrame:UnregisterEventsByEventTable(eventTable)

EventScrollFrame
EventScrollFrame:CopyDeferredCallbacks(callbackType, event, target)
EventScrollFrame:GenerateCallbackEvents(eventTable)
EventScrollFrame:GetCallbacksByEvent(callbackType, event) : event
EventScrollFrame:GetCallbackTable(callbackType) : unknown
EventScrollFrame:GetCallbackTables() : callbackTables
EventScrollFrame:GetMutableCallbacksByEvent(callbackType, event) : mutableCallbacksByEvent
EventScrollFrame:HasRegistrantsForEvent(event) : hasRegistrantsForEvent
EventScrollFrame:OnLoad()
EventScrollFrame:ReconcileDeferredCallbacks(event, closures, funcs)
EventScrollFrame:RegisterCallback(event, func, owner, ...) : owner
EventScrollFrame:RegisterCallbackWithHandle(event, func, owner, ...) : unknown
EventScrollFrame:SecureInsertEvent(event)
EventScrollFrame:SetUndefinedEventsAllowed(allowed)
EventScrollFrame:TriggerEvent(event, ...)
EventScrollFrame:UnregisterCallback(event, owner)
EventScrollFrame:UnregisterEvents()
EventScrollFrame:UnregisterEventsByEventTable(eventTable)

ItemButton
ItemButton:GetBagID() : bagID
ItemButton:GetItem() : item
ItemButton:GetItemButtonBackgroundTexture() : itemButtonBackgroundTexture
ItemButton:GetItemButtonCount() : itemButtonCount
ItemButton:GetItemButtonIconTexture() : itemButtonIconTexture
ItemButton:GetItemContextOverlayMode() : unknown
ItemButton:GetItemID() : itemID
ItemButton:GetItemInfo() : itemLink, itemQuality, itemIcon
ItemButton:GetItemLink() : itemLink
ItemButton:GetItemLocation() : itemLocation
ItemButton:GetMatchesSearch() : matchesSearch
ItemButton:GetSlotAndBagID() : slotAndBagID, slotAndBagID
ItemButton:OnItemContextChanged()
ItemButton:OnUpdateItemContextMatching(bagID)
ItemButton:RegisterBagButtonUpdateItemContextMatching()
ItemButton:Reset()
ItemButton:SetAlpha(alpha)
ItemButton:SetBagID(bagID)
ItemButton:SetItem(item) : unknown
ItemButton:SetItemButtonAnchorPoint(point, x, y)
ItemButton:SetItemButtonBorderVertexColor(r, g, b)
ItemButton:SetItemButtonCount(count)
ItemButton:SetItemButtonQuality(quality, itemIDOrLink, suppressOverlays, isBound, ignoreColorOverrides)
ItemButton:SetItemButtonScale(scale)
ItemButton:SetItemButtonTexture(texture)
ItemButton:SetItemButtonTextureVertexColor(r, g, b)
ItemButton:SetItemInternal(item) : unknown
ItemButton:SetItemLocation(itemLocation) : unknown
ItemButton:SetItemSource(itemLocation)
ItemButton:SetMatchesSearch(matchesSearch)
ItemButton:UpdateCraftedProfessionsQualityShown()
ItemButton:UpdateItemContextMatching()
ItemButton:UpdateItemContextOverlay()
ItemButton:UpdateItemContextOverlayTextures(contextMode)

ScrollingMessageFrame
ScrollingMessageFrame:AcquireFontString() : fontString
ScrollingMessageFrame:AcquireHighlightTexture() : texture
ScrollingMessageFrame:AddMessage(message, r, g, b, ...)
ScrollingMessageFrame:AddOnDisplayRefreshedCallback(callback)
ScrollingMessageFrame:AdjustMessageColors(transformFunction)
ScrollingMessageFrame:AtBottom() : unknown
ScrollingMessageFrame:AtTop() : unknown
ScrollingMessageFrame:BackFillMessage(message, r, g, b, ...)
ScrollingMessageFrame:CalculateLineAlphaValueFromTimestamp(now, timestamp) : unknown
ScrollingMessageFrame:CalculateLineSpacing() : lineSpacing
ScrollingMessageFrame:CalculateNumVisibleLines() : unknown
ScrollingMessageFrame:CalculateSelectingCharacterIndicesForVisibleLine(lineIndex, startLineIndex, endLineIndex, startCharacterIndex, endCharacterIndex) : startCharacterIndex, unknown
ScrollingMessageFrame:CallOnDisplayRefreshed()
ScrollingMessageFrame:CanEffectivelyFade() : unknown
ScrollingMessageFrame:Clear()
ScrollingMessageFrame:FindCharacterAndLineIndexAtCoordinate(x, y) : characterIndex, lineIndex
ScrollingMessageFrame:ForEachMessage(op)
ScrollingMessageFrame:ForEachMessageInfoText(op)
ScrollingMessageFrame:ForEachVisibleLineText(op)
ScrollingMessageFrame:GatherSelectedText(x, y) : unknown
ScrollingMessageFrame:GetFadeDuration() : fadeDurationSecs
ScrollingMessageFrame:GetFading() : shouldFadeAfterInactivity
ScrollingMessageFrame:GetFont() : font
ScrollingMessageFrame:GetFontObject() : fontObject
ScrollingMessageFrame:GetIndentedWordWrap() : indentedWordWrap
ScrollingMessageFrame:GetInsertMode() : insertMode
ScrollingMessageFrame:GetJustifyH() : justifyH
ScrollingMessageFrame:GetJustifyV() : justifyV
ScrollingMessageFrame:GetMaxLines() : maxLines
ScrollingMessageFrame:GetMaxScrollRange() : maxScrollRange
ScrollingMessageFrame:GetMessageInfo(messageIndex) : messageInfo
ScrollingMessageFrame:GetNumMessages() : numMessages
ScrollingMessageFrame:GetNumVisibleLines() : numVisibleLines
ScrollingMessageFrame:GetOnLineRightClickedCallback() : onLineRightClickedCallback
ScrollingMessageFrame:GetOnScrollChangedCallback() : onScrollChangedCallback
ScrollingMessageFrame:GetOnTextCopiedCallback() : onTextCopiedCallback
ScrollingMessageFrame:GetPagingScrollAmount() : pagingScrollAmount
ScrollingMessageFrame:GetScaledCursorPosition() : scaledCursorPosition, scaledCursorPosition
ScrollingMessageFrame:GetScrollOffset() : scrollOffset
ScrollingMessageFrame:GetShadowColor() : shadowColor
ScrollingMessageFrame:GetShadowOffset() : shadowOffset
ScrollingMessageFrame:GetSpacing() : spacing
ScrollingMessageFrame:GetTextColor() : textColor
ScrollingMessageFrame:GetTimeVisible() : timeVisibleSecs
ScrollingMessageFrame:HasFontObject() : hasFontObject
ScrollingMessageFrame:InitializeFontableFrame(name)
ScrollingMessageFrame:InitializeFontString(fontString)
ScrollingMessageFrame:IsScrollAllowed() : isScrollAllowed
ScrollingMessageFrame:IsSelectingText() : isSelectingText
ScrollingMessageFrame:IsTextCopyable() : textIsCopyable
ScrollingMessageFrame:MakeFontObjectCustom()
ScrollingMessageFrame:MarkDisplayDirty()
ScrollingMessageFrame:MarkLayoutDirty()
ScrollingMessageFrame:OnColorsUpdated()
ScrollingMessageFrame:OnFontObjectUpdated()
ScrollingMessageFrame:PackageEntry(message, r, g, b, ...) : unknown
ScrollingMessageFrame:PageDown()
ScrollingMessageFrame:PageUp()
ScrollingMessageFrame:RefreshDisplay()
ScrollingMessageFrame:RefreshIfNecessary()
ScrollingMessageFrame:RefreshLayout()
ScrollingMessageFrame:RemoveMessagesByPredicate(predicate) : unknown
ScrollingMessageFrame:ResetAllFadeTimes()
ScrollingMessageFrame:ResetSelectingText()
ScrollingMessageFrame:ScrollByAmount(amount)
ScrollingMessageFrame:ScrollDown()
ScrollingMessageFrame:ScrollToBottom()
ScrollingMessageFrame:ScrollToTop()
ScrollingMessageFrame:ScrollUp()
ScrollingMessageFrame:SetFadeDuration(fadeDurationSecs)
ScrollingMessageFrame:SetFading(shouldFadeAfterInactivity)
ScrollingMessageFrame:SetFont(font, fontHeight, fontFlags)
ScrollingMessageFrame:SetFontObject(fontObject)
ScrollingMessageFrame:SetIndentedWordWrap(indentWordWrap)
ScrollingMessageFrame:SetInsertMode(insertMode)
ScrollingMessageFrame:SetJustifyH(justifyH)
ScrollingMessageFrame:SetJustifyV(justifyV)
ScrollingMessageFrame:SetMaxLines(maxLines)
ScrollingMessageFrame:SetOnLineRightClickedCallback(onLineRightClickedCallback)
ScrollingMessageFrame:SetOnScrollChangedCallback(onScrollChangedCallback)
ScrollingMessageFrame:SetOnTextCopiedCallback(onTextCopiedCallback)
ScrollingMessageFrame:SetScrollAllowed(allowed)
ScrollingMessageFrame:SetScrollOffset(offset)
ScrollingMessageFrame:SetShadowColor(r, g, b, a)
ScrollingMessageFrame:SetShadowOffset(offsetX, offsetY)
ScrollingMessageFrame:SetSpacing(spacing)
ScrollingMessageFrame:SetTextColor(r, g, b, a)
ScrollingMessageFrame:SetTextCopyable(textIsCopyable)
ScrollingMessageFrame:SetTimeVisible(timeVisibleSecs)
ScrollingMessageFrame:TransformMessages(predicate, transformFunction) : unknown
ScrollingMessageFrame:UnpackageEntry(entry) : message, r, g, b, unknown
ScrollingMessageFrame:UpdateFading()
ScrollingMessageFrame:UpdateSelectingText()

UIThemeContainerFrame
UIThemeContainerFrame:CheckUpdateTheme(cvar, value)
UIThemeContainerFrame:GetCVarValue() : cVarValue
UIThemeContainerFrame:IsDarkMode(cvarValue) : isDarkMode
UIThemeContainerFrame:RegisterBackgroundTexture(texture, textureKit)
UIThemeContainerFrame:RegisterFontString(fontString)
UIThemeContainerFrame:RegisterFontStrings(...)
UIThemeContainerFrame:RegisterFrame(frame)
UIThemeContainerFrame:RegisterFrames(...)
UIThemeContainerFrame:RegisterObject(container, object)
UIThemeContainerFrame:RegisterObjects(container, ...)
UIThemeContainerFrame:UpdateBackground(cvarValue)
UIThemeContainerFrame:UpdateFontStrings(cvarValue)
UIThemeContainerFrame:UpdateFrames(cvarValue)
UIThemeContainerFrame:UpdateTheme(cvarValue)

---


---

Scripts

AnimationGroup
OnFinished(self, requested) - Invoked when the animation group finishes animating.
OnLoop(self, loopState) - Invoked when the animation group's loop state changes.
OnPause(self) - Invoked when the animation group is paused.
OnPlay(self) - Invoked when the animation group begins to play.
OnStop(self, requested) - Invoked when the animation group is stopped.
OnUpdate(self, elapsed) - Invoked on every frame.
OnLoad(self) - Invoked when the object is created.

Animation
OnFinished(self, requested) - Invoked when the animation finishes animating.
OnPause(self) - Invoked when the animation is paused.
OnPlay(self) - Invoked when the animation begins to play.
OnStop(self, requested) - Invoked when the animation is stopped.
OnUpdate(self, elapsed) - Invoked on every frame.
OnLoad(self) - Invoked when the object is created.

ScriptRegion
OnShow(self) - Invoked when the widget is shown.
OnHide(self) - Invoked when the widget is hidden.
OnEnter(self, motion) - Invoked when the cursor enters the widget's interactive area.
OnLeave(self, motion) - Invoked when the mouse cursor leaves the widget's interactive area.
OnMouseDown(self, button) - Invoked when a mouse button is pressed while the cursor is over the widget.
OnMouseUp(self, button, upInside) - Invoked when the mouse button is released following a mouse down action in the widget.
OnMouseWheel(self, delta) - Invoked when the widget receives a mouse wheel scrolling action.
OnLoad(self) - Invoked when the widget is created.
Frame
OnAttributeChanged(self, key, value) - Invoked when a secure frame attribute is changed.
OnChar(self, text) - Invoked for each text character typed in the frame.
OnDisable(self) - Invoked when the frame is disabled.
OnDragStart(self, button) - Invoked when the mouse is dragged starting in the frame
OnDragStop(self) - Invoked when the mouse button is released after a drag started in the frame,
OnEnable(self) - Invoked when the frame is enabled.
OnEvent(self, event, ...) - Invoked whenever an event fires for which the frame is registered.
OnGamePadButtonDown(self, button) - Invoked when a gamepad button is pressed.
OnGamePadButtonUp(self, button) - Invoked when a gamepad button is released.
OnGamePadStick(self, stick, x, y, len) - Invoked when a gamepad stick is moved.
OnHyperlinkClick(self, link, text, button, region, left, bottom, width, height) - Invoked when the mouse clicks a hyperlink on the FontInstance object.
OnHyperlinkEnter(self, link, text, region, left, bottom, width, height) - Invoked when the mouse moves over a hyperlink on the FontInstance object.
OnHyperlinkLeave(self) - Invoked when the mouse moves away from a hyperlink on the FontInstance object.
OnKeyDown(self, key) - Invoked when a keyboard key is pressed if the frame is keyboard enabled.
OnKeyUp(self, key) - Invoked when a keyboard key is released if the frame is keyboard enabled.
OnReceiveDrag(self) - Invoked when the mouse button is released after dragging into the frame.
OnSizeChanged(self, width, height) - Invoked when a frame's size changes.
OnUpdate(self, elapsed) - Invoked on every frame.

Button
OnClick(self, self, button, down) - Invoked when clicking a button.
OnDoubleClick(self, self, button) - Invoked when double-clicking a button.
PostClick(self, button, down) - Invoked immediately after `OnClick`.
PreClick(self, button, down) - Invoked immediately before `OnClick`.

Model
OnAnimFinished(self) - Invoked when the model's animation finishes.
OnAnimStarted(self) - Invoked when the model's animation starts.
OnModelLoaded(self) - Invoked when the model is loaded.

CinematicModel
OnPanFinished(self) - Invoked when the camera has finished panning.

DressUpModel
OnDressModel(self, itemModifiedAppearanceID, invSlot, removed) - Invoked when the dressup model is updated.

ModelScene
OnDressModel(self, itemModifiedAppearanceID, invSlot, removed) - Invoked when the modelscene model is updated.

ModelSceneActor
Scripts for this widget can only be set from XML.
OnAnimFinished(self)
OnModelCleared(self)
OnModelLoaded(self)
OnModelLoading(self)

EditBox
OnArrowPressed(self, key)
OnCharComposition(self, text) - Invoked for each text character typed in the frame while using an input method editor (IME).
OnCursorChanged(self, x, y, w, h) - Invoked when moving the text insertion cursor.
OnEditFocusGained(self) - Invoked when gaining edit focus.
OnEditFocusLost(self) - Invoked when losing edit focus.
OnEnterPressed(self) - Invoked when pressing Enter while the widget has focus.
OnEscapePressed(self) - Invoked when pressing Escape while the widget has focus.
OnSpacePressed(self) - Invoked when pressing Space while the widget has focus.
OnInputLanguageChanged(self, language) - Invoked when changing the language input mode.
OnTabPressed(self) - Invoked when pressing Tab while the widget has focus.
OnTextChanged(self, userInput) - Invoked when changing the value.
OnTextSet(self) - Invoked when setting the value programmatically.

GameTooltip
OnTooltipCleared(self) - Run when the tooltip is hidden or its content is cleared.
OnTooltipSetDefaultAnchor(self) - Run when the tooltip is repositioned to its default anchor location.
OnTooltipSetFramestack(self, highlightFrame) - Run when the tooltip is filled with a list of frames under the mouse cursor.

---
