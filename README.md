-- GUI Setup
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local ESPButton = Instance.new("TextButton")
local AutoFarmButton = Instance.new("TextButton")
local TeleportButton = Instance.new("TextButton")
local AutoSpinButton = Instance.new("TextButton")

ScreenGui.Parent = game.CoreGui
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.new(0.1, 0.1, 0.1)
Frame.Position = UDim2.new(0.5, -100, 0.5, -100)
Frame.Size = UDim2.new(0, 200, 0, 250)

Title.Parent = Frame
Title.Text = "THOMAS TURBANO HUB"
Title.Position = UDim2.new(0.1, 0, 0, 0)
Title.Size = UDim2.new(0.8, 0, 0.2, 0)
Title.TextColor3 = Color3.new(1, 1, 1)
Title.BackgroundTransparency = 1

ESPButton.Parent = Frame
ESPButton.Text = "ESP Fruit"
ESPButton.Position = UDim2.new(0.1, 0, 0.2, 0)
ESPButton.Size = UDim2.new(0.8, 0, 0.15, 0)

AutoFarmButton.Parent = Frame
AutoFarmButton.Text = "Auto Farm Level"
AutoFarmButton.Position = UDim2.new(0.1, 0, 0.4, 0)
AutoFarmButton.Size = UDim2.new(0.8, 0, 0.15, 0)

TeleportButton.Parent = Frame
TeleportButton.Text = "Teleport"
TeleportButton.Position = UDim2.new(0.1, 0, 0.6, 0)
TeleportButton.Size = UDim2.new(0.8, 0, 0.15, 0)

AutoSpinButton.Parent = Frame
AutoSpinButton.Text = "Auto Spin Fruit"
AutoSpinButton.Position = UDim2.new(0.1, 0, 0.8, 0)
AutoSpinButton.Size = UDim2.new(0.8, 0, 0.15, 0)

-- ESP Function
local function ESPFruit()
    for _, fruit in pairs(game.Workspace.Fruits:GetChildren()) do
        local BillboardGui = Instance.new("BillboardGui", fruit)
        BillboardGui.Size = UDim2.new(0, 100, 0, 100)
        BillboardGui.AlwaysOnTop = true
        local TextLabel = Instance.new("TextLabel", BillboardGui)
        TextLabel.Text = fruit.Name
        TextLabel.Size = UDim2.new(1, 0, 1, 0)
        TextLabel.TextColor3 = Color3.new(1, 0, 0)
    end
end

-- Auto Farm Function
local function AutoFarmLevel()
    while true do
        wait(1)
        -- Código de auto farm aqui
    end
end

-- Teleport Function
local function Teleport()
    local player = game.Players.LocalPlayer
    player.Character.HumanoidRootPart.CFrame = CFrame.new(0, 100, 0) -- Coordenadas de teleporte
end

-- Auto Spin Function
local function AutoSpinFruit()
    while true do
        wait(1)
        -- Código de auto spin aqui
    end
end

-- Button Click Events
ESPButton.MouseButton1Click:Connect(ESPFruit)
AutoFarmButton.MouseButton1Click:Connect(AutoFarmLevel)
TeleportButton.MouseButton1Click:Connect(Teleport)
AutoSpinButton.MouseButton1Click:Connect(AutoSpinFruit)
