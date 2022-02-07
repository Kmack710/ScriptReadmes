### 710-Rosin for QBCore! - Made by Kmack710 
## Dependancies 
# QBCore -- https://github.com/qbcore-framework
# nh-contextmenu -- https://github.com/nerohiro/nh-context
# bt-target or qb-target (option in config) -- https://github.com/BerkieBb/qb-target 
# Map was changed a bit if you didnt get it with the download you can get it here might have a few more updates to it soon so be sure to watch in discord :)- https://drive.google.com/file/d/1NV8UN21a9P5oFzWRkpWNeBmk2LXy2w78/view?usp=sharing
# Original map credits - https://www.gta5-mods.com/maps/mlo-druglab
# Map edit credits (adding rosin press and fixing collisions) - Tony2#7210
## Join Discord for updates or to give me new script Ideas! - https://discord.gg/qpem5er64U


## For Shared.lua 
```lua 
-- 710-rosin items
	["godfatherog"] 				= {["name"] = "godfatherog", 			 	  	["label"] = "God Father OG", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "godfatherog.png", 			["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "AAAA God Father OG! - Would be great to make some Rosin out of!"},
	["godfatherrosin"] 				= {["name"] = "godfatherrosin", 			 	["label"] = "God Father OG - Rosin", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "godfatherrosin.png", 		["unique"] = false, 	["useable"] = true, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "AAAA God Father OG Rosin!"},
	["rosincontainer"] 				= {["name"] = "rosincontainer", 			 	["label"] = "Rosin Container", 			["weight"] = 100, 		["type"] = "item", 		["image"] = "rosincontainer.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Empty Rosin container to put Rosin in!"},
	["weedfilterbag"] 				= {["name"] = "weedfilterbag", 			 	  	["label"] = "Filter Bag for Rosin", 	["weight"] = 100, 		["type"] = "item", 		["image"] = "weedfilterbag.png", 		["unique"] = false, 	["useable"] = false, 	["shouldClose"] = true,    ["combinable"] = nil,   ["description"] = "Weed Filter bag for making Rosin!"},
```
## For consumables.lua - CLIENT - For drug effect 
```lua 
RegisterNetEvent("consumables:client:UseRosin")
AddEventHandler("consumables:client:UseRosin", function()
    QBCore.Functions.Progressbar("smoke_joint", "Hitting Dab..", 2000, false, true, {
        disableMovement = false,
        disableCarMovement = false,
		disableMouse = false,
		disableCombat = true,
    }, {}, {}, {}, function() -- Done
        local playerPed = PlayerId()
        TriggerEvent("inventory:client:ItemBox", QBCore.Shared.Items["godfatherrosin"], "remove")
        if IsPedInAnyVehicle(PlayerPedId(), false) then
            TriggerEvent('animations:client:EmoteCommandStart', {"smokeweed"})
            Wait(8000)
            TriggerEvent('animations:client:EmoteCommandStart', {"c"})
            ClearPedTasksImmediately(playerPed)
            SetTimecycleModifier("spectator6")
            SetPedMotionBlur(playerPed, true)
            SetPedMovementClipset(playerPed, "MOVE_M@DRUNK@VERYDRUNK", true)
            SetPedIsDrunk(playerPed, true)
            AnimpostfxPlay("ChopVision", 10000001, true)
            ShakeGameplayCam("DRUNK_SHAKE", 1.0)
            SetEntityHealth(playerPed, 200)
            Citizen.Wait(10000) --- Time your high for 
            SetPedMoveRateOverride(playerPed, 1.0)
            SetRunSprintMultiplierForPlayer(playerPed, 1.0)
            SetPedIsDrunk(playerPed, false)		
            SetPedMotionBlur(playerPed, false)
            ResetPedMovementClipset(playerPed)
            AnimpostfxStopAll()
            ShakeGameplayCam("DRUNK_SHAKE", 0.0)
            SetTimecycleModifierStrength(0.0)
            TriggerServerEvent('cosmo_hud:Server:RelieveStress', math.random(15, 30))
        else
            TriggerEvent('animations:client:EmoteCommandStart', {"bong"})
            Wait(8000)
            TriggerEvent('animations:client:EmoteCommandStart', {"c"})
            ClearPedTasksImmediately(playerPed)
            SetTimecycleModifier("spectator6")
            SetPedMotionBlur(playerPed, true)
            SetPedMovementClipset(playerPed, "MOVE_M@DRUNK@VERYDRUNK", true)
            SetPedIsDrunk(playerPed, true)
            AnimpostfxPlay("ChopVision", 10000001, true)
            ShakeGameplayCam("DRUNK_SHAKE", 1.0)
            SetEntityHealth(playerPed, 200)
            Citizen.Wait(10000) --- Time your high for 
            SetPedMoveRateOverride(playerPed,1.0)
            SetRunSprintMultiplierForPlayer(playerPed,1.0)
            SetPedIsDrunk(playerPed, false)		
            SetPedMotionBlur(playerPed, false)
            ResetPedMovementClipset(playerPed)
            AnimpostfxStopAll()
            ShakeGameplayCam("DRUNK_SHAKE", 0.0)
            SetTimecycleModifierStrength(0.0)
            TriggerServerEvent('cosmo_hud:Server:RelieveStress', math.random(15, 30))
        end
        TriggerEvent("evidence:client:SetStatus", "weedsmell", 300)
    end)
end)
```
## Consumables.lua server  
```lua
QBCore.Functions.CreateUseableItem("godfatherrosin", function(source, item)
    local Player = QBCore.Functions.GetPlayer(source)
	if Player.Functions.RemoveItem(item.name, 1, item.slot) then
        TriggerClientEvent('consumables:client:UseRosin', source)
    end
end)
```