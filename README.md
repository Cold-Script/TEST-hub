game:GetService("Workspace").CurrentRooms.DescendantAdded:Connect(function(v)
    if not _G.IncreasedDistance then return end
    if v.IsA(v,"ProximityPrompt") then
       if _G.IncreasedDistance then
           v.MaxActivationDistance *= _G.IncreasedDistance and 2 or 0.5
       end
    end
end)
-- // Linoria Ui \\
local repo = 'https://raw.githubusercontent.com/Cold-Script/LinoriaLib/patch-3/'
local v0 = loadstring(game:HttpGet(repo .. 'Library.lua'))()
local v1 = loadstring(game:HttpGet(repo .. 'addons/ThemeManager.lua'))()
local v2 = loadstring(game:HttpGet(repo .. 'addons/SaveManager.lua'))()
local UI = v0:CreateWindow({
    Title = "SADHUB:( |★v1★",
    Center = true,
    AutoShow = true,
    TabPadding = 10,
    MenuFadeTime = 0
})

})
local function billboard(child, name, name2, name3)
	local billboard_gui = Instance.new("BillboardGui")
	billboard_gui.Active = true
	billboard_gui.AlwaysOnTop = true
	billboard_gui.ClipsDescendants = true
	billboard_gui.LightInfluence = 1
	billboard_gui.Size = UDim2.new(3, 0, 2, 0)
	billboard_gui.ResetOnSpawn = false
	billboard_gui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	billboard_gui.Parent = child
	billboard_gui.Name = "KiwiHighlight"
	if name2 then
		billboard_gui.Name = "KiwiHighlight_2"
	end
	if name3 then
		billboard_gui.Name = "KiwiHighlight_3"
	end

	local text_label = Instance.new("TextLabel")
	text_label.Font = Enum.Font.Oswald
	text_label.Text = name
	text_label.TextColor3 = Color3.new(1, 1, 1)
	text_label.TextScaled = true
	text_label.TextSize = 10
	text_label.TextWrapped = true
	text_label.BackgroundColor3 = Color3.new(1, 1, 1)
	text_label.BackgroundTransparency = 1
	text_label.BorderColor3 = Color3.new(0, 0, 0)
	text_label.BorderSizePixel = 0
	text_label.Size = UDim2.new(1, 0, 1, 0)
	text_label.Visible = true
	text_label.Parent = billboard_gui

	local uistroke = Instance.new("UIStroke")
	uistroke.Thickness = 1
	uistroke.Parent = text_label

	spawn(function()
		while task.wait() do
			local hue = tick() % 5 / 5
			local color = Color3.new(1, 1, 1) 
			text_label.TextColor3 = color
		end
	end)
end

local function selection(child, name, name2, name3)
	billboard(child, name, name2, name3)
	local hi = Instance.new("Highlight")
	hi.Parent = child
	hi.Adornee = child
	hi.OutlineColor = Color3.fromRGB(161, 0, 0)
	hi.FillColor = Color3.fromRGB(255, 0, 0)
	hi.FillTransparency = 0.75
	hi.Name = "KiwiHighlight"
	if name2 then
		hi.Name = "KiwiHighlight_2"
	end
	if name3 then
		hi.Name = "KiwiHighlight_3"
	end
	if child:IsA("Part") then
		child.Color = Color3.fromRGB(0, 0, 0)
		child.Transparency = 0
	end
	spawn(function()
		while task.wait() do
			if hi then
				local hue = tick() % 5 / 5
				local color = Color3.new(1, 1, 1) 
				hi.OutlineColor = color
				hi.FillColor = color
			end
		end
	end)
end


function checkDistance(part, extra)
	if not extra then extra = 15 end
	if not game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") or not part then
		return false
	end
	local distanceToPart = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - part.Position).magnitude
	if distanceToPart <= extra then
		return true
	end
	return false
end

local v10={"RushMoving","AmbushMoving","Snare","A60","A120","SeekMoving","JeffTheKiller","Eyes"};local v11={"Candle","Crucifix","SkeletonKey","Vitamins","Lockpick","Lighter","Flashlight"};local v12=game.Players.LocalPlayer;local v13=v12.Character or v12.CharacterAdded:Wait();local v14=v13:FindFirstChildOfClass("Humanoid") or v13:WaitForChild("Humanoid") ;if  not fireproximityprompt then local v226=Instance.new("Message",workspace);v226.Text="you have fireproximityprompt function bro get better executor";task.wait(12 -6 );v226:Destroy();error("no prox");end function esp(v63,v64,v65,v66)local v67=0 -0 ;local v68;local v69;local v70;local v71;while true do if (v67==(1 + 2)) then if (v65 and v66) then local v431=1690 -(1121 + 569) ;local v432;local v433;while true do if (v431==2) then v432.Size=UDim2.new(214 -(22 + 192) ,691 -(483 + 200) ,0,8);v432.Position=UDim2.new(1463.5 -(1404 + 59) ,0 -0 ,0.5,0 -0 );Instance.new("UICorner",v432).CornerRadius=UDim.new(1,765 -(468 + 297) );Instance.new("UIStroke",v432);v431=565 -(334 + 228) ;end if (v431==3) then v433=Instance.new("TextLabel",v69);v433.AnchorPoint=Vector2.new(0.5,0.5);v433.BackgroundTransparency=1 -0 ;v433.BackgroundColor3=v64;v431=2 + 2 ;end if (5==v431) then v433.TextSize=20;v433.Text=v66;Instance.new("UIStroke",v433);task.spawn(function()while v69 do if ((v69.Adornee==nil) or  not v69.Adornee:IsDescendantOf(workspace)) then local v882=236 -(141 + 95) ;while true do if (v882==(0 + 0)) then v69.Enabled=false;v69.Adornee=nil;v882=1;end if (v882==1) then v69:Destroy();break;end end end task.wait();end end);break;end if (v431==4) then v433.TextColor3=v64;v433.Size=UDim2.new(2 -1 ,0 -0 ,0 + 0 ,136 -86 );v433.Position=UDim2.new(0.5,0,0.6,0);v433.Font=Enum.Font.Oswald;v431=4 + 1 ;end if (1==v431) then v69.MaxDistance=1042 + 958 ;v432=Instance.new("Frame",v69);v432.AnchorPoint=Vector2.new(0.5 -0 ,0.5);v432.BackgroundColor3=v64;v431=2 + 0 ;end if ((163 -(92 + 71))==v431) then v69=Instance.new("BillboardGui",game.CoreGui);v69.AlwaysOnTop=true;v69.Size=UDim2.new(0,400,0 + 0 ,168 -68 );v69.Adornee=v65;v431=766 -(574 + 191) ;end end end v71={};v67=4 + 0 ;end if ((9 -5)==v67) then v71.delete=function()for v434,v435 in pairs(v70) do local v436=0 + 0 ;while true do if (v436==(849 -(254 + 595))) then v435.Adornee=nil;v435.Visible=false;v436=127 -(55 + 71) ;end if (v436==1) then v435:Destroy();break;end end end if v69 then local v505=0 -0 ;while true do if (v505==(1791 -(573 + 1217))) then v69:Destroy();break;end if (v505==0) then v69.Enabled=false;v69.Adornee=nil;v505=2 -1 ;end end end end;return v71;end if (v67==(1 + 1)) then for v363,v364 in pairs(v68) do if v364:IsA("BasePart") then table.insert(v70,box);task.spawn(function()while box do local v704=0 -0 ;while true do if (v704==(939 -(714 + 225))) then if ((box.Adornee==nil) or  not box.Adornee:IsDescendantOf(workspace)) then box.Adornee=nil;box.Visible=true;box:Destroy();end task.wait();break;end end end end);end end function hightlightoutboi(v365,v366)local v367;if v366:FindFirstChildOfClass("Highlight") then v367=v366:FindFirstChildOfClass("Highlight");v367.OutlineColor=v365;v367.OutlineTransparency=0 -0 ;v367.FillColor=v365;v367.FillTransparency=0.5 -0 ;else local v510=0 + 0 ;while true do if (v510==(2 -0)) then v367.FillTransparency=806.5 -(118 + 688) ;v367.OutlineColor=v365;v510=51 -(25 + 23) ;end if (v510==(0 + 0)) then v367=Instance.new("Highlight",v366);v367.Enabled=true;v510=1887 -(927 + 959) ;end if (v510==(3 -2)) then v367.Name="Esphihihi";v367.FillColor=v365;v510=734 -(16 + 716) ;end if (v510==(5 -2)) then v367.OutlineTransparency=0;break;end end end local v368={};v368.delete=function()v367:Destroy();end;return v368;end v67=100 -(11 + 86) ;end if (v67==(2 -1)) then v69=nil;v70={};v67=287 -(175 + 110) ;end if (v67==(0 -0)) then v68=nil;if (typeof(v63)=="Instance") then if v63:IsA("Model") then v68=v63:GetChildren();elseif v63:IsA("BasePart") then v68={v63,table.unpack(v63:GetChildren())};end elseif (typeof(v63)=="table") then v68=v63;end v67=1797 -(503 + 1293) ;end end end local v15=game.ReplicatedStorage:WaitForChild("EntityInfo");function message(v72)local v73=0 -0 ;local v74;while true do if (v73==1) then task.wait(4 + 1 );v74:Destroy();break;end if (v73==0) then v74=Instance.new("Message",workspace);v74.Text=tostring(v72);v73=1;end end end local v16={espdoors=false,espkeys=false,espitems=false,espbooks=false,esprush=false,espchest=false,esplocker=false,esphumans=false,espgold=false,goldespvalue=1061 -(810 + 251) ,hintrush=false,hintrushhee=false,light=false,instapp=false,noseek=false,nogates=false,nopuzzle=false,noa90=false,noskeledoors=false,noseekarmsfire=false,noscreech=false,nodupe=false,getcode=false,getcodet=false,roomsnolock=false,draweraura=false,autorooms=false,itemsaura=false,autopulllever=false,bookcollecter=false,breakercollecter=false};local v17={table.unpack(v16)};local v18={doors={},keys={},items={},books={},entity={},chests={},lockers={},people={},gold={}};local v19=CFrame.new;local v20=game:GetService("ReplicatedStorage").GameData.LatestRoom;local v21=game:GetService("ReplicatedStorage").GameData.ChaseStart;local v22;v22=hookmetamethod(game,"__namecall",function(v75,...)local v76=0 + 0 ;local v77;local v78;while true do if (v76==(0 + 0)) then v77={...};v78=getnamecallmethod();v76=534 -(43 + 490) ;end if (v76==(734 -(711 + 22))) then if ((tostring(v75)=="Screech") and (v78=="FireServer") and getgenv().avoidsc) then local v437=0;while true do if (v437==(0 -0)) then v77[860 -(240 + 619) ]=true;return v22(v75,unpack(v77));end end end if ((tostring(v75)=="ClutchHeartbeat") and (v78=="FireServer") and getgenv().winhb) then v77[2]=true;return v22(v75,unpack(v77));end v76=1 + 1 ;end if (v76==(2 -0)) then return v22(v75,...);end end end);workspace.ChildAdded:Connect(function(v79)task.wait();if ((v79.Name=="RushMoving") or (v79.Name=="AmbushMoving")) then while workspace:FindFirstChild(v79.Name) and getgenv().hxde  do task.wait();part=v79:WaitForChild("RushNew");game.Players.LocalPlayer.Character.Collision.CFrame=CFrame.new(part.Position + Vector3.new(0 + 0 ,1819 -(1344 + 400) ,0) );end end end);
local WTF1 = UI:AddTab("Main")
local OMG1 = WTF1:AddLeftGroupbox("Chặn Thực Thể")
local OMG2 = WTF1:AddRightGroupbox("Xoá Thực Thể")
OMG2:AddToggle("MyToggle",{Text="Xoá Halt",Default=false,Tooltip="Anti Halt",Callback=function(v122)local v123=0;while true do if (v123==(1480 -(641 + 839))) then _G.BypassHalte=v122;if (_G.BypassHalte==true) then local v472=913 -(910 + 3) ;local v473;while true do if (v472==(0 -0)) then v473=game:GetService("ReplicatedStorage").ClientModules.EntityModules.Shade;v473.Parent=game.Workspace;break;end end elseif (_G.BypassHalte==false) then local v642=1684 -(1466 + 218) ;local v643;while true do if (v642==(0 + 0)) then v643=game.Workspace.Shade;v643.Parent=game:GetService("ReplicatedStorage").ClientModules.EntityModules;break;end end end break;end end end});OMG1:AddToggle("MyToggle",{Text="Chặn Thù Doạ từ Void,Glitch",Default=false,Tooltip="Anti Glitch & Void No JumpScares",Callback=function(v124)local v125=1148 -(556 + 592) ;while true do if (v125==(0 + 0)) then _G.GV=v124;if (_G.GV==true) then local v474=808 -(329 + 479) ;local v475;local v476;while true do if (v474==1) then v475.Parent=game.Workspace;v476.Parent=game.Workspace;break;end if (v474==(854 -(174 + 680))) then v475=game:GetService("ReplicatedStorage").ClientModules.EntityModules.Glitch;v476=game:GetService("ReplicatedStorage").ClientModules.EntityModules.Void;v474=3 -2 ;end end elseif (_G.GV==false) then local v644=0 -0 ;local v645;local v646;while true do if (v644==0) then v645=game.Workspace.Glitch;v646=game.Workspace.Void;v644=1 + 0 ;end if ((740 -(396 + 343))==v644) then v645.Parent=game:GetService("ReplicatedStorage").ClientModules.EntityModules;v646.Parent=game:GetService("ReplicatedStorage").ClientModules.EntityModules;break;end end end break;end end end});OMG1:AddToggle("MyToggle",{Text="Chặn Cửa Sai",Default=false,Tooltip="Anti Dupe",Callback=function(v128)v16.nodupe=v128;if v128 then local v288;v288=game:GetService("ReplicatedStorage").GameData.LatestRoom:GetPropertyChangedSignal("Value"):Connect(function()task.wait();for v397,v398 in pairs(game:GetService("Workspace").CurrentRooms:GetDescendants()) do if (v398.Name=="DoorFake") then v398.Hidden.CanTouch=false;end end repeat task.wait();until  not v16.nodupe v288:Disconnect();end);end end});local v48=game.ReplicatedStorage:WaitForChild("EntityInfo"):WaitForChild("A90");OMG2:AddToggle("MyToggle",{Text="Xoá A90",Default=false,Tooltip="Bypass A-90 Use In The Rooms",Callback=function(v130)v16.noa90=v130;if v130 then local v289=0 + 0 ;local v290;while true do if (v289==(1477 -(29 + 1448))) then v290=v12.PlayerGui:WaitForChild("MainUI"):WaitForChild("Jumpscare"):FindFirstChild("Jumpscare_A90");if v290 then v290.Parent=nil;v48.Parent=nil;repeat task.wait();game.SoundService.Main.Volume=1390 -(135 + 1254) ;until  not v16.noa90 v290.Parent=v12.PlayerGui.MainUI.Jumpscare;v48.Parent=v15;end break;end end end end});game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.bypassSnare then for v399,v400 in pairs(game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):GetChildren()) do if (v400.Name=="Snare") then v400.Hitbox['TouchInterest']:Destroy();end end end end);end);OMG1:AddToggle("MyToggle",{Text="Không Dẫm Bẫy",Default=false,Tooltip="Anti Snare",Callback=function(v132)_G.bypassSnare=v132;end});game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.Eyhasd then if workspace:FindFirstChild("Eyes") then game:GetService("ReplicatedStorage").EntityInfo.MotorReplication:FireServer(0,(_G.Eyhasd and  -(452 -332)) or (0 -0) ,0,false);end end end);end);OMG1:AddToggle("MyToggle",{Text="Không gây máu từ eyes",Default=false,Tooltip="Eyes No Damage",Callback=function(v133)_G.Eyhasd=v133;end});local v49=getrawmetatable(game);local v50=v49.__namecall;setreadonly(v49,false);v49.__namecall=newcclosure(function(v134,...)args={...};if (DisableEyes and EyesOnMap) then if (tostring(v134)=="MotorReplication") then args[2 + 0 ]= -(1647 -(389 + 1138));end end return v50(v134,table.unpack(args));end);
game:GetService("Workspace").DescendantAdded:Connect(function(v186)if  not _G.antibanananana then return;end if v186.IsA(v186,"Part") then if _G.antibanananana then if (v186.Name=="BananaPeel") then v186.CanTouch=false;end end end end);OMG1:AddToggle("MyToggle",{Text="Không dẫm chuối",Default=false,Tooltip="Anti BananaPeel!",Callback=function(v187)local v188=0;while true do if (v188==(0 + 0)) then _G.antibanananana=v187;if (_G.antibanananana==true) then for v600,v601 in pairs(game:GetService("Workspace"):GetDescendants()) do if v601:IsA("Part") then if (v601.Name=="BananaPeel") then v601.CanTouch=false;end end end end break;end end end});game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.antije then for v413,v414 in pairs(game.workspace:GetChildren()) do if (v414.Name=="JeffTheKiller") then v414.Knife.CanTouch=false;end end for v415,v416 in pairs(game.workspace:GetChildren()) do if (v416.Name=="JeffTheKiller") then v416.Head.CanTouch=false;end end for v417,v418 in pairs(game.workspace:GetChildren()) do if (v418.Name=="JeffTheKiller") then v418.HumanoidRootPart.CanTouch=false;end end for v419,v420 in pairs(game.workspace:GetChildren()) do if (v420.Name=="JeffTheKiller") then v420["Left Arm"].CanTouch=false;end end for v421,v422 in pairs(game.workspace:GetChildren()) do if (v422.Name=="JeffTheKiller") then v422["Left Leg"].CanTouch=false;end end for v423,v424 in pairs(game.workspace:GetChildren()) do if (v424.Name=="JeffTheKiller") then v424["Right Arm"].CanTouch=false;end end for v425,v426 in pairs(game.workspace:GetChildren()) do if (v426.Name=="JeffTheKiller") then v426["Right Leg"].CanTouch=false;end end for v427,v428 in pairs(game.workspace:GetChildren()) do if (v428.Name=="JeffTheKiller") then v428.Torso.CanTouch=false;end end end end);end);OMG1:AddToggle("MyToggle",{Text="Chặt Chém Jeff The Killer",Default=false,Tooltip="Anti Jeff!",Callback=function(v189)_G.antije=v189;end});
OMG2:AddToggle("nsc",{Text="Xoá Cuộc diễn của Seek",Default=false,Callback=function(v119)v16.noseek=v119;if v119 then local v279;v279=workspace.CurrentRooms.ChildAdded:Connect(function(v333)local v334=0 -0 ;local v335;while true do if (v334==(0 + 0)) then v335=v333:WaitForChild("TriggerEventCollision",2);if v335 then v335:Destroy();end break;end end end);repeat task.wait();until  not v16.noseek v279:Disconnect();end end});game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.SeekESe then if game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):FindFirstChild("Seek_Arm") then for v528,v529 in pairs(game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):GetChildren()) do if (v529.Name=="Seek_Arm") then v529.AnimatorPart.CanTouch=false;end end end end end);end);game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.SeekES then if game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):FindFirstChild("ChandelierObstruction") then for v530,v531 in pairs(game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):GetChildren()) do if (v531.Name=="ChandelierObstruction") then v531.HurtPart.CanTouch=false;end end end end end);end);OMG2:AddToggle("MyToggle",{Text="Ngăn Chặt Tay Seek và Lửa",Default=false,Tooltip="Remove Seek Arms and Chandelier HitBox From Seek Chase",Callback=function(v111)_G.SeekESe=v111;_G.SeekES=v111;end})local Toggle = OMG2:AddToggle("Nos",{Text = "Không có Screech",Default = false,Tooltip = "BypassScreech",Callback = function(Value)if Value then Screech = game:GetService("ReplicatedStorage").Entities.Screech Screech:Destroy() else Screech:Disconnect()end;end})
local Toggle = OMG1:AddToggle("BK",{Text = "Chặn Damage Lava",Default = false,Tooltip = "BypassKillbricks",Callback = function(Value)if Value then for _, child in pairs(workspace.CurrentRooms:GetChildren()) do
if child then for _, v in pairs(child:GetDescendants()) do
if v.Name == "Lava" then v.CanTouch = false end end end end ; killBricks = workspace.CurrentRooms.ChildAdded:Connect(function(child)
task.wait(1)if child then for _, v in pairs(child:GetDescendants()) do
if v.Name == "Lava" then v.CanTouch = false end end end end)else
killBricks:Disconnect()
for _, child in pairs(workspace.CurrentRooms:GetChildren()) do
if child then for _, v in pairs(child:GetDescendants()) do
if v.Name == "Lava" then v.CanTouch = true end end end end end end});
local Toggle = OMG1:AddToggle("Beyes",{Text = "Chặn Lookman",Default = false,Tooltip = "BypassLookman",Callback = function(Value)if Value then
Lookman = game:GetService("RunService").RenderStepped:Connect(function()
game:GetService("ReplicatedStorage").RemotesFolder.MotorReplication:FireServer(0, 90, 0, false) end) else Lookman:Disconnect() end end})
local Toggle = OMG2:AddToggle("BS",{Text = "Xoá Tường Seek",Default = false,Tooltip = "BypassSeek",Callback = function(Value)if Value then for _, child in pairs(workspace.CurrentRooms:GetChildren()) do
if child.Parts:FindFirstChild("ScaryWall") then child.Parts.ScaryWall:Destroy() end end
SeekWall = workspace.CurrentRooms.ChildAdded:Connect(function(child)
task.wait(1)
if child.Parts:FindFirstChild("ScaryWall") then child.Parts.ScaryWall:Destroy() end end) else SeekWall:Disconnect() end end});
local Toggle = OMG2:AddToggle("BD",{Text = "Xoá DrakoBloxxers",Default = false,Tooltip = "BypassDrakoBloxxers",Callback = function(Value)if Value then
DrakoBloxxers = workspace.ChildAdded:Connect(function(child)
task.wait(1)
if child.Name == "Drakobloxxer" then child:Destroy() for _, v in pairs(workspace:GetChildren()) do if v.Name == "Sound" and v:IsA("Sound") then v:Destroy() end end end end) else DrakoBloxxers:Disconnect() end end})
game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.MSHNL then if game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):FindFirstChild("Chandelier") then game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets").Chandelier:Destroy();end end end);end);game:GetService("RunService").RenderStepped:Connect(function()pcall(function()if _G.MSHNL then if game.workspace.CurrentRooms[tostring(game:GetService("ReplicatedStorage").GameData.LatestRoom.Value)]:WaitForChild("Assets"):FindF
