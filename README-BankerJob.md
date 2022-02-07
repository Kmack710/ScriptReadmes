
███████╗░░███╗░░░█████╗░░░░░░░██████╗░░█████╗░███╗░░██╗██╗░░██╗███████╗██████╗░░░░░░██╗░█████╗░██████╗░  ██████╗░██╗░░░██╗
╚════██║░████║░░██╔══██╗░░░░░░██╔══██╗██╔══██╗████╗░██║██║░██╔╝██╔════╝██╔══██╗░░░░░██║██╔══██╗██╔══██╗  ██╔══██╗╚██╗░██╔╝
░░░░██╔╝██╔██║░░██║░░██║█████╗██████╦╝███████║██╔██╗██║█████═╝░█████╗░░██████╔╝░░░░░██║██║░░██║██████╦╝  ██████╦╝░╚████╔╝░
░░░██╔╝░╚═╝██║░░██║░░██║╚════╝██╔══██╗██╔══██║██║╚████║██╔═██╗░██╔══╝░░██╔══██╗██╗░░██║██║░░██║██╔══██╗  ██╔══██╗░░╚██╔╝░░
░░██╔╝░░███████╗╚█████╔╝░░░░░░██████╦╝██║░░██║██║░╚███║██║░╚██╗███████╗██║░░██║╚█████╔╝╚█████╔╝██████╦╝  ██████╦╝░░░██║░░░
░░╚═╝░░░╚══════╝░╚════╝░░░░░░░╚═════╝░╚═╝░░╚═╝╚═╝░░╚══╝╚═╝░░╚═╝╚══════╝╚═╝░░╚═╝░╚════╝░░╚════╝░╚═════╝░  ╚═════╝░░░░╚═╝░░░

██╗░░██╗███╗░░░███╗░█████╗░░█████╗░██╗░░██╗███████╗░░███╗░░░█████╗░░░░██╗░██╗░░█████╗░███████╗░░███╗░░░█████╗░
██║░██╔╝████╗░████║██╔══██╗██╔══██╗██║░██╔╝╚════██║░████║░░██╔══██╗██████████╗██╔══██╗╚════██║░████║░░██╔══██╗
█████═╝░██╔████╔██║███████║██║░░╚═╝█████═╝░░░░░██╔╝██╔██║░░██║░░██║╚═██╔═██╔═╝██║░░██║░░░░██╔╝██╔██║░░██║░░██║
██╔═██╗░██║╚██╔╝██║██╔══██║██║░░██╗██╔═██╗░░░░██╔╝░╚═╝██║░░██║░░██║██████████╗██║░░██║░░░██╔╝░╚═╝██║░░██║░░██║
██║░╚██╗██║░╚═╝░██║██║░░██║╚█████╔╝██║░╚██╗░░██╔╝░░███████╗╚█████╔╝╚██╔═██╔══╝╚█████╔╝░░██╔╝░░███████╗╚█████╔╝
╚═╝░░╚═╝╚═╝░░░░░╚═╝╚═╝░░╚═╝░╚════╝░╚═╝░░╚═╝░░╚═╝░░░╚══════╝░╚════╝░░╚═╝░╚═╝░░░░╚════╝░░░╚═╝░░░╚══════╝░╚════╝░

█▀▄ █ █▀ █▀▀ █▀█ █▀█ █▀▄ ---  https://discord.gg/qpem5er64U 
█▄▀ █ ▄█ █▄▄ █▄█ █▀▄ █▄▀ 
### KNOWN "ERRORS"
- If the boss menu account doesnt have enough it will say "attempt to compare string with a number" to "fix" this change this event in qb-bossmenu to look like this 
- This Error is caused by the extra check to see if account will go negitive so this will allow your companies to go negitive.
### IF USING OKOKBANKING dont do this instead replace it with event below in OPTIONAL 
```lua
RegisterServerEvent("qb-bossmenu:server:removeAccountMoney")
AddEventHandler("qb-bossmenu:server:removeAccountMoney", function(account, amount)
    print(account.."- Account    Amount ---"..amount)
    if not Accounts[account] then
        Accounts[account] = 0
    end
   --[[if Accounts[account] >= amount then
        Accounts[account] = Accounts[account] - amount
    end]]
    Accounts[account] = Accounts[account] - amount
    TriggerClientEvent('qb-bossmenu:client:refreshSociety', -1, account, Accounts[account])
    SaveResourceFile(GetCurrentResourceName(), "./accounts.json", json.encode(Accounts), -1)
end)
```

███████████████████████████████████████████████████████████████████████████
█▄─▄▄▀█▄─▄▄─█▄─▄▄─█▄─▄▄─█▄─▀█▄─▄█▄─▄▄▀█▄─▄▄─█▄─▀█▄─▄█─▄▄▄─█▄─▄█▄─▄▄─█─▄▄▄▄█
██─██─██─▄█▀██─▄▄▄██─▄█▀██─█▄▀─███─██─██─▄█▀██─█▄▀─██─███▀██─███─▄█▀█▄▄▄▄─█
▀▄▄▄▄▀▀▄▄▄▄▄▀▄▄▄▀▀▀▄▄▄▄▄▀▄▄▄▀▀▄▄▀▄▄▄▄▀▀▄▄▄▄▄▀▄▄▄▀▀▄▄▀▄▄▄▄▄▀▄▄▄▀▄▄▄▄▄▀▄▄▄▄▄▀
- oxmysql(v1.9.0+) - https://github.com/overextended/oxmysql/releases
- QBCore of course as thats all I make scripts for! :)  
- qb-bossmenu - For paying companies/banker job. Option in config if you changed name to 710-bossmenu for example
- qb-input - for the menus for banker and paying loans 
- qb-menu - for the menus for bankers UI and pay Loan 


OPTIONAL (Options in configs) -- SEE OPTIONAL section below.
-okokBanking (with events you need to add provided below) - https://okok.tebex.io/package/4724937
-okokNotify (with 'loans' noti provided below to add to config) - https://okok.tebex.io/package/4724993

██████████████████████████████████████████ ██████████████████ ███████████████████████████████████ ██████████████████████████████
█▄─▄▄─█▄─▀─▄█▄─▄▄─█─▄▄─█▄─▄▄▀█─▄─▄─█─▄▄▄▄█ █▄─▄▄─█─▄▄─█▄─▄▄▀█ █─▄▄▄─█▄─▄▄▀█▄─▄▄─█▄─▄▄▀█▄─▄█─▄─▄─█ █─▄▄▄▄█─▄▄▄─█─▄▄─█▄─▄▄▀█▄─▄▄─█
██─▄█▀██▀─▀███─▄▄▄█─██─██─▄─▄███─███▄▄▄▄─█ ██─▄███─██─██─▄─▄█ █─███▀██─▄─▄██─▄█▀██─██─██─████─███ █▄▄▄▄─█─███▀█─██─██─▄─▄██─▄█▀█
▀▄▄▄▄▄▀▄▄█▄▄▀▄▄▄▀▀▀▄▄▄▄▀▄▄▀▄▄▀▀▄▄▄▀▀▄▄▄▄▄▀ ▀▄▄▄▀▀▀▄▄▄▄▀▄▄▀▄▄▀ ▀▄▄▄▄▄▀▄▄▀▄▄▀▄▄▄▄▄▀▄▄▄▄▀▀▄▄▄▀▀▄▄▄▀▀ ▀▄▄▄▄▄▀▄▄▄▄▄▀▄▄▄▄▀▄▄▀▄▄▀▄▄▄▄▄▀
## Can be used anywhere to raise/lower credit score! SERVER SIDE ONLY. 
```lua
--- INCREASE/RAISE credit score export be called from other scripts to incease wherever.
exports["710-banking"]:increaseCreditScore(citizenid, amount)
--- example below increases their credit score by 500 
exports["710-banking"]:increaseCreditScore(citizenid, 500)

--- DECREASE/LOWER credit score export be called from other scripts to decrease wherever.
exports["710-banking"]:decreaseCreditScore(citizenid or job, amount)
-- Example below lowers their credit score by 500 
exports["710-banking"]:decreaseCreditScore("realestate", 5000)
```
████████████████████████████████████████████████ ████████████ ███████████████████████████
█▄─▄▄▀█▄─▄▄─█─▄▄▄─█▄─██─▄█▄─▄█▄─▄▄▀█▄─▄▄─█▄─▄▄▀█ █─▄─▄─█─▄▄─█ █▄─▀█▀─▄██▀▄─██▄─█─▄█▄─▄▄─█
██─▄─▄██─▄█▀█─██▀─██─██─███─███─▄─▄██─▄█▀██─██─█ ███─███─██─█ ██─█▄█─███─▀─███─▄▀███─▄█▀█
▀▄▄▀▄▄▀▄▄▄▄▄▀───▄▄▀▀▄▄▄▄▀▀▄▄▄▀▄▄▀▄▄▀▄▄▄▄▄▀▄▄▄▄▀▀ ▀▀▄▄▄▀▀▄▄▄▄▀ ▀▄▄▄▀▄▄▄▀▄▄▀▄▄▀▄▄▀▄▄▀▄▄▄▄▄▀
████████████████████████████████████████████████████████████████
█─▄▄▄▄█─▄▄▄─█▄─▄▄▀█▄─▄█▄─▄▄─█─▄─▄─█ █▄─█▀▀▀█─▄█─▄▄─█▄─▄▄▀█▄─█─▄█
█▄▄▄▄─█─███▀██─▄─▄██─███─▄▄▄███─███ ██─█─█─█─██─██─██─▄─▄██─▄▀██
▀▄▄▄▄▄▀▄▄▄▄▄▀▄▄▀▄▄▀▄▄▄▀▄▄▄▀▀▀▀▄▄▄▀▀ ▀▀▄▄▄▀▄▄▄▀▀▄▄▄▄▀▄▄▀▄▄▀▄▄▀▄▄▀
### ADD TO YOUR SQL DATABASE 
```sql
CREATE TABLE `banker_loans` (
    `citizenid` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8_general_ci',
    `loantype` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8_general_ci',
    `loan_amount` INT(11) NULL DEFAULT NULL,
    `loan_owing` INT(11) NULL DEFAULT NULL,
    `loan_officer` VARCHAR(50) NULL DEFAULT NULL COLLATE 'utf8_general_ci',
    `loan_info` VARCHAR(255) NULL DEFAULT NULL COLLATE 'utf8_general_ci',
    `loan_id` INT(11) AUTO_INCREMENT,
    `lastpayment` DATETIME NULL DEFAULT NULL,
    PRIMARY KEY (`loan_id`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
AUTO_INCREMENT=15
;

CREATE TABLE `banker_creditscore` (
    `citizenid` VARCHAR(50) NOT NULL COLLATE 'utf8_general_ci',
    `creditscore` SMALLINT(6) NULL DEFAULT NULL,
    PRIMARY KEY (`citizenid`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;

``` 
``` lua ### BOSSMENU 
['banker'] = vector3(263.69, 209.05, 110.29)
```
## Items for shared/Items.lua
```lua 
["banktablet"]                      = {["name"] = "banktablet",                 ["label"] = "Banker Tablet",                        ["weight"] = 500,           ["type"] = "item",      ["image"] = "missiontablet.png",        ["unique"] = true,      ["useable"] = true,     ["shouldClose"] = true,     ["combinable"] = nil,               ["description"] = "A Secure Tablet for Bankers!"},
    ['bankinvoice']                  = {['name'] = 'bankinvoice',                   ['label'] = 'Bank Invoice',             ['weight'] = 0,         ['type'] = 'item',      ['image'] = 'stickynote.png',           ['unique'] = true,      ['useable'] = false,    ['shouldClose'] = false,   ['combinable'] = nil,   ['description'] = 'Invoice from the bank'},
```
### TO MAKE BANKINVOICE SHOW DETAILS ADD THIS TO inventory/html/app.js Under stickynote around LN 606 
```js
} else if (itemData.name == "bankinvoice") {
            $(".item-info-title").html("<p>" + itemData.label + "</p>");
            $(".item-info-description").html('<p><strong>Total Loan Amount: </strong><span>' + itemData.info.loanamount + '</span></p><p><strong>Type of Loan: </strong><span>' + itemData.info.loantype + '</span></p>');
```
## So it should look like this after 
```js
} else if (
            itemData.info.costs != undefined &&
            itemData.info.costs != null
        ) {
            $(".item-info-title").html("<p>" + itemData.label + "</p>");
            $(".item-info-description").html("<p>" + itemData.info.costs + "</p>");
        } else if (itemData.name == "stickynote") {
            $(".item-info-title").html("<p>" + itemData.label + "</p>");
            $(".item-info-description").html("<p>" + itemData.info.label + "</p>");
        } else if (itemData.name == "bankinvoice") {
            $(".item-info-title").html("<p>" + itemData.label + "</p>");
            $(".item-info-description").html('<p><strong>Total Loan Amount: </strong><span>' + itemData.info.loanamount + '</span></p><p><strong>Type of Loan: </strong><span>' + itemData.info.loantype + '</span></p>');
        } else if (itemData.name == "moneybag") {

```
## JOB 
```lua
['banker'] = {
        label = 'Pacific Standard Bank',
        defaultDuty = true,
        offDutyPay = false,
        grades = {
            ['0'] = {
                name = 'Teller',
                payment = 50
            },
            ['1'] = {
                name = 'Supervisor',
                payment = 75
            },
            ['2'] = {
                name = 'Guard',
                payment = 100
            },
            ['3'] = {
                name = 'Broker',
                payment = 125
            },
            ['4'] = {
                name = 'Manager',
                isboss = true,
                payment = 150
            },
        },
    },
```

███████████████████████████████████████████████
█─▄▄─█▄─▄▄─█─▄─▄─█▄─▄█─▄▄─█▄─▀█▄─▄██▀▄─██▄─▄███--- I DIDNT CHANGE qb- HERE SO IF YOU CHANGE YOUR NAMES CHANGE THEM BEFORE YOU COPY PASTA 
█─██─██─▄▄▄███─████─██─██─██─█▄▀─███─▀─███─██▀█--- Simple banking option below okok option 
▀▄▄▄▄▀▄▄▄▀▀▀▀▄▄▄▀▀▄▄▄▀▄▄▄▄▀▄▄▄▀▀▄▄▀▄▄▀▄▄▀▄▄▄▄▄▀
###OPTIONAL  OKOK NOTIFY 
```lua 
loans = {
        highlightColor = 'blue',
        icon = 'cash-stack'
    },
```

## OPTIONAL for if you have okokbanking and want okokBanking to handle all your qb-bossmenu add/remove money events 
# in qb-bossmenu look for these events delete the old 2 events and add these instead 
# this will make all old bossmenu calls work but send them to okok intead!
```lua
RegisterServerEvent("qb-bossmenu:server:addAccountMoney")
AddEventHandler("qb-bossmenu:server:addAccountMoney", function(account, amount, note)
    if note ~= nil then 
        note = note 
    else 
        note = "Business Income"
    end
    local societyName = QBCore.Shared.Jobs[account].label
    local society = "society_"..account
    TriggerEvent('okokBanking:DepositMoneyToSocietyAccount', amount, society, societyName, note)
end)

RegisterServerEvent("qb-bossmenu:server:removeAccountMoney")
AddEventHandler("qb-bossmenu:server:removeAccountMoney", function(account, amount, note)
    if note ~= nil then 
        note = note 
    else 
        note = "Business Debit"
    end
    local societyName = QBCore.Shared.Jobs[account].label
    local society = "society_"..account
    TriggerEvent("okokBanking:WithdrawMoneyToSocietyAccount", amount, society, societyName, note)
end)
```
# And then add this anywhere on server.lua for okokBanking (Pref all the way at the bottom.)
```lua 
RegisterNetEvent("okokBanking:DepositMoneyToSocietyAccount")
AddEventHandler("okokBanking:DepositMoneyToSocietyAccount", function(amount, society, societyName, note)
    MySQL.query('UPDATE okokBanking_societies SET value = value + @value WHERE society = @society AND society_name = @society_name', {
        ['@value'] = amount,
        ['@society'] = society,
        ['@society_name'] = societyName,
    }, function(changed)
    end)
    TriggerEvent('okokBanking:AddDepositTransactionToSocietyB', amount, society, societyName, note)
end)

RegisterNetEvent("okokBanking:WithdrawMoneyToSocietyAccount", function(amount, society, societyName, note)
    MySQL.query('UPDATE okokBanking_societies SET value = value - @value WHERE society = @society AND society_name = @society_name', {
        ['@value'] = amount,
        ['@society'] = society,
        ['@society_name'] = societyName,
    }, function(changed)
    end)
    TriggerEvent('okokBanking:AddWithdrawTransactionToSocietyB', amount, society, societyName, note)
end)

RegisterServerEvent("okokBanking:AddDepositTransactionToSocietyB")
AddEventHandler("okokBanking:AddDepositTransactionToSocietyB", function(amount, society, societyName, note)
    MySQL.query('INSERT INTO okokBanking_transactions (receiver_identifier, receiver_name, sender_identifier, sender_name, date, value, type) VALUES (@receiver_identifier, @receiver_name, @sender_identifier, @sender_name, CURRENT_TIMESTAMP(), @value, @type)', {
        ['@receiver_identifier'] = society,
        ['@receiver_name'] = note,
        ['@sender_identifier'] = "The bank",
        ['@sender_name'] = 'Bank',
        ['@value'] = tonumber(amount),
        ['@type'] = 'deposit'
    }, function (result)
    end)
end)

RegisterServerEvent("okokBanking:AddWithdrawTransactionToSocietyB")
AddEventHandler("okokBanking:AddWithdrawTransactionToSocietyB", function(amount, society, societyName, note)
    MySQL.query('INSERT INTO okokBanking_transactions (receiver_identifier, receiver_name, sender_identifier, sender_name, date, value, type) VALUES (@receiver_identifier, @receiver_name, @sender_identifier, @sender_name, CURRENT_TIMESTAMP(), @value, @type)', {
        ['@receiver_identifier'] = "The bank",
        ['@receiver_name'] = "Bank",
        ['@sender_identifier'] = society,
        ['@sender_name'] = note,
        ['@value'] = tonumber(amount),
        ['@type'] = 'withdraw'
    }, function (result)
    end)
end)
```
### SIMPLE BANKING -- server-customize is set up to use this event by default if you put custom into the bank option 
## Add this to Simple banking/lua/server/sv_society.lua 
```lua
RegisterNetEvent('qb-banking:society:server:WithdrawMoneyLoan')
AddEventHandler('qb-banking:society:server:WithdrawMoneyLoan', function(amount, account)

    if not a then return end
    if not n then return end

    local s = GetSociety(n)
    local sMoney = tonumber(s.money)
    local amount = tonumber(a)
    local withdraw = sMoney - amount 

    local setter = MySQL.Sync.fetchAll("UPDATE society SET money =  ? WHERE name = ?", {withdraw, n})
    -- local setter = exports.oxmysql:execute("UPDATE society SET money =  ? WHERE name = ?", {withdraw, n})
end)

RegisterServerEvent('qb-banking:society:server:DepositMoneyLoan')
AddEventHandler('qb-banking:society:server:DepositMoneyLoan', function(amount, account)

    if not a then return end
    if not n then return end

    local s = GetSociety(n)
    local sMoney = tonumber(s.money)
    local amount = tonumber(a)
    local deposit = sMoney + amount

    
    local setter = MySQL.Sync.fetchAll("UPDATE society SET money =  ? WHERE name = ?", {deposit, n})
    -- local setter = exports.oxmysql:execute("UPDATE society SET money =  ? WHERE name = ?", {deposit, n})
end)
```