local Library = loadstring(game:HttpGet("https://gist.githubusercontent.com/feellikegod666/e406b71317d6f1c5eea3407957eb76ce/raw/52adbc20e6308e0cb4330620c560967759ae1f3f/catto"))()
local Window = Library:CreateWindow("fraudsense", Vector2.new(600, 450), Enum.KeyCode.RightShift)

local Aiming = loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/57b772001e6698360a7531ed21d2d3f4/raw/267d73c89c6d1df8e924dca0d52945769df2abb2/fov"))()
local ESP = loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/586c8a265eb0d6b24b4874817157211a/raw/82ee3985459db74f59cc911ddddeb64ce79c4cd9/esp"))()
ESP:Toggle(false)
ESP.Tracers = false
ESP.Names = false
ESP.Boxes = false
Aiming.TeamCheck(false)
Aiming.VisibleCheck = false

local Workspace = game:GetService("Workspace")
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local LocalPlayer = Players.LocalPlayer
local Mouse = LocalPlayer:GetMouse()
local CurrentCamera = Workspace.CurrentCamera
local LocalPlayer = Players.LocalPlayer
local Mouse = LocalPlayer:GetMouse()
local CurrentCamera = Workspace.CurrentCamera

local FraudsenseSettings = {
    Blatant = {
        Movement = {
            SpeedEnabled = false,
            SpeedType = "Default",
            SpeedRender = "Default",
            SpeedAmount = 5
        },
        Cash = {
            AutoDrop = false,
            AutoDropAmount = 5000,
            AutoPickCash = false
        },
        Character = {
            AntiBag = false,
        },
    },
}

local AimingTab = Window:CreateTab("rage")
local SilentSection = AimingTab:CreateSector("target aim", "left")

local DaHoodSettings = {
    SilentAim = false,
    AimLock = false,
    Prediction = 0.178
}

local SilentAimToggle = SilentSection:AddToggle("target aim", true, function(bool)
    loadstring(game:HttpGet("https://raw.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/n23536457m457m23looo/main/loo"))();
end)

local FovCircleToggle = SilentSection:AddToggle("fov", nil, function(bool)
    Aiming.ShowFOV = bool
end)

local VisibleCheckToggle = SilentSection:AddToggle("auto prediction", nil, function(bool)
    
end)

local HitAirShootsToggle = SilentSection:AddToggle("airshot func", nil, function(bool)
    
end)

SilentSection:AddTextbox("prediction", nil, function(L_70_arg0)
    
end)

local fovsettings = AimingTab:CreateSector("fov stuff", "right")

local fovsize = fovsettings:AddSlider("fov size", 0, 30, 500, 1, function(value)
    Aiming.FOV = value
end)

local fovsides = fovsettings:AddSlider("fov sides", 1, 40, 40, 1, function(value)
    Aiming.FOVSides  = value
end)
-------------------------------
-----// AIMING FUNCTION -----
function Aiming.Check()
    if not (Aiming.Enabled == true and Aiming.Selected ~= LocalPlayer and Aiming.SelectedPart ~= nil) then
        return false
    end
 
    local Character = Aiming.Character(Aiming.Selected)
    local KOd = Character:WaitForChild("BodyEffects")["K.O"].Value
    local Grabbed = Character:FindFirstChild("GRABBING_CONSTRAINT") ~= nil
 
    if (KOd or Grabbed) then
        return false
    end
 
    return true
end
local __index
__index = hookmetamethod(game, "__index", function(t, k)
    if (t:IsA("Mouse") and (k == "Hit" or k == "Target") and Aiming.Check()) then
        local SelectedPart = Aiming.SelectedPart
        if (DaHoodSettings.SilentAim and (k == "Hit" or k == "Target")) then
            local Hit = SelectedPart.CFrame + (SelectedPart.Velocity * DaHoodSettings.Prediction)
 
            return (k == "Hit" and Hit or SelectedPart)
        end
    end
 
    return __index(t, k)
end)
 
local LMFAO = false
 
UserInputService.InputBegan:Connect(function(Key, Is)
    if Key.UserInputType == Enum.UserInputType.MouseButton2 and not Is then
        LMFAO = true
    end
end)
 
UserInputService.InputEnded:Connect(function(Key, Is)
    if Key.UserInputType == Enum.UserInputType.MouseButton2 and not Is then
        LMFAO = false
    end
end)


local aimlock = AimingTab:CreateSector("aimlock", "left")
local aimlocktoggle = aimlock:AddToggle("aimlock",  nil, function()
getgenv().AimPart = "HumanoidRootPart"
getgenv().AimlockKey = "v"
getgenv().AimRadius = 30
getgenv().ThirdPerson = true
getgenv().FirstPerson = true
getgenv().TeamCheck = false
getgenv().PredictMovement = true
getgenv().PredictionVelocity = 9
local L_27_, L_28_, L_29_, L_30_ =
    game:GetService "Players",
game:GetService "UserInputService",
game:GetService "RunService",
game:GetService "StarterGui"
local L_31_, L_32_, L_33_, L_34_, L_35_, L_36_, L_37_ =
    L_27_.LocalPlayer,
L_27_.LocalPlayer:GetMouse(),
workspace.CurrentCamera,
CFrame.new,
Ray.new,
Vector3.new,
Vector2.new
local L_38_, L_39_, L_40_ = true, false, false
local L_41_
getgenv().CiazwareUniversalAimbotLoaded = true
getgenv().WorldToViewportPoint = function(L_42_arg0)
    return L_33_:WorldToViewportPoint(L_42_arg0)
end
getgenv().WorldToScreenPoint = function(L_43_arg0)
    return L_33_.WorldToScreenPoint(L_33_, L_43_arg0)
end
getgenv().GetObscuringObjects = function(L_44_arg0)
    if L_44_arg0 and L_44_arg0:FindFirstChild(getgenv().AimPart) and L_31_ and L_31_.Character:FindFirstChild("Head") then
        local L_45_ = workspace:FindPartOnRay(L_35_(L_44_arg0[getgenv().AimPart].Position, L_31_.Character.Head.Position))
        if L_45_ then
            return L_45_:IsDescendantOf(L_44_arg0)
        end
    end
end
getgenv().GetNearestTarget = function()
    local L_46_ = {}
    local L_47_ = {}
    local L_48_ = {}
    for L_50_forvar0, L_51_forvar1 in pairs(L_27_:GetPlayers()) do
        if L_51_forvar1 ~= L_31_ then
            table.insert(L_46_, L_51_forvar1)
        end
    end
    for L_52_forvar0, L_53_forvar1 in pairs(L_46_) do
        if L_53_forvar1.Character ~= nil then
            local L_54_ = L_53_forvar1.Character:FindFirstChild("Head")
            if getgenv().TeamCheck == true and L_53_forvar1.Team ~= L_31_.Team then
                local L_55_ =
                    (L_53_forvar1.Character:FindFirstChild("Head").Position - game.Workspace.CurrentCamera.CFrame.p).magnitude
                local L_56_ =
                    Ray.new(
                        game.Workspace.CurrentCamera.CFrame.p,
                        (L_32_.Hit.p - game.Workspace.CurrentCamera.CFrame.p).unit * L_55_
                    )
                local L_57_, L_58_ = game.Workspace:FindPartOnRay(L_56_, game.Workspace)
                local L_59_ = math.floor((L_58_ - L_54_.Position).magnitude)
                L_47_[L_53_forvar1.Name .. L_52_forvar0] = {}
                L_47_[L_53_forvar1.Name .. L_52_forvar0].dist = L_55_
                L_47_[L_53_forvar1.Name .. L_52_forvar0].plr = L_53_forvar1
                L_47_[L_53_forvar1.Name .. L_52_forvar0].diff = L_59_
                table.insert(L_48_, L_59_)
            elseif getgenv().TeamCheck == false and L_53_forvar1.Team == L_31_.Team then
                local L_60_ =
                    (L_53_forvar1.Character:FindFirstChild("Head").Position - game.Workspace.CurrentCamera.CFrame.p).magnitude
                local L_61_ =
                    Ray.new(
                        game.Workspace.CurrentCamera.CFrame.p,
                        (L_32_.Hit.p - game.Workspace.CurrentCamera.CFrame.p).unit * L_60_
                    )
                local L_62_, L_63_ = game.Workspace:FindPartOnRay(L_61_, game.Workspace)
                local L_64_ = math.floor((L_63_ - L_54_.Position).magnitude)
                L_47_[L_53_forvar1.Name .. L_52_forvar0] = {}
                L_47_[L_53_forvar1.Name .. L_52_forvar0].dist = L_60_
                L_47_[L_53_forvar1.Name .. L_52_forvar0].plr = L_53_forvar1
                L_47_[L_53_forvar1.Name .. L_52_forvar0].diff = L_64_
                table.insert(L_48_, L_64_)
            end
        end
    end
    if unpack(L_48_) == nil then
        return nil
    end
    local L_49_ = math.floor(math.min(unpack(L_48_)))
    if L_49_ > getgenv().AimRadius then
        return nil
    end
    for L_65_forvar0, L_66_forvar1 in pairs(L_47_) do
        if L_66_forvar1.diff == L_49_ then
            return L_66_forvar1.plr
        end
    end
    return nil
end
L_32_.KeyDown:Connect(
    function(L_67_arg0)
        if L_67_arg0 == AimlockKey and L_41_ == nil then
            pcall(
                function()
                    if L_39_ ~= true then
                        L_39_ = true
                    end
                    local L_68_
                    L_68_ = GetNearestTarget()
                    if L_68_ ~= nil then
                        L_41_ = L_68_
                    end
                end
            )
        elseif L_67_arg0 == AimlockKey and L_41_ ~= nil then
            if L_41_ ~= nil then
                L_41_ = nil
            end
            if L_39_ ~= false then
                L_39_ = false
            end
        end
    end
)
L_29_.RenderStepped:Connect(
    function()
        if getgenv().ThirdPerson == true and getgenv().FirstPerson == true then
            if
                (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude > 1 or
                (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude <= 1
            then
                L_40_ = true
            else
                L_40_ = false
            end
        elseif getgenv().ThirdPerson == true and getgenv().FirstPerson == false then
            if (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude > 1 then
                L_40_ = true
            else
                L_40_ = false
            end
        elseif getgenv().ThirdPerson == false and getgenv().FirstPerson == true then
            if (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude <= 1 then
                L_40_ = true
            else
                L_40_ = false
            end
        end
        if L_38_ == true and L_39_ == true then
            if L_41_ and L_41_.Character and L_41_.Character:FindFirstChild(getgenv().AimPart) then
                if getgenv().FirstPerson == true then
                    if L_40_ == true then
                        if getgenv().PredictMovement == true then
                            L_33_.CFrame =
                                L_34_(
                                    L_33_.CFrame.p,
                                    L_41_.Character[getgenv().AimPart].Position +
                                    L_41_.Character[getgenv().AimPart].Velocity / PredictionVelocity
                                )
                        elseif getgenv().PredictMovement == false then
                            L_33_.CFrame = L_34_(L_33_.CFrame.p, L_41_.Character[getgenv().AimPart].Position)
                        end
                    end
                elseif getgenv().ThirdPerson == true then
                    if L_40_ == true then
                        if getgenv().PredictMovement == true then
                            L_33_.CFrame =
                                L_34_(
                                    L_33_.CFrame.p,
                                    L_41_.Character[getgenv().AimPart].Position +
                                    L_41_.Character[getgenv().AimPart].Velocity / PredictionVelocity
                                )
                        elseif getgenv().PredictMovement == false then
                            L_33_.CFrame = L_34_(L_33_.CFrame.p, L_41_.Character[getgenv().AimPart].Position)
                        end
                    end
                end
            end
        end
    end
)
end
)

aimlock:AddTextbox("aimlock key", nil, function(L_69_arg0)
		getgenv().AimlockKey = L_69_arg0
end)

aimlock:AddTextbox("prediction", nil, function(L_70_arg0)
    PredictionVelocity = L_70_arg0
end)

aimlock:AddDropdown("hitbox", {"Head", "UpperTorso", "HumanoidRootPart", "LowerTorso"}, "Head", false, function(L_71_arg0)
    getgenv().AimPart = L_71_arg0
end)


local TeleportsTab = Window:CreateTab("locations")
local gunssection = TeleportsTab:CreateSector("guns", "left")

local revolver = gunssection:AddButton("revolver", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-638.75, 18.8500004, -118.175011, -1, 0, 0, 0, 1, 0, 0, 0, -1)
end)

local ak = gunssection:AddButton("ak", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-587.529358, 5.39480686, -753.717712, -1, 0, 0, 0, 1, 0, 0, 0, -1)
end)

local smg = gunssection:AddButton("smg", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-577.123413, 5.47666788, -718.031433, -1, 0, 0, 0, 1, 0, 0, 0, -1)
end)

local ar = gunssection:AddButton("ar", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-591.824158, 5.46046877, -744.731628, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)

local dbs = gunssection:AddButton("double barrel", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1039.59985, 18.8513641, -256.449951, -1, 0, 0, 0, 1, 0, 0, 0, -1)
end)

local shotgun = gunssection:AddButton("shotgun", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-578.623657, 5.47212696, -725.131531, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)

local flame = gunssection:AddButton("flame thrower", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-157.122437, 50.9120102, -104.93145, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local tac = gunssection:AddButton("tactical shotgun", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(470.877533, 45.1272316, -620.630676, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local rpg = gunssection:AddButton("rpg", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(118.664856, -29.6487694, -272.349792, -1, 0, 0, 0, 1, 0, 0, 0, -1)
end)

local drumgun = gunssection:AddButton("drum gun", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-83.548996, 19.7020588, -82.1449585, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local armor = gunssection:AddButton("high armor", function(bool)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-939, -25, 571)
end)

local bat = gunssection:AddButton("bat", function(bool)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(380, 49, -283)
end)

local mediumarmor = gunssection:AddButton("medium", function(bool)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(528, 50, -637)
end)

local placessection = TeleportsTab:CreateSector("places", "right")

local church = placessection:AddButton("church", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(147.299988, 18.8493252, 31.7999744, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)

local admin1 = placessection:AddButton("admin base", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-872.853516, -34.4276848, -538.013306, -0.999724388, -3.9898886e-08, -0.0234765243, -3.9204977e-08, 1, -3.00177518e-08, 0.0234765243, -2.90890814e-08, -0.999724388)
end)

local admin2 = placessection:AddButton("admin guns", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-808.708557, -39.6492004, -932.789368, 0.999899805, 2.01343173e-08, -0.0141554065, -2.17800533e-08, 1, -1.16108232e-07, 0.0141554065, 1.16404912e-07, 0.999899805)
end)

local admin3 = placessection:AddButton("admin food", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-788.053406, -39.6492004, -932.951233, 0.998369277, 2.46515359e-08, 0.0570784509, -2.8773524e-08, 1, 7.13949646e-08, -0.0570784509, -7.29209759e-08, 0.998369277)
end)

local ufo = placessection:AddButton("ufo", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(2.85052466, 132, -736.571106, -0.0460956171, -4.24733706e-08, -0.998937011, 7.26012459e-08, 1, -4.58687275e-08, 0.998937011, -7.46384217e-08, -0.0460956171)
end)

local casino = placessection:AddButton("casino", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-995, 21.6998043, -153.100037, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local bank = placessection:AddButton("bank", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-318.891174, 80.2145309, -257.177429, 0.0479469746, -5.14644114e-08, 0.998850107, -3.12971538e-09, 1, 5.16738901e-08, -0.998850107, -5.60372015e-09, 0.0479469746)
end)

local taco = placessection:AddButton("taco", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(584.026855, 48.1605072, -474.033936, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local revRoof = placessection:AddButton("revolver roof", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-634.463135, 80.434761, -204.232559, -0.0190527271, -1.03574322e-07, -0.999818563, 4.36709335e-09, 1, -1.03676342e-07, 0.999818563, -6.3416179e-09, -0.0190527271)
end)

local playground = placessection:AddButton("playground", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-282.694153, 19.7496624, -807.719727, 1, 0, 0, 0, 1, 0, 0, 0, 1)
end)

local gas = placessection:AddButton("gas station", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(604.800415, 46.0998344, -258.249573, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)

local cementery = placessection:AddButton("cementery", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(135.109558, 99.75, -57.2315979, 0.999993503, -0.000633752206, -0.0035054055, 0.000638642872, 0.999998808, 0.00139435288, 0.00350463158, -0.00139658386, 0.999992728)
end)

local school = placessection:AddButton("school roof", function(bool)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-525.353455, 68.125, 311.824402, 0.999992013, 1.03866675e-08, -0.00399552286, -1.03507425e-08, 1, 9.01170427e-09, 0.00399552286, -8.97027519e-09, 0.999992013)
end)

--- Esp Tab ---
local EspSection = AimingTab:CreateSector("esp", "right")

local espToggle = EspSection:AddToggle("enable esp", false, function(bool)
    ESP:Toggle(bool)
end)

local tracersToggle = EspSection:AddToggle("enable tracers", false, function(bool)
    ESP.Tracers = bool
end)

local namesToggle = EspSection:AddToggle("enable names", false, function(bool)
    ESP.Names = bool
end)

local boxesToggle = EspSection:AddToggle("enable boxes", false, function(bool)
    ESP.Boxes = bool
end)
espToggle:AddKeybind()

local togglessector = AimingTab:CreateSector("other stuff", "right")
local Reach = togglessector:AddToggle("reach", nil, function(e)
    if e == true then
        game:GetService('RunService'):BindToRenderStep("reach", 0 , function()
            local success, err = pcall(function()
                if game.Players.LocalPlayer.Character.BodyEffects.Attacking.Value == true then
                    for i,v in pairs(game:GetService('Players'):GetChildren()) do
                        if (v.Character.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.LeftHand.Position).Magnitude <= 50 then
                            if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool") then
                                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool"):FindFirstChild('Handle') then
                                    firetouchinterest(game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Handle, v.Character.UpperTorso, 0)
                                else
                                    firetouchinterest(game.Players.LocalPlayer.Character['RightHand'], v.Character.UpperTorso, 0)
                                    firetouchinterest(game.Players.LocalPlayer.Character['LeftHand'], v.Character.UpperTorso, 0)
                                    firetouchinterest(game.Players.LocalPlayer.Character['RightFoot'], v.Character.UpperTorso, 0)
                                    firetouchinterest(game.Players.LocalPlayer.Character['LeftFoot'], v.Character.UpperTorso, 0)
                                    firetouchinterest(game.Players.LocalPlayer.Character['RightLowerLeg'], v.Character.UpperTorso, 0)
                                    firetouchinterest(game.Players.LocalPlayer.Character['LeftLowerLeg'], v.Character.UpperTorso, 0)
                                end
                            end
                        end
                    end
                end
            end)
        end)
    elseif e == false then
        game:GetService('RunService'):UnbindFromRenderStep("Reach")
    end
end)

local AntiStomp = togglessector:AddToggle("anti stomp", nil, function(x)
    if x == true then
        game:GetService('RunService'):BindToRenderStep("Anti-Stomp", 0 , function()
            if game.Players.LocalPlayer.Character.Humanoid.Health <= 5 then
                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                    if v:IsA('MeshPart') or v:IsA('Part') then
                        v:Destroy()
                    end
                end
                for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
                    if v:IsA('Accessory') then
                        v.Handle:Destroy()
                    end
                end
            end
        end)
    elseif x == false then
        game:GetService('RunService'):UnbindFromRenderStep("Anti Stomp")
    end
end)

local fly2 = togglessector:AddButton("fly", function()
    loadstring(Game:HttpGet('https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/1c42fc4d9c1793644ad5284bd98c7b15/raw/12b6d2632babd83e532f9fe30c9e66b9c7667450/fly'))()
    game.StarterGui:SetCore("SendNotification", {
        Title = "fraudsense";
        Text = "Fly keybind is X.";
        Icon = "";
        Duration = "BLANK";
        callbakc = bindableFunction;
    })
end)

local fovchanger = togglessector:AddSlider("fov changer", 1, 70, 120, 1, function(value)
    game:GetService'Workspace'.Camera.FieldOfView = value
end)

getgenv().SpinBotSpeed = 20

local spinbot = togglessector:AddToggle("spinbot", nil, function(state)
	function getRoot(char)
				local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('UpperTorso')
				return rootPart
			end

			if state == true then
				local Spin = Instance.new("BodyAngularVelocity")
				Spin.Name = "Spinning"
				Spin.Parent = getRoot(game.Players.LocalPlayer.Character)
				Spin.MaxTorque = Vector3.new(0, math.huge, 0)
				Spin.AngularVelocity = Vector3.new(0,getgenv().SpinBotSpeed,0)
			else
				for i,v in pairs(getRoot(game.Players.LocalPlayer.Character):GetChildren()) do
					if v.Name == "Spinning" then
						v:Destroy()
					end
				end
			end
		end)
spinbot:AddKeybind()

local spinbotspeed = togglessector:AddSlider("speed", 1, 20, 50, 1, function(value)
    getgenv().SpinBotSpeed = value
end)

--- Visuals Tab ---
local VisualsTab = Window:CreateTab("character")
local VisualsSection = VisualsTab:CreateSector("character", "left")

local animationgamepass = VisualsSection:AddButton("animation gamepass", function()
	loadstring(game:HttpGet('https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/4652ea1afb452348f528552a9f708d60/raw/0429b6df2f5eef92733a82462b73e516bc0e1513/animationpack'))()
end)

local headlbutton = VisualsSection:AddButton("headless clientside", function(bool)
game.Players.LocalPlayer.Character.Head.Transparency = 1
for i,v in pairs(game.Players.LocalPlayer.Character.Head:GetChildren()) do
if (v:IsA("Decal")) then
v:Destroy()
end
end
end)

local animatedbeastmode = VisualsSection:AddButton("animated beastmode", function()
	while true do
local player = game.Players.LocalPlayer.Character
if player:findFirstChild("Humanoid") then
    player.Head.face.Texture = "https://www.roblox.com/asset/?id=209712379"
    end
wait(1)
if player:findFirstChild("Humanoid") then
    player.Head.face.Texture = "https://www.roblox.com/asset/?id=127959433"
    end
wait(1)
end
end)

local facesection = VisualsTab:CreateSector("face changer", "right")

local meanie = facesection:AddButton("meanie", function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/eksotopro/holders/main/faces/508490451.lua'))()
end)

local sshf = facesection:AddButton("super super happy face", function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/eksotopro/holders/main/faces/494290547.lua'))()
end)

local silverpunk = facesection:AddButton("silver punk face", function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/eksotopro/holders/main/faces/387256104.lua'))()
end)

local yum = facesection:AddButton("yum", function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/eksotopro/holders/main/faces/26018945.lua'))()
end)

local playful = facesection:AddButton("playfull vampire", function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/eksotopro/holders/main/faces/2409281591.lua'))()
end)

local beastmode = facesection:AddButton("beast mode", function()
	loadstring(game:HttpGet('https://raw.githubusercontent.com/eksotopro/holders/main/faces/127959433.lua'))()
end)

--- Misc Tab ---
local MiscTab = Window:CreateTab("desync and misc")
local MiscSection = MiscTab:CreateSector("miscellaneous", "left")
local scriptsSection = MiscTab:CreateSector("other stuff", "right")

local fpsboost = MiscSection:AddButton('low gfx', function(state)
    if state then
    
        local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
        local g = game
        local w = g.Workspace
        local l = g.Lighting
        local t = w.Terrain
        t.WaterWaveSize = 0
        t.WaterWaveSpeed = 0
        t.WaterReflectance = 0
        t.WaterTransparency = 0
        l.GlobalShadows = false
        l.FogEnd = 9e9
        l.Brightness = 0
        settings().Rendering.QualityLevel = "Level01"
        for i, v in pairs(g:GetDescendants()) do
            if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then
                v.Material = "Plastic"
                v.Reflectance = 0
            elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
                v.Transparency = 1
            elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
                v.Lifetime = NumberRange.new(0)
            elseif v:IsA("Explosion") then
                v.BlastPressure = 1
                v.BlastRadius = 1
            elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") then
                v.Enabled = false
            elseif v:IsA("MeshPart") then
                v.Material = "Plastic"
                v.Reflectance = 0
                v.TextureID = 10385902758728957
            end
        end
        for i, e in pairs(l:GetChildren()) do
            if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
                e.Enabled = false
            end
        end
    else
      end
end)

local trash = MiscSection:AddButton("trash talk", function(State)
    loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/f47e2561ae2269686a86b8ef554042c2/raw/2ce983de9d16ea07055feaee59327230fce29782/trash"))()
    game.StarterGui:SetCore("SendNotification", {
        Title = "fraudsense";
        Text = "Trash Talk keybind is J.";
        Icon = "";
        Duration = "BLANK";
        callbakc = bindableFunction;
    })
end)

local nocooldown = MiscSection:AddButton("no jump cooldown", function(State)
    loadstring(game:HttpGet('https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/904dbb8452f09a797283c766d7939e40/raw/d0ce4355c9f8de0b9435ae76302e488169d52037/nojumpcooldwon'))()
end)

local god = MiscSection:AddButton("god mode", function(State)
    loadstring(game:HttpGet('https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/f24de1dffcda943435a3dbef2c0d4903/raw/f45753d41565335f68fd17cf36038a82242098ab/god'))()
    game.StarterGui:SetCore("SendNotification", {
    Title = "fraudsense";
    Text = "This can't be stopped.";
    Icon = "";
    Duration = "BLANK";
    callbakc = bindableFunction;
    })
end)

local reset = MiscSection:AddButton("reset character", function(reset)
    game.Players.LocalPlayer.Character.Humanoid.Health = 0
end)

local idepomilion = MiscSection:AddButton('sing goofy songs', function(State)
    game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("Mam głód pierdolę wszystko","All")
wait(1)
game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("ty stój kiedy idę po milion","All")
wait(1.2)
game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("jxak znxów coś mi nie wyszło","All")
wait(1.3)
game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("i huj nadal idę po milion","All")
wait(0.7)
game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("już nie czekam na przyszłość ","All")
wait(0.8)
game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("alxe nie mów nic bo","All")
wait(0.9)
game.ReplicatedStorage.DefaultChatSystemChatEvents.SayMessageRequest:FireServer("bo bo idę po milion", "All")
end)

local MovementSector = MiscTab:CreateSector("movement", "right")
local SpeedToggle = MovementSector:AddToggle('speed enabled', false, function(State)
    FraudsenseSettings.Blatant.Movement.SpeedEnabled = State
end)

SpeedToggle:AddSlider(0, 5, 10, 1, function(Value)
    FraudsenseSettings.Blatant.Movement.SpeedAmount = Value
end)

MovementSector:AddDropdown("speed type", {"CFrame"}, "CFrame", false, function(Value)
    FraudsenseSettings.Blatant.Movement.SpeedType = Value
end)

MovementSector:AddDropdown("speed render type", {"Default", "Fast"}, "Default", false, function(Value)
    FraudsenseSettings.Blatant.Movement.SpeedRenderType = Value
end)
SpeedToggle:AddKeybind()

local swagfly = scriptsSection:AddButton("normal desync (x)", function ()
        loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/7af22484eff651087301b4effd914d95/raw/f97963f7044c2214ac2678702f62183f73cecdf3/desynnnnnc"))();
end)

local speedboost = scriptsSection:AddButton("spin desync (rejoin for disable)", function()
        loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/223a070cd27048d0d0ffb4c711caaadd/raw/7499e1e6f2fb29e9b5b84bd507e0daa82f0ade92/dawand2"))();
end)

local antilock = scriptsSection:AddButton("roll aa (reset for disable)", function()
        loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/a5b4a93c4c55843edbc1d9e5b6b67808/raw/f7093d020c4c270183c783cfed40955128ca62e8/rolla"))();
end)

local undergroundaa = scriptsSection:AddButton("underground aa (v)", function()
    loadstring(game:HttpGet("https://gist.githubusercontent.com/23b49j872b47324b723butwerbuwehbrwebr3/61cf461b7b3321c93a900f053bf0515e/raw/608ab869d05338a20b93963cf5d1da0874d3d64f/underground"))();
end)
