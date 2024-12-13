--[[ 
Stand Power Script (English Version)
Note: Created for educational purposes only. Do not use for unethical practices.
]]

local UserInterface = {}
local FarmSettings = {AttackSpeed = 1, Distance = 10, AttackType = "Punch"} -- Default Attack Type is "Punch"
local TPSettings = {BossDistance = 20}

-- Function to create the user interface
function UserInterface:CreateMenu()
    -- Main screen
    local ScreenGui = Instance.new("ScreenGui")
    ScreenGui.Name = "StandPowerScript"
    ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

    -- Main window
    local MainFrame = Instance.new("Frame")
    MainFrame.Size = UDim2.new(0, 300, 0, 500)
    MainFrame.Position = UDim2.new(0.5, -150, 0.5, -250)
    MainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
    MainFrame.Parent = ScreenGui

    -- Close button
    local CloseButton = Instance.new("TextButton")
    CloseButton.Text = "X"
    CloseButton.Size = UDim2.new(0, 25, 0, 25)
    CloseButton.Position = UDim2.new(1, -30, 0, 5)
    CloseButton.Parent = MainFrame
    CloseButton.MouseButton1Click:Connect(function()
        ScreenGui:Destroy() -- Close the menu
    end)

    -- Add menu buttons
    self:CreateMenuButtons(MainFrame)
end

function UserInterface:CreateMenuButtons(MainFrame)
    -- Farm button
    local FarmButton = Instance.new("TextButton")
    FarmButton.Text = "Farm"
    FarmButton.Size = UDim2.new(1, -10, 0, 50)
    FarmButton.Position = UDim2.new(0, 5, 0, 50)
    FarmButton.Parent = MainFrame
    FarmButton.MouseButton1Click:Connect(function()
        self:ActivateFarm()
    end)

    -- Teleport button
    local TPButton = Instance.new("TextButton")
    TPButton.Text = "Teleport"
    TPButton.Size = UDim2.new(1, -10, 0, 50)
    TPButton.Position = UDim2.new(0, 5, 0, 110)
    TPButton.Parent = MainFrame
    TPButton.MouseButton1Click:Connect(function()
        self:ActivateTeleport()
    end)

    -- Buy button
    local BuyButton = Instance.new("TextButton")
    BuyButton.Text = "Buy"
    BuyButton.Size = UDim2.new(1, -10, 0, 50)
    BuyButton.Position = UDim2.new(0, 5, 0, 170)
    BuyButton.Parent = MainFrame
    BuyButton.MouseButton1Click:Connect(function()
        self:ActivateBuy()
    end)

    -- Attack Type Selector
    local AttackLabel = Instance.new("TextLabel")
    AttackLabel.Text = "Attack Type:"
    AttackLabel.Size = UDim2.new(1, -10, 0, 25)
    AttackLabel.Position = UDim2.new(0, 5, 0, 240)
    AttackLabel.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
    AttackLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    AttackLabel.Parent = MainFrame

    local AttackDropdown = Instance.new("TextButton")
    AttackDropdown.Text = "Punch"
    AttackDropdown.Size = UDim2.new(1, -10, 0, 50)
    AttackDropdown.Position = UDim2.new(0, 5, 0, 270)
    AttackDropdown.Parent = MainFrame
    AttackDropdown.MouseButton1Click:Connect(function()
        if FarmSettings.AttackType == "Punch" then
            FarmSettings.AttackType = "Stand"
            AttackDropdown.Text = "Stand"
        elseif FarmSettings.AttackType == "Stand" then
            FarmSettings.AttackType = "Style"
            AttackDropdown.Text = "Fighting Style"
        else
            FarmSettings.AttackType = "Punch"
            AttackDropdown.Text = "Punch"
        end
    end)
end

function UserInterface:ActivateFarm()
    print("Farm activated!")
    -- Example: Farm logic based on Attack Type
    local Player = game.Players.LocalPlayer
    local Bosses = {"Funny Valentine"}
    
    for _, bossName in pairs(Bosses) do
        local boss = game.Workspace:FindFirstChild(bossName)
        if boss then
            Player.Character:MoveTo(boss.Position + Vector3.new(0, TPSettings.BossDistance, 0))
            self:Attack(boss)
        end
    end
end

function UserInterface:Attack(target)
    if FarmSettings.AttackType == "Punch" then
        print("Attacking with Punch!")
        -- Logic for punch attack
    elseif FarmSettings.AttackType == "Stand" then
        print("Attacking with Stand!")
        -- Logic for stand attack
    elseif FarmSettings.AttackType == "Style" then
        print("Attacking with current Fighting Style!")
        -- Logic for fighting style (Boxing, Hamon, Spin)
    end
end

function UserInterface:ActivateTeleport()
    print("Teleport activated!")
    -- Example: Teleport to NPCs
    local NPCs = {"Mr. Monster", "Ippo", "The Pro Boxer", "Jonathan Joestar"}
    for _, npcName in pairs(NPCs) do
        local npc = game.Workspace:FindFirstChild(npcName)
        if npc then
            game.Players.LocalPlayer.Character:MoveTo(npc.Position)
            wait(1) -- Interval between teleports
        end
    end
end

function UserInterface:ActivateBuy()
    print("Buy activated!")
    -- Example: Buy fighting styles
    local FightingStyles = {"Boxing", "Hamon", "Spin"}
    for _, style in pairs(FightingStyles) do
        print("Buying style: " .. style)
        -- Add logic for purchase
    end
end

-- Create the menu when the script is loaded
UserInterface:CreateMenu()
