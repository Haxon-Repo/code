--[[

        _   _         _                _            _               _    _        _            _                _                   _            _     
       /\_\/\_\ _    / /\             /\ \         /\ \            / /\ /\ \     /\_\         /\ \     _    _  /\ \                /\ \         /\ \   
      / / / / //\_\ / /  \           /  \ \____   /  \ \          / /  \\ \ \   / / /        /  \ \   /\_\ /\_\\ \ \              /  \ \        \ \ \  
     /\ \/ \ \/ / // / /\ \         / /\ \_____\ / /\ \ \        / / /\ \\ \ \_/ / /        / /\ \ \_/ / // / / \ \ \            / /\ \ \       /\ \_\ 
    /  \____\__/ // / /\ \ \       / / /\/___  // / /\ \_\      / / /\ \ \\ \___/ /        / / /\ \___/ // / /   \ \ \          / / /\ \_\     / /\/_/ 
   / /\/________// / /  \ \ \     / / /   / / // /_/_ \/_/     / / /\ \_\ \\ \ \_/        / / /  \/____/ \ \ \____\ \ \        / / /_/ / /    / / /    
  / / /\/_// / // / /___/ /\ \   / / /   / / // /____/\       / / /\ \ \___\\ \ \        / / /    / / /   \ \________\ \      / / /__\/ /    / / /     
 / / /    / / // / /_____/ /\ \ / / /   / / // /\____\/      / / /  \ \ \__/ \ \ \      / / /    / / /     \/________/\ \    / / /_____/    / / /      
/ / /    / / // /_________/\ \ \\ \ \__/ / // / /______     / / /____\_\ \    \ \ \    / / /    / / /                \ \ \  / / /\ \ \  ___/ / /__     
\/_/    / / // / /_       __\ \_\\ \___\/ // / /_______\   / / /__________\    \ \_\  / / /    / / /                  \ \_\/ / /  \ \ \/\__\/_/___\    
        \/_/ \_\___\     /____/_/ \/_____/ \/__________/   \/_____________/     \/_/  \/_/     \/_/                    \/_/\/_/    \_\/\/_________/    


This Injection Screen is made by N4ri for his own exploit, Coco Z.
Please do not rename this and call this your own, this is unobfuscated
to give the least amount of impact to Coco Z. This is not meant for
anyone else.

- <3 N4ri


]]--

local CCInject = Instance.new("ScreenGui")
local MainFrame = Instance.new("ImageLabel")
local CocoLogo = Instance.new("ImageLabel")
local T2 = Instance.new("TextLabel")
local T1 = Instance.new("TextLabel")

CCInject.Name = "CCInject"
CCInject.Parent = game.CoreGui
CCInject.ResetOnSpawn = false

MainFrame.Name = "MainFrame"
MainFrame.Parent = CCInject
MainFrame.AnchorPoint = Vector2.new(0.5, 0)
MainFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
MainFrame.BackgroundTransparency = 1.000
MainFrame.BorderSizePixel = 0
MainFrame.ClipsDescendants = true
MainFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
MainFrame.ScaleType = Enum.ScaleType.Slice
MainFrame.SliceCenter = Rect.new(100, 100, 100, 100)

CocoLogo.Name = "CocoLogo"
CocoLogo.Parent = MainFrame
CocoLogo.AnchorPoint = Vector2.new(0.5, 0.5)
CocoLogo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CocoLogo.BackgroundTransparency = 1.000
CocoLogo.BorderSizePixel = 0
CocoLogo.ClipsDescendants = true
CocoLogo.Position = UDim2.new(0.5, 0, 1.5, 0)
CocoLogo.Size = UDim2.new(0, 90, 0, 90)

T2.Name = "T2"
T2.Parent = MainFrame
T2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
T2.BackgroundTransparency = 1.000
T2.BorderColor3 = Color3.fromRGB(27, 42, 53)
T2.BorderSizePixel = 0
T2.Position = UDim2.new(1.51400006, 0, 0.456, 0)
T2.Size = UDim2.new(0, 81, 0, 23)
T2.Font = Enum.Font.GothamBold
T2.Text = "Haxon"
T2.TextColor3 = Color3.fromRGB(255, 255, 255)
T2.TextSize = 25.000

T1.Name = "T1"
T1.Parent = MainFrame
T1.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
T1.BackgroundTransparency = 1.000
T1.BorderColor3 = Color3.fromRGB(27, 42, 53)
T1.BorderSizePixel = 0
T1.Position = UDim2.new(1.51400006, 0, 0.372999996, 0)
T1.Size = UDim2.new(0, 81, 0, 13)
T1.Font = Enum.Font.Gotham
T1.Text = "Welcome to"
T1.TextColor3 = Color3.fromRGB(255, 255, 255)
T1.TextSize = 12.000

local function CocoInjectLoad()
	local script = Instance.new('LocalScript', CCInject)

	local TweenService = game:GetService("TweenService")
	local time = 0.5 
	local RoundOut = TweenService:Create(script.Parent.MainFrame, TweenInfo.new(time), {SliceScale = 0.05})
	local RoundOutMore = TweenService:Create(script.Parent.MainFrame, TweenInfo.new(time), {SliceScale = 0})
	local FadeMain = TweenService:Create(script.Parent.MainFrame, TweenInfo.new(time), {ImageTransparency = 1})
	local FadeOutLogo = TweenService:Create(script.Parent.MainFrame.CocoLogo, TweenInfo.new(time), {ImageTransparency = 0})
	local FadeInText = TweenService:Create(script.Parent.MainFrame.T1, TweenInfo.new(time), {TextTransparency = 0})
	local FadeOutText = TweenService:Create(script.Parent.MainFrame.T1, TweenInfo.new(time), {TextTransparency = 1})
	
	wait(5)
	script.Parent.MainFrame:TweenPosition(UDim2.new(0.5,0,0.5,-57), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame:TweenSize(UDim2.new(0,115,0,115), "Out", "Quad", 0.5, true)
	wait(0.5)
	FadeOutLogo:Play()
	script.Parent.MainFrame.CocoLogo:TweenPosition(UDim2.new(0.5,0,0.5,0), "Out", "Quad", 0.5, true)
	wait(1)
	RoundOut:Play()
	script.Parent.MainFrame:TweenSize(UDim2.new(0,240,0,144), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame:TweenPosition(UDim2.new(0.5,0,0.5,-72), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.CocoLogo:TweenPosition(UDim2.new(0.328,0,0.5,0), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.T1:TweenPosition(UDim2.new(0.514,0,0.373,0), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.T2:TweenPosition(UDim2.new(0.514,0,0.456,0), "Out", "Quad", 0.5, true)
	wait(2)
	script.Parent.MainFrame:TweenSize(UDim2.new(0.5,0,0,40), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame:TweenPosition(UDim2.new(0.5,0,0,-40), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.CocoLogo:TweenPosition(UDim2.new(-1.328,0,0.5,0), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.T2:TweenPosition(UDim2.new(0.514,0,-1.456,0), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.T2:TweenPosition(UDim2.new(0.514,0,-1.456,0), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.T1:TweenSize(UDim2.new(1,0,0,12), "Out", "Quad", 0.5, true)
	script.Parent.MainFrame.T1:TweenPosition(UDim2.new(0,0,0.5,-6), "Out", "Quad", 0.5, true)
	RoundOutMore:Play()
	FadeMain:Play()
	FadeOutText:Play()
	wait(0.5)
	FadeInText:Play()
	script.Parent.MainFrame.T1.Text = "Welcome to Haxon API"
	wait(2)
	FadeOutText:Play()
	wait(0.5)
	FadeInText:Play()
	script.Parent.MainFrame.T1.Text = "axonexploits.weebly.com"
	wait(2)
	FadeOutText:Play()
	wait(0.5)
	CCInject:Destroy()
end
coroutine.wrap(CocoInjectLoad)()
