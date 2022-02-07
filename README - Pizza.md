### 710-Pizza Job and delivery! 
##Dependancies  
# QBCore and qb-bossmenu, qb-inventory -- https://github.com/qbcore-framework
# nh-contextmenu -- https://github.com/nerohiro/nh-context
# bt-target or qb-target (option in config) -- https://github.com/BerkieBb/qb-target 
# Dons Mods made the map it can be found here(free) https://dons.tebex.io/package/4492673 
# If you need support or for updates check out my discord - https://discord.gg/qpem5er64U
# Should be plug and play make sure to read the config as there is LOTS of options!
### For Shared.lua in qb-core ### All items and stuff for consumables below. ###
# Job 
```lua 
	["lspizza"] = {
		label = "LS Pizza",
		defaultDuty = true,
		bossmenu = vector3(-342.291, -133.370, 0.009),
		grades = {
            ['0'] = {
                name = "In Training",
                payment = 2500
            },
			['1'] = {
                name = "Cook",
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
```
# Items 
```lua 
	-- 710-Pizza Items 
	["pizzacheese"] 				= {["name"] = "pizzacheese", 			 	  	["label"] = "Pizza Cheese", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzacheese.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Cheese for Pizzas!"},
	["pizzasauce"] 					= {["name"] = "pizzasauce", 			 		["label"] = "Pizza Sauce", 				["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzasauce.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Pizza sauce to make Pizzas with!"},
	["pizzadough"] 					= {["name"] = "pizzadough", 			 		["label"] = "Pizza dough", 				["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzadough.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Pizza Dough to make Pizza with!"},
	["pepperoni"] 					= {["name"] = "pepperoni", 			 	 	 	["label"] = "Pizza Pepperoni", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "pepperoni.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Pepperoni to make Pizza with!"},
	["pineapple"] 					= {["name"] = "pineapple", 			 	 	 	["label"] = "Fresh Pineapple", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "pineapple.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fresh pineapple mainly used on Pizza!"},
	["rawbacon"] 					= {["name"] = "rawbacon", 			 			["label"] = "Raw Bacon", 				["weight"] = 100, 		["type"] = "item", 		["image"] = "rawbacon.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Raw Bacon!"},
	["rawchicken"] 					= {["name"] = "rawchicken", 			 		["label"] = "Raw Chicken", 				["weight"] = 100, 		["type"] = "item", 		["image"] = "rawchicken.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Raw Chicken!"},
	["rawchickenwings"] 			= {["name"] = "rawchickenwings", 			 	 ["label"] = "Raw Chicken Wings", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "rawchickenwings.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Raw Chicken Wings!"},
	["meat"] 						= {["name"] = "meat", 			 	 	 		["label"] = "Uncooked Meat", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "meat.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Uncooked meat"},
	["jalapenos"] 					= {["name"] = "jalapenos", 			 			["label"] = "Jalapenos", 				["weight"] = 100, 		["type"] = "item", 		["image"] = "jalapenos.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fresh Jalapenos"},
	["peppers"] 					= {["name"] = "peppers", 			 			["label"] = "Bell Peppers", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "peppers.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Bell Peppers!"},
	["tomato"] 						= {["name"] = "tomato", 			 			["label"] = "Fresh Tomato", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "tomato.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fresh Tomato!"},
	["bbqpsauce"] 					= {["name"] = "bbqpsauce", 			 	 	 	["label"] = "Pizza BBQ Sauce", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "bbqpsauce.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "BBQ Pizza Sauce"},
	["onions"] 						= {["name"] = "onions", 			 			["label"] = "Fresh Onions", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "onions.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fresh Onions"},
	["mushrooms"] 					= {["name"] = "mushrooms", 			 			["label"] = "Fresh Mushrooms", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "mushrooms.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fresh Mushrooms!"},
	["pcheesepizza"] 				= {["name"] = "pcheesepizza", 			 		["label"] = "Prepped Cheese Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Cheese Pizza ready to go in the oven!"},
	["ppeppizza"] 					= {["name"] = "ppeppizza", 			 	 	 	["label"] = "Prepped Pepperoni Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Pepperoni Pizza ready to go in the oven!"},
	["phawapizza"] 					= {["name"] = "phawapizza", 			 		["label"] = "Prepped Hawiian Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Hawaiian Pizza ready to go in the oven!"},
	["pmexpizza"] 					= {["name"] = "pmexpizza", 			 			["label"] = "Prepped Mexican Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Mexican Pizza ready to go in the oven!"},
	["pchickenpizza"] 				= {["name"] = "pchickenpizza", 			 		["label"] = "Prepped Chicken Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Chicken Pizza ready to go in the oven!"},
	["pbbqpizza"] 					= {["name"] = "pbbqpizza", 			 	 	 	["label"] = "Prepped BBQ Pizza", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "BBQ Pizza ready to go in the oven!"},
	["pveggiepizza"] 				= {["name"] = "pveggiepizza", 			 		["label"] = "Prepped Veggie Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "preppedpizza.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Veggie Pizza ready to go in the oven!"},
	["cheesepizza"] 				= {["name"] = "cheesepizza", 			 		["label"] = "Box of Cheese Pizza", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of Cheese Pizza"},
	["peppizza"] 					= {["name"] = "peppizza", 			 	 	 	["label"] = "Box of Pepperoni Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of Pepperoni Pizza!"},
	["hawapizza"] 					= {["name"] = "hawapizza", 			 			["label"] = "Box of Hawiian Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of Hawaiian Pizza!"},
	["mexpizza"] 					= {["name"] = "mexpizza", 			 			["label"] = "Box of Mexican Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of Mexican Pizza!"},
	["chickenpizza"] 				= {["name"] = "chickenpizza", 			 		["label"] = "Box of Chicken Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of Chicken Pizza!"},
	["bbqpizza"] 					= {["name"] = "bbqpizza", 			 	 	 	["label"] = "Box of BBQ Pizza", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of BBQ Pizza!"},
	["veggiepizza"] 				= {["name"] = "veggiepizza", 			 		["label"] = "Box of Veggie Pizza", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzaboxed.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box with 6 slices of Veggie Pizza!"},
	["slcheesepizza"] 				= {["name"] = "slcheesepizza", 			 		["label"] = "Slice of Cheese Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "slcheesepizza.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of Cheese Pizza"},
	["slpeppizza"] 					= {["name"] = "slpeppizza", 			 	 	["label"] = "Slice of Pepperoni Pizza", ["weight"] = 100, 		["type"] = "item", 		["image"] = "slpeppizza.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of Pepperoni Pizza!"},
	["slhawapizza"] 				= {["name"] = "slhawapizza", 			 		["label"] = "Slice of Hawiian Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "slhawapizza.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of Hawaiian Pizza!"},
	["slmexpizza"] 					= {["name"] = "slmexpizza", 			 		["label"] = "Slice of Mexican Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "slmexpizza.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of Mexican Pizza!"},
	["slchickenpizza"] 				= {["name"] = "slchickenpizza", 			 	["label"] = "Slice of Chicken Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "slchickenpizza.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of Chicken Pizza!"},
	["slbbqpizza"] 					= {["name"] = "slbbqpizza", 			 	 	["label"] = "Slice of BBQ Pizza", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "slbbqpizza.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of BBQ Pizza!"},
	["slveggiepizza"] 				= {["name"] = "slveggiepizza", 			 		["label"] = "Slice of Veggie Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "slveggiepizza.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Slice of Veggie Pizza!"},
	["pepcalzone"] 					= {["name"] = "pepcalzone", 			 		["label"] = "Pepperoni Calzone", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "pepcalzone.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Pepperoni Calzone - Basically a big Pizza Pocket"},
	["chcalzone"] 					= {["name"] = "chcalzone", 			 	 		["label"] = "Cheese Calzone", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "chcalzone.png", 			["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Cheese Calzone - Basically a big Pizza Pocket!"},
	["dzchickenwings"] 				= {["name"] = "dzchickenwings", 			 	["label"] = "Dozen Chicken Wings", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "dzchickenwings.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "A Dozen Chickenwings!"},
	["fcocacola"] 					= {["name"] = "fcocacola", 			 			["label"] = "Fountain Cocacola", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "fdrink.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fountain CocaCola - Hopefully it doesnt taste like water!"},
	["fsprite"] 					= {["name"] = "fsprite", 			 	 		["label"] = "Fountain Sprite", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "fdrink.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fountain Sprite - Hopefully it doesnt taste like water!"},
	["fnestea"] 					= {["name"] = "fnestea", 			 			["label"] = "Fountain Nestea", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "fdrink.png", 				["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fountain Nestea - Hopefully it doesnt taste like water!"},	
	["fcup"] 						= {["name"] = "fcup", 			 				["label"] = "Fountain Drink Cup", 		["weight"] = 100, 		["type"] = "item", 		["image"] = "fcup.png", 				["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Fountain Cup for drinks!"},
	["pizzasupplies"] 				= {["name"] = "pizzasupplies", 			 	 	["label"] = "Supplies for LS Pizza", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "pizzasupplies.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Box full of supplies for LS Pizza!"},

```
## Consumables for qb-smallresources/consumables.lua (Client, Config and Server)
# Config.lua under Consumeables = 
```lua
    --- 710-pizza 
    ["pepcalzone"] = math.random(30, 50),
    ["dzchickenwings"] = math.random(30, 50),
    ["chcalzone"] = math.random(20, 50),
    ["slcheesepizza"] = math.random(30, 40),
    ["slpeppizza"] = math.random(20, 40),
    ["slhawapizza"] = math.random(35, 40),
    ["slmexpizza"] = math.random(35, 54),
    ["slchickenpizza"] = math.random(30, 50),
    ["slbbqpizza"] = math.random(35, 54),
    ["slveggiepizza"] = math.random(35, 54),
    ["fcocacola"] = math.random(30, 50),
    ["fsprite"] = math.random(30, 50),
    ["fnestea"] = math.random(20, 50),
```
# Client 
```lua 
RegisterNetEvent("consumables:client:openPizzaBox")
AddEventHandler("consumables:client:openPizzaBox", function(itemName)
    TriggerEvent('animations:client:EmoteCommandStart', {"UNCUFF"})
    QBCore.Functions.Progressbar("drink_something", "Opening Pizza box..", 5000, false, true, {
        disableMovement = false,
        disableCarMovement = false,
		disableMouse = false,
		disableCombat = true,
    }, {}, {}, {}, function() -- Done
        TriggerEvent("inventory:client:ItemBox", QBCore.Shared.Items[itemName], "remove")
        TriggerEvent('animations:client:EmoteCommandStart', {"c"})
    end)
end)
```
# Server 
```lua 
--- Start of 710-pizza stuff ---
QBCore.Functions.CreateUseableItem("fcocacola", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("fsprite", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)

QBCore.Functions.CreateUseableItem("fnestea", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Drink", source, item.name)
    end
end)
--- food --- 
QBCore.Functions.CreateUseableItem("slcheesepizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("slpeppizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("slhawapizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("slmexpizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("slchickenpizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("slbbqpizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("slveggiepizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("chcalzone", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("dzchickenwings", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
QBCore.Functions.CreateUseableItem("pepcalzone", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent("consumables:client:Eat", source, item.name)
    end
end)
--- pizza boxes 
QBCore.Functions.CreateUseableItem("cheesepizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slcheesepizza", 6)
    end
end)
QBCore.Functions.CreateUseableItem("peppizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slpeppizza", 6)
    end
end)
QBCore.Functions.CreateUseableItem("phawapizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slhawapizza", 6)
    end
end)
QBCore.Functions.CreateUseableItem("pmexpizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slmexpizza", 6)
    end
end)
QBCore.Functions.CreateUseableItem("chickenpizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slchickenpizza", 6)
    end
end)
QBCore.Functions.CreateUseableItem("bbqpizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slbbqpizza", 6)
    end
end)
QBCore.Functions.CreateUseableItem("veggiepizza", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        Player.Functions.AddItem("slveggiepizza", 6)
    end
end)

```