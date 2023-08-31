# BadgesPlus
Scripted by JavyDev (@Javy) 
[ Badges Plus ] The best roblox module allowing easy badges/achievements.

[ Links ]

[DevForum Documentation](https://devforum.roblox.com/t/badgesplus-free-easy-badge-awarding/2570929)

[Discord Server](https://discord.gg/wjmwafmEq5)

# Documentation
[ Usage ]
```
 -> local module = require("Path to this module")
 
 -> module.playerHasBadge(player, badgeId, output?) -> ... output: print result?, returns true or false
 -> module.awardBadge(player, badgeId, output?) -> ... output: print result?, returns true or false
 -> module.getBadgeInfo(badgeId, output?) -> ... output: print result?, returns info or error

 player -> PlayerObject --- e.g game.Players.JavyDev
 badgeId -> number --- e.g 123456789
 output -> boolean --- ... optional ; e.g true
```

[ Example Script ]
```
local module = require(script.Parent) --> ... replace with actual path
local badgeId = 2151242948

game.Players.PlayerAdded:Connect(function(p) --> a way you can do it

	--[[
	
	This could be used to give an welcome badge
	
	for example;
	
	-- Welcome badge giver using BadgesPlus
	game.Players.PlayerAdded:Connect(function(p)
		local hasBadge = module.playerHasBadge(p, badgeId)
		
		if not hasBadge then
			module.awardBadge(p, badgeId) --> ... returns true or false (true meaning success)
		else
			--> already has badge!
		end
	end)
	
	--]]

	-- Welcome badge giver using BadgesPlus
	game.Players.PlayerAdded:Connect(function(p)
		local hasBadge = module.playerHasBadge(p, badgeId)
		
		if not hasBadge then
			module.awardBadge(p, badgeId) --> ... returns true or false (true meaning success)
		else
			--> already has badge!
		end
	end)
	
	module.playerHasBadge(p, badgeId, true) --> ... returns true or false
	module.awardBadge(p, badgeId, true) --> ... returns true or false
	module.getBadgeInfo(p, true) --> ... returns info or error
end)
```

Enjoy!
