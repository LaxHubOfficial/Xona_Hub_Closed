local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
   Name = "Xona Hub - Closed ❌",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Xona Hub - Closed ❌",
   LoadingSubtitle = "by SuPraa006",
   ShowText = "Xona", -- for mobile users to unhide rayfield, change if you'd like
   Theme = "Amethyst", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   ToggleUIKeybind = "K", -- The keybind to toggle the UI visibility (string like "K" or Enum.KeyCode)

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = true, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "5nN3XkrhHt", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ ABCD would be ABCD
      RememberJoins = false -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Xona Key",
      Subtitle = "Key System",
      Note = "Discord.", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Xona728438Abx"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local Tab = Window:CreateTab("❌ Xona hub has been closed ❌", 4483362458) -- Title, Image

local Paragraph = Tab:CreateParagraph({Title = "Bad news", Content = "We are sorry to inform you but the script is now closed, we will open it later 1 or 2 days. key for acces is in discord for devlopers"})


local Button = Tab:CreateButton({
   Name = "Launch Beta vertion",
   Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/LaxHubOfficial/Xona_Hub_Beta/refs/heads/main/README.md",true))()
   end,
})
