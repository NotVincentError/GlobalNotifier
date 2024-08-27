# GlobalNotifier
GlobalNotifier is an enhanced utility for simplifying the use of MessagingService in Roblox. Designed with beginners in mind, it provides an intuitive interface for messaging, while still offering robust functionality for advanced developers. If you have any suggestions for optimizing or improving this module, please share your ideas.

The game: https://www.roblox.com/games/121702741662077/Interact-Universe

This the template which all your variables and topics are at!
```lua
local Warp = require(game:GetService("ReplicatedStorage"):FindFirstChild("ClientModules").Warp)
local Template = {}

Template.Topic = {}
Template.IndexTopic = true--show index topic 

local Remote: StringValue = {
	"Messenger",
	"Announcement",
	"AnnouncementGUI"
}

local RemoteWarp = {} -- Remote turned into warp

for _, name in ipairs(Remote) do
	table.insert(RemoteWarp, Warp.Server(name))
end

function Template:getRemote(index: NumberValue)
	if index >= 1 and index <= #RemoteWarp then
		return RemoteWarp[index]
	else
		return nil -- Return nil if the index is out of range
	end
end

function Template:getTopics(i: NumberValue)
	return Template.Topic[i]
end

return Template
```

I will update the guide etc. if i got time :3
