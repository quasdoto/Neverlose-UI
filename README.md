# Neverlose-UI for roblox exploit scripts

#### Loadstring
This loadstring retrieves the UI library from the GitHub repository:
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/quasdoto/Neverlose-UI/refs/heads/main/uisource.lua"))()
```

#### Creating Window
This function initializes the main window of the UI:
```lua
local Window = Library:Window({
    text = "Window"
})
```
Default text - Neverlose

#### Creating Tab Sections
A tab section is created to organize tabs within the UI:
```lua
local TabSection = Window:TabSection({
    text = "TabSection"
})

local Tab = TabSection:Tab({
    text = "Tab",
    icon = "rbxassetid://7999345313",
})
```

#### Creating Section
```lua
local Section = Tab:Section({
    text = "Section"
})
```

### Elements

#### Creating Button
```lua
Section:Button({
    text = "Button",
    callback = function()
        print("Clicked button")
    end,
})
```

#### Creating Toggle
```lua
Section:Toggle({
    text = "Toggle",
    state = false, -- Default boolean
    callback = function(boolean)
        print("Toggle current: ",boolean)
    end
})
```

#### Creating Slider
```lua
Section:Slider({
    text = "Slider",
    min = 10,
    max = 100,
    -- [[Float = 0,]] Idk what it does
    callback = function(number)
        print(number)
    end
})

```

#### Creating Dropdown
```lua
Section:Dropdown({
    text = "Dropdown",
    list = {"Apple", "Banana","Coconut"},
    default = "Apple",
    callback = function(String)
        print(String)
    end
})
```

#### Creating TextBox
```lua
Section:Textbox({
    text = "Textbox",
    value = "Default",
    callback = function(String)
        print(String)
    end
})
```

#### Creating Colorpicker
```lua
Section:Colorpicker({
    text = "Colorpicker",
    color = Color3.new(1,1,1),
    callback = function(HSV)
        print(HSV)
    end
})
```

#### Creating Keybind
```lua
Section:Keybind({
    text = "Keybind",
    default = Enum.KeyCode.Z,
    callback = function(defaultBind)
        print("Triggered keybind")
        print(defaultBind)
    end
})
```
