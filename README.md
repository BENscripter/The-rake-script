local Luxtl = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Luxware-UI-Library/main/Source.lua"))() 
  
local Luxt = Luxtl.CreateWindow("Fluxus Rake", 6105620301)    

local Examples = Luxt:Tab("The Rake") 
local ff = Examples:Section("Make u See Rake But Not Item") 
ff:Label("Esp")
ff:Button("Press", function()
getgenv().esp = false
local highlights = {}
 
function start()
    while task.wait() do
        local esp = getgenv().esp
        local rake = game.Workspace:FindFirstChild("Rake")
        local rakeHighlight = game.CoreGui:FindFirstChild("Rake")
 
        if esp and rake then
            if not rakeHighlight then
                local highlight = Instance.new("Highlight", game.CoreGui)
                highlight.Name = "Rake"
                highlight.Adornee = rake
                highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
                highlight.FillColor = Color3.fromRGB(193, 30, 0)
                highlights[rake] = highlight
            end
        else
            if rakeHighlight then
                rakeHighlight:Destroy()
                highlights[rake] = nil
            end
        end
    end
end

ff:Label("TpWalk")
ff:Button("Press", function()
getgenv().WalkSpeed = true 
 
while WalkSpeed == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame + game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.lookVector * 3.5
wait()
end

ff:Label("Resets [KICKS U]")
ff:Button("Press", function()
game.Players.LocalPlayer:Kick("
你因作弊而被封禁，请在discord举报，看看是否有错误[FAKE]")
