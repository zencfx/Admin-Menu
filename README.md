# Setting Up `zAdmin`
- Make Sure To Have [Overextended Library](https://github.com/overextended/ox_lib) Resource, Start It Before Admin Menu
- In The `fxmanifest.lua` of `zAdmin` Make Sure Its The Right SQL
- In The `config.lua` At The Top Put Your Framework. 

**First in the `config.lua` you will need to configure these options! Also anything else in the config!**
```lua
    Server = {
        Name = "Zen Development",
        Discord = "discord.gg/zdev",
        Tebex = "zdev.tebex.io",
        RGB = { 0, 128, 255 }
    },
```


# Permissions
```lua
Permissions = {
    GroupAces = {
        ['group.admin'] = {'owner', 'immune', 'gotobring', 'ban', 'kick'}, -- add in here their perms which are found below
        ['group.manager'] = {'gotobring', 'ban', 'kick'},
    },

    AllPerms = { -- Add Any Identifier, Make Sure Linked To Player
        'discord:000000000000000000'
    }
}
```
**Admin Permissions**
- kick, ban, gotobring, revive, clearinventory, clearloadout, spectate, freeze, clearchat, unban, entitywipe, spawnvehicle, repairvehicle, cleanvehicle, flipvehicle, healtharmour, godmode, invisibility, noclip, giveweapon, givemoney, giveitem, setjob, teleport, changeskin, staffchat, announce, gangcreator, immune

**Group Permissions** (basically what menu title is)
- moderator, administrator, developer, management, owner

# How To Setup Ace Perms With Discord
- If you do not already have these setup!
- [DiscordAcePerms](https://github.com/JaredScar/DiscordAcePerms) | [Badger_Discord_API](https://github.com/JaredScar/Badger_Discord_API)
- Setup [Tutorial](https://www.youtube.com/watch?v=81Of9tZRQjw) That I Found On YouTube

# Discord Server Logs
- There are logs for almost everything!
- Video on creating a [Webhook](https://www.youtube.com/watch?v=K8vgRWZnSZw)

```lua
DiscordLogs = {
    SpectatePlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    FreezePlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    BanPlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    UnbanPlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    OfflineBanPlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    KickPlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    ClearLoadout = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    ClearInventory = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    RevivePlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    GotoBringPlayer = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    OpenInventory = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    EntityWipe = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    ForceSkin = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    ClearChat = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    SpawnVehicle = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    HealthArmour = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    Invisiblity = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    Godmode = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    GiveWeapon = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    GiveMoney = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    GiveItem = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    Setjob = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
    PlayerReports = 'https://discord.com/api/webhooks/0000000000000000/webhookid',
}
```

# Whitelisting
- Not all Vehicles, Weapons, Items can be spawned/given. Only whitelisted ones!

**Below You Can See How Simple It Is To Setup!**
```lua
    Whitelisted = { 
        Weapons = {
            {label = 'AP Pistol', spawncode = 'weapon_appistol'},
            {label = 'Combat Pistol', spawncode = 'weapon_combatpistol'},
            {label = 'Special Carbine', spawncode = 'weapon_specialcarbine'},
            {label = 'Switch Blade', spawncode = 'weapon_switchblade'}
        },

        Items = {
            {label = 'Armour', item = 'armour'},
            {label = 'MedKit', item = 'medkit'},
            {label = 'Repair Kit', item = 'repairkit'}
        },

        Vehicles = {
            {label = 'Manchez', spawncode = 'manchez'},
            {label = 'Blista', spawncode = 'blista'},
            {label = 'Hydra', spawncode = 'hydra'}
        },
    },
```
