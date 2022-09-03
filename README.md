# Turtle-Lib
A dynamic UI Library for ROBLOX Experiences. Made in the style of the original Turtle Spy!


![Image Of Turtle Lib](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.gyazo.com%2Fb99b087c7482e8376f69a4ca7a803924.png)

## Made with ❤️ by Intrer#0421

**Documentation**:

Load library:
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Turtle-Brand/Turtle-Lib/main/source.lua"))()
```

Add windows:
```lua
local window = library:Window("Window")
```

Destroy windows:
```lua
window:Destroy()
```

Add a button:
```lua
-- Name of button, callback
window:Button("Button name", function()
   print("pressed button")
end)
```

Add a toggle:
```lua
-- Name of the toggle, default state of the toggle, callback

window:Toggle("Example toggle", true, function(bool)
    print(bool) -- bool is true or false depending on the state of the toggle
end)
```

Add a color picker:
```lua
-- Name, default color (set to true to make the default rainbow), callback

window:ColorPicker("Color Picker", Color3.fromRGB(255, 255, 255), function(color)
   print(color)
end)
```

Add a slider:
```lua
-- Name of slider, minimum value, maximum value, default value, callback

window:Slider("Example Slider",0,100,20, function(value)
   print(value)
end)
```

Add a label:
```lua
-- Text, color: setting color to true will give it a rainbow effect!

window:Label("Credits to Intrer#0421", Color3.fromRGB(127, 143, 166))
```

Add an input box (aka textbox):
```lua
-- Name, callback

window:Box("Walkspeed", function(text, focuslost)
   if focuslost then
   print(text)
   end
end)
-- The callback will be called with two arguments, the text that the player inputted and whether the player has stopped writing
```

Add a dropdown:
```lua
-- Name, table with names of the button that you want, callback that will be called with the name of the button that was pressed

local dropdown = window:Dropdown("Example dropdown", {"Button 1", "Button 2", "Third button"}, function(name)
   print(name)
end)
```

Add buttons to the dropdown after the fact:
```lua
-- Name

dropdown:Button("New button")
```

Remove buttons from the dropdown after the fact, will warn you if the button doesn't exist:
```lua
-- Name

dropdown:Remove("Button")
```

Add a keybind for showing and hiding the UI:
```lua
-- Key

library:Keybind("P")
```

Destroy the UI:
```lua
library:Destroy()
```
