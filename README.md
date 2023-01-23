SCRIPT BELOW
--------------

if game.placeid == 893973440 then

--Load
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

--Main
local Window = OrionLib:MakeWindow({Name = "DG HUB", HidePremium = false, SaveConfig = true, ConfigFolder = "DgCfg", IntroEnabled = false})


--Valor
_G.CrawlSpeed = true

--funcao
function CrawlSpeed()
        while _G.CrawlSpeed == true do
             local functionInfo = {
    ["upvalues"] = {
        [1] = game:GetService("UserInputService"),
        [2] = {
            ["CreateStat"] = function() CreateStat end,
            ["GetValue"] = function() GetValue end,
            ["SetValue"] = function() SetValue end,
            ["ResetValues"] = function() ResetValues end,
            ["Get"] = function() Get end
        },
        [3] = game:GetService("ReplicatedStorage").RemoteEvent,
        [4] = game:GetService("Players").LocalPlayer.Character.Humanoid,
        [5] = getNil("AnimCrawl", "AnimationTrack")
    },
    ["info"] = {
        ["source"] = "=Workspace.Mcdodo29.LocalPlayerScript",
        ["what"] = "Lua",
        ["numparams"] = 3,
        ["func"] = function() CrawlFunction end,
        ["short_src"] = "Workspace.Mcdodo29.LocalPlayerScript",
        ["name"] = "CrawlFunction",
        ["currentline"] = 36,
        ["namewhat"] = "function",
        ["is_vararg"] = 0,
        ["nups"] = 5
    },
    ["constants"] = {
        [1] = "TouchEnabled",
        [2] = "Enum",
        [3] = "UserInputState",
        [4] = "Begin",
        [5] = Enum.UserInputState.Begin,
        [6] = "GetValue",
        [7] = "IsCrawling",
        [8] = "Input",
        [9] = "Crawl",
        [10] = "FireServer",
        [11] = "HipHeight",
        [12] = "Stop",
        [13] = "WalkSpeed",
        [14] = 1.100000001,
        [15] = "Play",
        [16] = "End",
        [17] = Enum.UserInputState.End
    }
}
        end
end

--Jogador
local FastVentTab = Window:MakeTab({
	Name = "FastVent",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})
local Section = FastVentTab:AddSection({
 	Name = "FastCrawl-configurado"
})
FastVentTab:AddToggle({
 	Name = "Velocidade-Crawl",
 	Default = false,
 	Callback = function(Value)
 		   _G.CrawlSpeed = value 
             CrawlSpeed() 	
     end 
})


end
