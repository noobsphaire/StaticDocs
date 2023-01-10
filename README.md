# StaticDocs

# Loading The Library
```lua
print("Private")
```

## Creating Window
```lua
local Window = Library:Create({ 
     Name = "Example Window", 
     ToggleKey = Enum.KeyCode.RightShift, 
     KeySystem = false, 
     Key = "123456", 
     DiscordLink = nil, 
     KeyLink = nil, 
 }) 
```

## Creating Tabs
```lua
 local Tab = Window:Tab({ 
         Name = "Example Tab" 
 }) 
```

## Creating Sections
```lua
 Tab:Section({ 
         Name = "Example Section" 
 }) 
```
## Creating Labels
```lua
 Tab:Label({ 
         Name = "Example Label" 
 }) 
```

## Creating Buttons
```lua
 Tab:Button({ 
         Name = "Example Button", 
         Callback = function()
         Window:Notification({ 
                         Name = "Button", 
                         Description = "Clicked", 
                 }) 
         end, 
 }) 
```

## Creating Toggles
```lua
 Tab:Toggle({ 
         Name = "Example Toggle", 
         Callback = function(Bool) 
                 Window:Notification({ 
                         Name = "Toggle", 
                         Description = Bool, 
                 }) 
         end, 
         Default = false 
 }) 
```

## Creating Sliders
```lua
 Tab:Slider({ 
         Name = "Example Slider", 
         Callback = function()
         end, 
         Default = 0,
         Max = 500,
        Min = 0,
 })
```

## Creating Textboxes
```lua
 Tab:Textbox({ 
         Name = "Example Textbox", 
         Callback = function(Val) 
                 Window:Notification({ 
                         Name = "Textbox", 
                         Description = Val, 
                 }) 
         end, 
 })
```

## Creating Keybinds
```lua
 Tab:Keybind({ 
         Name = "Keybind", 
         Default = Enum.KeyCode.LeftAlt, 
         Callback = function() 
                 Window:Notification({ 
                         Name = "Keybind", 
                         Description = "Clicked", 
                 }) 
         end, 
 }) 
```

## Creating Dropdowns
```lua
 local dropdown = Tab:Dropdown({ 
         Name = "Example Dropdown", 
         Items = {1, "XD",2}, 
         Default = 1, 
         Callback = function(item) 
                 Window:Notification({ 
                         Name = "Dropdown", 
                         Description = item, 
                 }) 
         end 
 }) 
```

## Creating Suggestions (With A button)
```lua
Tab:Button({ 
         Name = "e", 
         Callback = function() 
                 Window:Suggestion({ 
                         Name = "Example Suggestion", 
                         Description = "This is NOT a suggestion!", 
                         Option1 = "e1", 
                         Option2 = "e2", 
                         Callback = function(val) 
                                 Window:Notification({ 
                                         Name = "Suggestion",
                                         Description = "Suggestion"..tostring(val), 
                                 }) 
                         end 
                 }) 
         end, 
 })
```
