noclip = false
plr = game.Players.LocalPlayer

game:GetService('RunService').Stepped:connect(function()
  if noclip then
	plr.Character.Humanoid:ChangeState(11)
  end
end)
local gui = Instance.new("ScreenGui")
gui.Name = 'Hack'
gui.Parent = game.CoreGui

local frame = Instance.new("Frame")
frame.Name = 'HackFrame'
frame.AnchorPoint = Vector2.new(0.5, 0.5)
frame.Parent = gui
frame.Draggable = true
frame.Active = true
frame.Selectable = true
frame.BackgroundColor3 = Color3.new(0, 1, 1)
frame.BorderSizePixel = 0
frame.Position = UDim2.new(0.5, 0,0.499, 0)
frame.Size = UDim2.new(0, 304,0, 276)

local TOP = Instance.new("Frame")
TOP.Name = 'TOP'
TOP.Parent = frame
TOP.BackgroundColor3 = Color3.new(0, 0.901961, 1)
TOP.BorderSizePixel = 0
TOP.Position = UDim2.new(0, 0,0, 0)
TOP.Size = UDim2.new(0, 304,0, 52)

local topTitle = Instance.new("TextLabel")
topTitle.Name = 'Title'
topTitle.Text = 'ElCacarucho HACK'
topTitle.Parent = TOP
topTitle.BorderSizePixel = 0
topTitle.BackgroundTransparency = 1
topTitle.Font = Enum.Font.Fantasy
topTitle.TextScaled = true
topTitle.Position = UDim2.new(0.171, 0,0.096, 0)
topTitle.Size = UDim2.new(0, 200,0, 42)

local noclipButton = Instance.new("TextButton")
noclipButton.Name = 'Title'
noclipButton.Text = 'NOCLIP'
noclipButton.Parent = frame
noclipButton.BorderColor3 = Color3.new(0, 0, 0)
noclipButton.BorderSizePixel = 2
noclipButton.Font = Enum.Font.Fantasy
noclipButton.TextScaled = true
noclipButton.Position = UDim2.new(0.171, 0,0.272, 0)
noclipButton.Size = UDim2.new(0, 200,0, 29)

noclipButton.MouseButton1Click:Connect(function()
noclip = not noclip
game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
end)
