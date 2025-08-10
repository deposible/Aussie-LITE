# WIRE Library

The WIRE library is every function that aussie wire has custom created to prevent issues!

## WIRE.loop(delay, function)
```lua
<function> WIRE.loop(type: Int, type: function)
```
```lua
-- Example

WIRE.loop(1, function() -- Will run every 1 second
  print('Running')
end)
```

## WIRE.find(String, Table or String)
```lua
<function> WIRE.find(type: string, type: string OR Table)
```
```lua
-- Example #1
local results = WIRE.find("Text", "Text")

if results then
 print('Successfully found matching text')
end
```
```lua
-- Example #2
local results = WIRE.find("Text", {"array", "table", "issue", "master ghost", "Tissue", text"}) -- Will auto lower case everything so then you dont have to worry about it being the exact same it just looks for exact text

if results then
  print('Found a matching text')
end
```

## WIRE.firetouchinterest(Instance1, Instance2)
```lua
<function> WIRE.firetouchinterest(type: Instance, type: Instance) -- Will auto toggle to simulate a touch/untouched event
```
```lua
-- Example

WIRE.firetouchinterest(game.Players.LocalPlayer.HumanoidRootPart, workspace:FindFirstChildWhichIsA("BasePart"))
```

## WIRE.esp(name, parent, color, type, keeping)
```lua
--[[
Type 1: Highlights
Type 2: Textbox w the ESP Name as the text
]]

<function> WIRE.esp(type: string, type: Instance, type: Color3.fromRGB, type: Int --[[This is where the type is]], type: boolean --[[Weather you want to keep it or not]]) 
```
```lua
-- Example 1 (Creating & Destroying) [ Highlights Version ]
local LocalPlayer = game.Players.LocalPlayer

WIRE.esp("ESP Name", LocalPlayer.Character, {255, 255, 255}, 1, true) --[[Creating]] -- the 1 represents the type of ESP
task.wait(5)
WIRE.esp("ESP Name", LocalPlayer.Character, {255, 255, 255}, 1, false) --[[Destroying]] (Just change the true and false)
```
```lua
-- Example 2 (Creating & Destroying) [ Textbox Version ]

local LocalPlayer = game.Players.LocalPlayer

WIRE.esp("ESP Name", LocalPlayer.Character, {255, 255, 255}, 2, true) --[[Creating]] -- the 2 represents the type of ESP
task.wait(5)
WIRE.esp("ESP Name", LocalPlayer.Character, {255, 255, 255}, 2, false) --[[Destroying]] (Just change the true and false)
```

## WIRE.Tween(delay, position)
```lua
<function> WIRE.Tween(type: Int, type: Vector3)
```
```lua
-- Example
WIRE.Tween(5, Vector3.new(0, 0, 0)) -- Take 5 seconds to tween to vector3s position
```

## WIRE.CreatePart(name, shape, transparency, material, parent, CanCollide)
```lua
<function> WIRE.CreatePart(type: string, type: string, type: Int, type: string, type: boolean)
```
```lua
-- Example
local NewPart = WIRE.CreatePart("Name", "Block" or false, 0, "Plastic" or false, workspace, true)

while task.wait(0.1) do
  NewPart.Size = Vector3.new(10, 10, 10)
  NewPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0, -5, 0)
end
```

## WIRE.Click(table OR <void>)
```lua
<function> WIRE.Click(type: Int OR <void>)
```
```lua
-- Example 1
WIRE.Click()
```
```lua
-- Example 2
WIRE.Click({version = 0, delay = 0}) -- Version represents either through clicking your screen manually or sending data to roblox saying you clicked it
```
```lua
-- Example 3
WIRE.Click({version = 1, delay = 0}) -- Only 2 Versions 0 & 1
```
