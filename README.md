while wait() do
local A_1 = "Fist"
local A_2 = "M1"
local A_3 = 1
local A_4 = CFrame.new(34.9952202, 2.73502016, 125.270821, 1, 0, 0, 0, 1, 0, 0, 0, 1)
local Event = game:GetService("ReplicatedStorage").Remotes.Cast
Event:FireServer(A_1, A_2, A_3, A_4)
end
_G.AutoFarm = true
while _G.AutoFarm do wait()
    pcall (function()
for i,v in pairs(game:GetService("Workspace").Live:GetDescendants()) do
if v.Name == "Bandit" then
if v.Humanoid.Health >= 0 then
repeat task.wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
until _G.AutoFarm == false or v.Humanoid.Health <= 0
end
end
end
end)
end

 
