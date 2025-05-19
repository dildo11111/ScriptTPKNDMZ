local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Teleport by Darkll3ss KNDMZ", "DarkTheme")
local Tab = Window:NewTab("Уебаны")
local Section = Tab:NewSection("Телепорт")

--------------------дилдо
players = {}

for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end

Section:NewDropdown("Кто отсосёт?", " ", players, function(abc)
    Select = abc
end)


Section:NewButton("Рефреш", " ", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
   table.insert(players,v.Name)
end
end)

Section:NewButton("Тэпэхнуца", " ", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame
end)
