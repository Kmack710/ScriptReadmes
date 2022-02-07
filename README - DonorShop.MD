## █▀▄ █▀█ █▄ █ █▀█ █▀█ 	█▀▀ █▄█ █▀█ █▀█ 	 
## █▄▀ █▄█ █ ▀█ █▄█ █▀▄ 	▄██ █ █ █▄█ █▀▀ 

## █▄▄ ▀▄▀ 	█▄▀ █▄ ▄█ ▄▀▄ █▀▀ █▄▀
## █▄█  █  	█ █ █ ▀ █ █▀█ █▄▄ █ █
# Dependencies
# QBCore 
# nh-context (Most updated version for pictures)
# qb-target 
# qb-vehiclekeys (Can reach out to me if you have something else we can impliment it)

### █▄█ █▀█ █ █ █ 	▀█▀ █▀█ 	▄▀▄ █▀▄ █▀▄ 	█▀▀ ▄▀▄ █▀█ █▀▀ 
### █ █ █▄█ ▀▄▀▄▀ 	 █  █▄█ 	█▀█ █▄▀ █▄▀ 	█▄▄ █▀█ █▀▄ ▄██ 
# Goto your Shared/vehicles.lua and either do method 1 or method 2 listed below depending on if your cars are already added to that file 
## 𝗠𝗘𝗧𝗛𝗢𝗗 𝗢𝗡𝗘 - The Already on the shared/vehicles.lua 
# Its actually VERY simple is what you want to do is set the "shop" to whatever Config.donorCarShopName is - "donorshop" by default 
# THEN TO GET A PICTURE add this line to the bottom of that car under ['shop']
```lua
['url'] = 'https://i.redd.it/df1sqybb15e71.png', --- Insert any picture link that ends in .png or .jpeg 
```
# This line under is what adds the picture to the menu - Dont worry it wont effect your other stores! :) 
## 𝗠𝗘𝗧𝗛𝗢𝗗 𝗧𝗪𝗢 -- ADDING NEW CARS 
## its really just like adding any car to your server below is an example but its basically method 1 just copy and paste then edit the feilds 

```lua
['911r'] = {							
	['name'] = 'Porsche 911R',
	['brand'] = 'Porsche',
	['model'] = '911r',
	['price'] = 15, -- This price is in donorcoin as long as shop = donorshop
	['category'] = 'super',                           
	['hash'] = `911r`,
	['shop'] = 'donorshop',
	['url'] = 'https://i.redd.it/df1sqybb15e71.png', --- Picture is OPTIONAL if you dont want them and just want the menu you can leave this out
},
```

### ▀█▀ █▀█	  █   ▀█▀ █▄ █ █▄▀ 	█ █ █ ▀█▀ ▀█▀ █▄█ 	▀█▀ █▀▀ █▄▄ █▀▀ ▀▄▀ 
###  █  █▄█   █▄▄ ▄█▄ █ ▀█ █ █ 	▀▄▀▄▀ ▄█▄  █  █ █  	 █  ██▄ █▄█ ██▄ █ █ 
## 1- Goto your tebex store and link your DATABASE - https://docs.tebex.io/store/integrating-with-your-game-server-or-website/mysql
## 2 -When you add a new package that gives "donor coin" you MUST add this line (Step3) in each package under that database server you just made above! 
## 3- For this line below 30 is the example of amount of donor coin being given.
```sql
INSERT INTO `710donor_tebex` VALUES ('{transaction}', '30', '0', NULL);
```
## 4 - Tell your donors to use their Tebex ID to redeem ingame with /redeem 
## Goto the donor shop and Enjoy :) 
### 𝗜𝗙 𝗬𝗢𝗨 𝗔𝗥𝗘 𝗛𝗔𝗩𝗜𝗡𝗚 𝗧𝗥𝗢𝗨𝗕𝗟𝗘𝗦 𝗪𝗜𝗧𝗛 𝗧𝗛𝗜𝗦 𝗥𝗘𝗔𝗗 𝗛𝗢𝗪 𝗧𝗢 𝗠𝗔𝗞𝗘 𝗦𝗤𝗟 𝗔𝗖𝗖𝗢𝗨𝗡𝗧 𝗕𝗘𝗟𝗢𝗪

### █▄█ █▀█ █ █ █ 	▀█▀ █▀█ 	█▄ ▄█ ▄▀▄ █▄▀ █▀▀ 	 
### █ █ █▄█ ▀▄▀▄▀  	 █  █▄█ 	█ ▀ █ █▀█ █ █ ██▄ 	
### ▄▀▄ 	█▀▀ █▀█  █   	▄▀▄ █▀▀ █▀▀ █▀█ █ █ █▄ █ ▀█▀
### █▀█ 	▄██ █▄▀▄ █▄▄ 	█▀█ █▄▄ █▄▄ █▄█ █▄█ █ ▀█  █ 
# So this can be different for everyone but Im going to give you 3 ways to make an account if you havent yet.
# before we start this SQL account allows you to connect to your database from outside the server itself.
# So when you are making this account be sure to use a SECURE username and password.
# Once you have done this you could also log in from your home PC to your database via a program like HeidiSQL 
### ▀█▀ █▄ ▄█ █▀█ █▀█ █▀█ ▀█▀ ▄▀▄ █▄ █ ▀█▀ 𝗔𝗟𝗟 𝗦𝗧𝗘𝗣𝗦 𝗕𝗘𝗟𝗢𝗪 𝗪𝗛𝗘𝗡 𝗔𝗦𝗞𝗘𝗗 𝗙𝗢𝗥 𝗛𝗢𝗦𝗧 𝗢𝗥 𝗜𝗣 
### ▄█▄ █ ▀ █ █▀▀ █▄█ █▀▄  █  █▀█ █ ▀█  █  ** 𝗔𝗟𝗪𝗔𝗬𝗦 𝗣𝗨𝗧 % 𝗡𝗢𝗧 𝗔𝗡𝗬 𝗜𝗣 ***

## 𝗠𝗘𝗧𝗛𝗢𝗗 𝗢𝗡𝗘 -- Mainly for linux servers but also works for Windows servers running Wampserver and a few others.
# 1- Open chrome/firefox/whatever browser you use (on your server computer) and goto this site or just click this - http://localhost/
# 1.a - Sometimes you need to put a port after so if that doesnt work try http://localhost:80  -- Thats just one example it could be - 81, 8888, 443 also.
# 2- make the browser full screen look for user accounts then click create new account then make the info you want 

## 𝗠𝗘𝗧𝗛𝗢𝗗 𝗧𝗪𝗢 -- Honestly I probably should of made this Method 1 but oh well here is the EASY way :) 
# 1 - Open your Database however you normally would (Hopefully locally) and go to run a query / SQL file like you normally would.
# 2- Either Copy and paste the below SQL code into your Query section and run it OR if you have no idea what im talking about 2.a. **If you know what im talking about skip to 2.b**
# 2.a - Look in the Readme Folder For RUNMEFORANEWACCOUNT.SQL - 𝗜𝗧𝗦 𝗩𝗘𝗥𝗬 𝗜𝗠𝗣𝗢𝗥𝗧𝗔𝗡𝗧 𝗧𝗛𝗔𝗧 𝗬𝗢𝗨 𝗢𝗣𝗘𝗡 𝗔𝗡𝗗 𝗘𝗗𝗜𝗧 𝗧𝗛𝗜𝗦 𝗙𝗜𝗟𝗘!
# 2.b - Once you have the file/query open/ready you will see I have filled it out with placeholders, This is what you want YOUR account to be. 

```sql
CREATE USER 'YOUR_DESIRED_USERNAME_HERE'@'%' IDENTIFIED BY 'PASSWORD_YOU_WANT_TO_PICK_HERE';
GRANT ALL PRIVILEGES ON *.* TO 'YOUR_DESIRED_USERNAME_HERE'@'%';
FLUSH PRIVILEGES;
```
## 𝗠𝗘𝗧𝗛𝗢𝗗 𝗧𝗛𝗥𝗘𝗘 --- For HeidiSQL Users 
# 1 - Look for the little 2 people icon near the refresh Icon and under the Goto menu. 
# 2 - Click that Icon then click +Add 
# 3 - Pick a username then pick "connect from anywhere"
# 4 - Make a Password and repeat it.
# 5 - Make sure to give global perms if you dont want to give full perms just make sure it can drop, update and create tables within your RP servers database. 

## If you still dont have it figured out after these 3 steps check out youtube on how to make and link a SQL account :) 