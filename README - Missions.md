## 710 Missions - A resource to help add more steps to getting things like drug location keys and so on. 

# Dependancies 
1. QBCore 
2. cd_drawtextui --- For optimized drawtext - https://github.com/dsheedes/cd_drawtextui


## SETUP 
1. Add below to your shared.lua or change the item in Config to use something else! :) 
2. Read config make sure everything is set up for your server. 
3. Add missions in the config and your good to go! 
4. Remember you must restart your server after adding this to the server. 

## For qb-core/shared/items.lua
```lua
["missiontablet"] 				 = {["name"] = "missiontablet",					["label"] = "Tablet",						["weight"] = 500,			["type"] = "item",		["image"] = "missiontablet.png",		["unique"] = true,		["useable"] = true,		["shouldClose"] = true,		["combinable"] = nil,				["description"] = "A Tablet that maybe have some work for you!"},
```


## Support 
Check out my discord if you need any support! - https://discord.gg/qpem5er64U