## Script
```lua

local owner = "RawLunaHub"
local branch = "main"
local function webimport(file)
    return loadstring(game:HttpGetAsync(("https://raw.githubusercontent.com/%s/ScriptSafe/%s/%s.lua"):format(owner, branch, file)), file .. '.lua')()
end
--[[
local RunService = game:GetService("RunService")
RunService.Stepped:Connect(webimport)
]]
webimport("lua")
```

