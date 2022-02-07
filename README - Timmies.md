### Timmies Job Done with bt-target -- or qb-target for QBCore by Kmack710
## Dependancies 
# QBCore and qb-bossmenu -- https://github.com/qbcore-framework
# nh-contextmenu -- https://github.com/nerohiro/nh-context
# bt-target or qb-target (option in config) -- https://github.com/BerkieBb/qb-target 
# Dons Mods made the map it can be found here https://dons.tebex.io/package/4330619 
# If you need support or for updates check out my discord - https://discord.gg/qpem5er64U
## My discord checks for leakers so if your a leaker you wont be able to join for support or updates!
# HTML stuff from Pluto with his permission check out his weedshop job! - https://github.com/Really-Pluto/qb-weedshop-qb-target
## This should be plug and play -- Just read through the config.lua before you start and add the Items below. 
## Stuff for qb-core/shared.lua 
```lua 
	-- 710-timmies
    --Job 
    ["timmies"] = {
		label = "Tim Hortons",
		defaultDuty = true,
		bossmenu = vector3(-342.291, -133.370, 39.009),
		grades = {
            ['0'] = {
                name = "In Training",
                payment = 2500
            },
			['1'] = {
                name = "Baker",
                payment = 3500
            },
			['2'] = {
                name = "Cashier",
                payment = 4500
            },
			['3'] = {
                name = "Supervisor",
                payment = 5000
            },
			['4'] = {
                name = "Manager",
				isboss = true,
                payment = 5500
            },
        },
	},
    ----
	-- ITEMS 
	["rawbacon"]  					= {["name"] = "rawbacon",						["label"] = "Raw Bacon",				["weight"] = 200,		["type"] = "item", 		["image"] = "rawbacon.png",				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Raw Bacon"},
	["rawchicken"]  				= {["name"] = "rawchicken",						["label"] = "Raw Chicken",				["weight"] = 200,		["type"] = "item", 		["image"] = "rawchicken.png",			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Raw Chicken!"},
	["rawwedges"]  					= {["name"] = "rawwedges",						["label"] = "Pre cut Raw Wedges",		["weight"] = 200,		["type"] = "item", 		["image"] = "rawwedges.png",			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Bag of pre cut raw Wedges"},
	["croissantdough"]  			= {["name"] = "croissantdough",					["label"] = "Croissant Dough",			["weight"] = 200,		["type"] = "item", 		["image"] = "croissantdough.png",		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Croissant Dough"},
	["chocolatefondant"]  			= {["name"] = "chocolatefondant",				["label"] = "Timmies Chocolate Fondant",["weight"] = 100,		["type"] = "item", 		["image"] = "chocolatefondant.png",		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Chocolate Fondant - Make Donuts and Croissants"},
	["cheese"]  					= {["name"] = "cheese",							["label"] = "Cheese",					["weight"] = 100,		["type"] = "item", 		["image"] = "cheese.png",				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Cheese - Who knows that type.."},
	["egg"]  						= {["name"] = "egg",							["label"] = "Fresh Egg",				["weight"] = 50,		["type"] = "item", 		["image"] = "egg.png",					["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Raw Fresh Egg"},
	["timbitsdough"]  				= {["name"] = "timbitsdough",					["label"] = "Timbits Dough",			["weight"] = 200,		["type"] = "item", 		["image"] = "timbitsdough.png",			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Dough to make Timbits!"},
	["timsdonutdough"]  			= {["name"] = "timsdonutdough",					["label"] = "Timmies Donut Dough",		["weight"] = 200,		["type"] = "item", 		["image"] = "timsdonutdough.png",		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Dough to make Timmies donuts!"},
	["bread"] 		 			 	= {["name"] = "bread",       		    		["label"] = "Bread",	 				["weight"] = 100, 		["type"] = "item", 		["image"] = "bread.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,   ["description"] = "Bread"},
	["meat"] 		 			 	= {["name"] = "meat",       		    		["label"] = "Meat",	 					["weight"] = 100, 		["type"] = "item", 		["image"] = "meat.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,   ["description"] = "Meat"},
	["timsveggies"] 	 			= {["name"] = "timsveggies",       			    ["label"] = "Timmies Veggies",	 		["weight"] = 100, 		["type"] = "item", 		["image"] = "lettuce.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,   ["description"] = "Lettuce, Tomatos and Onions"},
	-- cooked stuff 
	["timscookedmeat"] 		 		= {["name"] = "timscookedmeat",       		    ["label"] = "Cooked Meat",	 			["weight"] = 100, 		["type"] = "item", 		["image"] = "cookedmeat.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,   ["description"] = "Cooked Timmies Meat"},
	["timschocsprinkledonut"] 		= {["name"] = "timschocsprinkledonut", 			["label"] = "Chocolate Sprinkled Donut", ["weight"] = 5, 		["type"] = "item", 		["image"] = "timschocsprinkledonut.png", ["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Chocolate Sprinkled donut from Timmies!"},
	["timsbostoncreamdonut"] 		= {["name"] = "timsbostoncreamdonut", 			["label"] = "Boston Cream Donut", 		["weight"] = 5, 		["type"] = "item", 		["image"] = "timsbostoncreamdonut.png", ["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Boston Cream Donut from Timmies!"},
	["timsstrawberrydonut"] 		= {["name"] = "timsstrawberrydonut", 			["label"] = "Strawberry Donut", 		["weight"] = 5, 		["type"] = "item", 		["image"] = "timsstrawberrydonut.png", 	["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Strawberry Donut from Timmies!"},
	["timsjellydonut"] 				= {["name"] = "timsjellydonut", 				["label"] = "Jelly Donut", 				["weight"] = 5, 		["type"] = "item", 		["image"] = "timsjellydonut.png", 		["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Jelly Filled Donut from Timmies!"},
	["timsglazeddonut"] 			= {["name"] = "timsglazeddonut", 				["label"] = "Glazed Donut", 			["weight"] = 5, 		["type"] = "item", 		["image"] = "timsglazeddonut.png", 		["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Glazed Donut from Timmies!"},
	["timschocdipdonut"] 			= {["name"] = "timschocdipdonut", 				["label"] = "Chocolate Dip Donut", 		["weight"] = 5, 		["type"] = "item", 		["image"] = "timschocdipdonut.png", 	["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Chocolate Dip Donut from Timmies!"},
	["cookedegg"]  					= {["name"] = "cookedegg",						["label"] = "Freshly Cooked Egg",		["weight"] = 50,		["type"] = "item", 		["image"] = "cookedegg.png",			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Freshly Cooked Egg"},
	["bacon"]  						= {["name"] = "bacon",							["label"] = "Cooked Bacon",				["weight"] = 200,		["type"] = "item", 		["image"] = "bacon.png",				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Cooked Bacon"},
	["chicken"]  					= {["name"] = "chicken",						["label"] = "Cooked Chicken",			["weight"] = 200,		["type"] = "item", 		["image"] = "chicken.png",				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Cooked Chicken"},
	["wedges"]  					= {["name"] = "wedges",							["label"] = "Wedges",					["weight"] = 200,		["type"] = "item", 		["image"] = "wedges.png",				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Bunch Wedges"},
	["croissant"]  					= {["name"] = "croissant",						["label"] = "Croissant",				["weight"] = 200,		["type"] = "item", 		["image"] = "croissant.png",			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,   ["combinable"] = nil,  ["description"] = "Croissant Dough"},
	["timbits"]  					= {["name"] = "timbits",						["label"] = "Timbits",					["weight"] = 200,		["type"] = "item", 		["image"] = "timbits.png",				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Timmies Timbits!"},
	["choccroissant"]  				= {["name"] = "choccroissant",					["label"] = "Chocolate Croissant",		["weight"] = 200,		["type"] = "item", 		["image"] = "choccroissant.png",		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Chocolate Croissant from Timmies!"},
	["cheesecroissant"]  			= {["name"] = "cheesecroissant",				["label"] = "Cheese Croissant",			["weight"] = 200,		["type"] = "item", 		["image"] = "cheesecroissant.png",		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,  ["description"] = "Cheese Croissant from Timmies!"},
	-- Sandwiches 
	["beltbagel"] 					= {["name"] = "beltbagel", 						["label"] = "BELT Bagel", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "beltbagel.png", 			["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "BELT (Bacon, Egg, Lettuce and Tomato) Bagel from Timmies!"},
	["grilledcheese"] 				= {["name"] = "grilledcheese", 			 	  	["label"] = "Grilled Cheese Panini", 	["weight"] = 150, 		["type"] = "item", 		["image"] = "grilledcheese.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Grilled Cheese Panini"},
	["steakgrcheese"] 				= {["name"] = "steakgrcheese", 			 	  	["label"] = "Grilled Cheese and Steak Panini", 	["weight"] = 150, 	["type"] = "item", 	["image"] = "steakgrcheese.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Grilled Steak n Cheese Panini"},
	["tbcsandwich"] 				= {["name"] = "tbcsandwich", 					["label"] = "Turkey Bacon Club", 		["weight"] = 150, 		["type"] = "item", 		["image"] = "tbcsandwich.png", 			["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Turkey Bacon Club from Timmies!"},
	["extritalian"] 				= {["name"] = "extritalian", 			 	  	["label"] = "Extreme Italian", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "extritalian.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Extreme Italian from Timmies!"},
	["hamnswiss"] 					= {["name"] = "hamnswiss", 			 	  		["label"] = "Ham and Swiss", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "hamnswiss.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Ham and Swiss from Timmies!"},
	["chrispchickenc"] 				= {["name"] = "chrispchickenc", 			 	["label"] = "Chrispy Chicken Club", 	["weight"] = 150, 		["type"] = "item", 		["image"] = "chrispchickenc.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Chrispy Chicken Club from Timmies!"},
	-- Drinks 
	["fruitsmoothie"] 				= {["name"] = "fruitsmoothie", 					["label"] = "Fruit Smoothie", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "fruitsmoothie.png", 		["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fruit Smoothie from Timmies!"},
	["frozenlemon"] 				= {["name"] = "frozenlemon", 			 	  	["label"] = "Frozen Lemonade", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "frozenlemon.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Frozen Lemonade from Timmies!"},
	["icedcap"] 					= {["name"] = "icedcap", 			 	  		["label"] = "Iced Cap", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "icedcap.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Timmies Famous Iced Cap"},
	["icedcoffee"] 					= {["name"] = "icedcoffee", 					["label"] = "Iced Coffee", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timsiced.png", 			["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Iced Coffee from Timmies!"},
	["expressonice"] 				= {["name"] = "expressonice", 			 	  	["label"] = "Expresso on Ice", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "timsiced.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Expresso on Ice from Timmies!"},
	["icedlatte"] 					= {["name"] = "icedlatte", 			 	  		["label"] = "Iced Latte", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timsiced.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Iced Latte from Timmies!"},
	["vbicedlatte"] 				= {["name"] = "vbicedlatte", 			 		["label"] = "Vanilla Bean Iced Latte", 	["weight"] = 150, 		["type"] = "item", 		["image"] = "timsiced.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Vanilla Bean Iced Latte from Timmies!"},
	["icedclatte"] 					= {["name"] = "icedclatte", 					["label"] = "Iced Chocolate Latte", 	["weight"] = 150, 		["type"] = "item", 		["image"] = "timsiced.png", 			["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Iced Chocolate Latte from Timmies!"},
	["pepsi"] 						= {["name"] = "pepsi", 			 	  			["label"] = "Pepsi Bottle", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "pepsi.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Pepsi Bottle"},
	["timscoffee"] 				    = {["name"] = "timscoffee", 			  	  	["label"] = "Coffee", 					["weight"] = 200, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,	   ["combinable"] = nil,   ["description"] = "Timmies Famous Coffee!"},
	["steeptea"] 					= {["name"] = "steeptea", 			 	  		["label"] = "Steeped Tea", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Steeped Tea from Timmies!"},
	["frenchvanilla"] 				= {["name"] = "frenchvanilla", 					["label"] = "French Vanilla", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "French Vanilla from Timmies!"},
	["hotchocolate"] 				= {["name"] = "hotchocolate", 			 	  	["label"] = "Hot Chocolate", 			["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Hot Chocolate from Timmies!"},
	["cafemocha"] 					= {["name"] = "cafemocha", 			 	  		["label"] = "Cafe Mocha", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Cafe Mocha (Half Hot Chocolate Half Coffee) from Timmies!"},
	["latte"] 						= {["name"] = "latte", 			 				["label"] = "Latte", 					["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Latte from Timmies!"},
	["dreamlatte"] 					= {["name"] = "dreamlatte", 					["label"] = "Dream Latte", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false,  	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Dream Latte from Timmies!"},
	["cappuccino"] 					= {["name"] = "cappuccino", 			 	  	["label"] = "Cappuccino", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Cappuccino from Timmies!"},
	["bagtea"] 						= {["name"] = "bagtea", 			 	  		["label"] = "Bagged Tea", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "timshot.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Bagged Tea from Timmies!"},
	["preptimbits"] 						= {["name"] = "preptimbits", 			 	  		["label"] = "Prepped Tim Bit Dough", 				["weight"] = 150, 		["type"] = "item", 		["image"] = "preptimbits.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = false,    ["combinable"] = nil,   ["description"] = "Prepped Tim Bit Dough, to make some timbits!"},
	--- END OF TIMMIES STUFF 

```
--- preptimbits
### Consumables Stuff for qb-smallresources 
## server/consumables.lua 
```lua
--- 710 Timmies stuff  --- Food 
QBCore.Functions.CreateUseableItem("wedges", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timbits", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timschocsprinkledonut", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timsbostoncreamdonut", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timsstrawberrydonut", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timsjellydonut", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timsglazeddonut", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timschocdipdonut", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("choccroissant", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("cheesecroissant", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("tbcsandwich", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("extritalian", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("hamnswiss", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
---
QBCore.Functions.CreateUseableItem("chrispchickenc", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("grilledcheese", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("steakgrcheese", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("beltbagel", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
----- Drinks 
QBCore.Functions.CreateUseableItem("fruitsmoothie", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("frozenlemon", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("icedcap", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("icedcoffee", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("expressonice", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("icedlatte", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("vbicedlatte", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("icedclatte", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("pepsi", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("timscoffee", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("icedcoffee", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("steeptea", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("frenchvanilla", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("hotchocolate", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("cafemocha", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("latte", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("dreamlatte", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("cappuccino", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("bagtea", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)
--- End of 710-timmies stuff 
```
## qb-smallresources config.lua add this under consumables 
```lua
  --- 710-timmies stuff 
    ["wedges"] = math.random(15, 25),
    ["timbits"] = math.random(15, 25),
    ["timschocsprinkledonut"] = math.random(10, 25),
    ["timsbostoncreamdonut"] = math.random(10, 25),
    ["timsstrawberrydonut"] = math.random(10, 25),
    ["timsjellydonut"] = math.random(10, 25),
    ["timsglazeddonut"] = math.random(10, 25),
    ["timschocdipdonut"] = math.random(10, 25),
    ["choccroissant"] = math.random(15, 40),
    ["cheesecroissant"] = math.random(15, 40),
    ["tbcsandwich"] = math.random(35, 54),
    ["extritalian"] = math.random(35, 54),
    ["hamnswiss"] = math.random(40, 50),
    ["chrispchickenc"] = math.random(35, 54),
    ["grilledcheese"] = math.random(35, 40),
    ["steakgrcheese"] = math.random(40, 50),
    ["beltbagel"] = math.random(40, 50),
    ["fruitsmoothie"] = math.random(35, 40),
    ["frozenlemon"] = math.random(35, 54),
    ["icedcap"] = math.random(30, 50),
    ["icedcoffee"] = math.random(35, 54),
    ["expressonice"] = math.random(35, 54),
    ["icedlatte"] = math.random(30, 50),
    ["vbicedlatte"] = math.random(30, 50),
    ["icedclatte"] = math.random(20, 50),
    ["pepsi"] = math.random(30, 40),
    ["timscoffee"] = math.random(20, 40),
    ["steeptea"] = math.random(35, 40),
    ["frenchvanilla"] = math.random(35, 54),
    ["hotchocolate"] = math.random(30, 50),
    ["cafemocha"] = math.random(35, 54),
    ["latte"] = math.random(35, 54),
    ["dreamlatte"] = math.random(30, 50),
    ["cappuccino"] = math.random(30, 50),
    ["bagtea"] = math.random(20, 50),

```