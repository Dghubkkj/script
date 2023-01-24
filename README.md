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
             local Events = game:GetService("Players").LocalPlayer.Character.LocalPlayerScript
             Event:InvokeServer()
             wait(0.1000000001)
             
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
