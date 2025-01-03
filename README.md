#================================================================================================================================
# Loot Filter - for Path of Exile 2
#================================================================================================================================

# Welcome to Isallonda's Lootfilter!

# This filter is designed for general mapping. You can change or delete any special categories you don’t need. 
# The "special shows" are set for my Deadeye build with Dualstring Bow and Visceral Quiver, plus valuable white items like Headhunter or Atramentis.

#=================================================================================================================================

# To hide something, just change Show to Hide (capitalize the H).

# Yellow items are only shown as Expert bases. 
# Magic items are only shown for jewelry, mage wands, scepters, etc. 
# You can adjust the gold amount by changing both numbers in the filter.

# Colors are based on RGB values. Google an RGB picker to adjust colors to your liking.

# To remove beams or map icons, delete the "PlayEffect" or "minimapicon" sections.

# Waystones are shown from tier 10 upwards. If you want to show them at lower tiers, just change "Hide" to "Show" for levels you want to be shown.

#===============================================================================================================================

# Need help or want to give feedback? DM me in POE2: Isallonda#6132.

# Thanks for using my filter!  May your loot be plentiful, your map runs smooth, and your adventures full of sparkles. Stay sane Exiles! <3

# May your loot be plentiful, your map runs smooth, and your Exile adventures full of sparkles. Stay sane (and loot crazy)! <3

#===============================================================================================================================


#---------------------------------------------------------------------------------
# Special shows 
#---------------------------------------------------------------------------------

# White Bases for Chance Orbs

Show
Class "Rings" "Amulets" "Belts"
BaseType  "Stellar" "Heavy" "Gold" "Prismatic" "Amethyst" "Sapphire" "Solar" "Breach"
SetBorderColor 0 240 190 170
Rarity = Normal
SetTextColor 255 255 255 200
SetBackgroundColor 179 2 96 255
PlayEffect Pink


#Crafting Base for your build - Ranger

#Put everything in here what you like to be special highlighted with an Purple beam (color can be changed -> just change the name at playeffect)

Show
Class "Bow"
BaseType "Expert Dualstring Bow"
SetBorderColor 255 255 0 170
SetBackgroundColor 0 0 0 170
PlayEffect Purple

Show
Class "Quiver"
BaseType "Visceral Quiver" 
SetBorderColor 255 255 255 170
SetBackgroundColor 0 0 0 170
PlayEffect Purple

#---------------------------------
# Uniques and High Valuable Currency
#---------------------------------

Show
Rarity Unique
SetTextColor 175 96 37 255
SetBorderColor 175 96 37 255
SetBackgroundColor 53 13 13 255
PlayAlertSound 3 300
PlayEffect Brown
MinimapIcon 1 Brown Star
SetFontSize 40

## Divine Orb Style
Show
Class "Currency"
BaseType "Mirror" "Divine" "Perfect Jeweller's Orb"
SetFontSize 45
SetTextColor 255 0 0 255
SetBorderColor 255 0 0 255
SetBackgroundColor 255 255 255 255
PlayAlertSound 6 300
PlayEffect Red
MinimapIcon 0 Red Star

Show
BaseType == "Distilled Isolation" "Distilled Suffering"
SetFontSize 45
SetTextColor 255 0 0 255
SetBorderColor 255 0 0 255
SetBackgroundColor 255 255 255 255
PlayAlertSound 6 300
PlayEffect Red
MinimapIcon 0 Red Star


#---------------------------------
# Gold - can be set to another stack size, just change the number at both "StackSize"
#---------------------------------

Hide
BaseType == "Gold"
StackSize <= 1000
SetFontSize 32
SetTextColor 128 108 0 255
SetBorderColor 255 255 255 0


Show
BaseType == "Gold"
StackSize >= 1000
SetFontSize 32
SetTextColor 128 108 0 255
SetBorderColor 255 255 255 0


#---------------------------------
# Uncut Gems
#---------------------------------

# Always make Spirit gems pop
Show
BaseType "Uncut Spirit Gem"
SetTextColor 20 240 240
SetBorderColor 20 240 240
PlayAlertSound 2 300
PlayEffect Cyan
MinimapIcon 1 Cyan Triangle
SetFontSize 34

# Make support gems pop during leveling
Show
AreaLevel < 68
BaseType "Uncut Support Gem"
SetTextColor 20 240 240
SetBorderColor 20 240 240
PlayAlertSound 2 300
PlayEffect Cyan
MinimapIcon 1 Cyan Triangle
SetFontSize 34

# Make skill gems pop during leveling
Show
AreaLevel < 65
BaseType "Uncut Skill Gem"
SetTextColor 20 240 240
SetBorderColor 20 240 240
PlayAlertSound 2 300
PlayEffect Cyan
MinimapIcon 1 Cyan Triangle
SetFontSize 34

# Gems up to level 17 in maps don't get shown
Show
BaseType "Uncut Skill Gem"
ItemLevel = 18
SetTextColor 20 240 240
SetBorderColor 20 240 240
PlayAlertSound 2 300
PlayEffect Cyan
MinimapIcon 1 Cyan Triangle
SetFontSize 34

Show
BaseType "Uncut Skill Gem"
ItemLevel = 19
SetTextColor 20 240 240
SetBorderColor 20 240 240
PlayAlertSound 2 300
PlayEffect Cyan
MinimapIcon 1 Cyan Triangle
SetFontSize 34

Show
BaseType "Uncut Support Gem"
SetTextColor 20 240 240
SetBorderColor 20 240 240
SetFontSize 30

# Gem Level 20 in maps get a special highlight (Divine worth)
Show
BaseType "Uncut Skill Gem"
ItemLevel = 20
SetFontSize 42
SetTextColor 255 0 0 255
SetBorderColor 255 0 0 255
SetBackgroundColor 255 255 255 255
PlayAlertSound 6 300
PlayEffect Red
MinimapIcon 0 Red Star

Hide
ItemLevel <= 17
BaseType "Uncut Skill Gem"
SetTextColor 20 240 240
SetBorderColor 20 240 240
SetFontSize 40


Show
BaseType "Uncut Skill Gem"
SetTextColor 20 240 240
SetBorderColor 20 240 240
PlayAlertSound 2 300
PlayEffect Cyan
MinimapIcon 1 Cyan Triangle
SetFontSize 40

#---------------------------------
# Socketables and Special Equipment
#---------------------------------

# Special A Tier - Specific socketables and jewels
Show 
BaseType "Soul Core" "Timeless"
SetTextColor 0 240 190
SetBorderColor 0 240 190
SetFontSize 45
MinimapIcon 0 Cyan Diamond
PlayAlertSound 2 300
PlayEffect Cyan

# Special Highlight - Breach Rings
Show 
Rarity Rare
BaseType == "Breach Ring"
SetTextColor 0 240 190
SetBorderColor 0 240 190
SetFontSize 40
MinimapIcon 1 Cyan Diamond
PlayEffect Cyan
PlayAlertSound 2 300

Show 
Rarity <= Magic
BaseType == "Breach Ring"
SetTextColor 0 240 190
SetFontSize 35
MinimapIcon 2 Cyan Diamond
PlayEffect Cyan Temp

# Special A Tier - Sanctum Relics
Show 
Class "Relic"
SetTextColor 0 240 190
SetBorderColor 0 240 190
SetFontSize 40
MinimapIcon 1 Cyan Diamond
PlayAlertSound 2 300
PlayEffect Green

# Special A Tier - Rare Jewels
Show
Class "Jewel"
Rarity <= Rare
SetTextColor 0 240 190
SetBorderColor 0 240 190
SetFontSize 40
MinimapIcon 1 Cyan Diamond
PlayEffect Cyan
PlayAlertSound 2 300

# Special B Tier - Any Runes and Charms - All are hidden (besides iron runes), when you want them to show change Hide into Show

Show
BaseType "Iron Rune" 
SetTextColor 0 240 190
PlayEffect Cyan Temp

Hide
BaseType " Rune" 
SetTextColor 0 240 190
PlayEffect Cyan Temp

Hide
BaseType "Charm"
SetTextColor 0 240 190
PlayEffect Cyan Temp

#---------------------------------
# Scroll of Wisdom hidden while mapping
#---------------------------------

Hide
BaseType "Scroll of Wisdom"


#---------------------------------
# Differrent Currencies
#---------------------------------

# Currency Tier A: Gemcutter, Annullment
Show
Class "Currency"
BaseType "Orb of Annulment" "Orb of Chance" "Greater Jeweller's Orb" "Distilled Fear" "Distilled Despair"
SetTextColor 255 255 255 255
SetBorderColor 255 255 255 255
SetBackgroundColor 240 90 35
PlayAlertSound 1 300
PlayEffect White
MinimapIcon 1 Orange Star
SetFontSize 45

# Currency Tier B: Exalt
Show
Class "Currency"
BaseType "Exalted Orb" "Chaos Orb"
SetTextColor 255 255 255 255
SetBorderColor 255 255 255 255
SetBackgroundColor 240 90 35
PlayAlertSound 1 300
PlayEffect Orange
MinimapIcon 1 Orange Star
SetFontSize 45

Show
BaseType "Gold Key" "Silver Key" "Bronze Key"
SetTextColor 255 207 132
SetBorderColor 255 207 132
SetBackgroundColor 76 51 12
PlayAlertSound 2 300
PlayEffect White
MinimapIcon 2 White Circle
SetFontSize 40

# Currency Tier B: Regal, Vaal 
Show
Class "Currency"
BaseType "Gemcutter's Prism" "Vaal Orb" "Lesser Jeweller's Orb" "Regal Orb" "Artificer's Orb" "Glassblower's Bauble" "Orb of Alchemy"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetBackgroundColor 213 162 45 255
PlayAlertSound 2 300
PlayEffect White
MinimapIcon 1 Yellow Circle
SetFontSize 38

Show
Class "Currency"
BaseType "Simulacrum Splinter"
SetFontSize 36
SetTextColor 50 50 50 255
SetBorderColor 50 50 50 255
SetBackgroundColor 249 150 25 255
PlayAlertSound 2 300
PlayEffect Yellow

Show
Class "Currency"
BaseType "Greater Essence of "
SetFontSize 45
SetTextColor 0 50 255
SetBorderColor 0 50 255
SetBackgroundColor 249 150 25 255
PlayAlertSound 1 300
PlayEffect Orange

Show
Class "Currency"
BaseType " of Torment" " of Ruin" " of Haste" " of Electricity" 
SetFontSize 40
SetTextColor 0 50 255
SetBorderColor 0 50 255
SetBackgroundColor 249 150 25 255
PlayAlertSound 1 300
PlayEffect Orange
MinimapIcon 1 Orange Raindrop


Show
Class "Currency"
BaseType " of the Body" " of the Mind" " of Enhancement" " of the Infinite" " of Flames" " of Ice" " of Battle" " of Sorcery"
SetFontSize 32
SetTextColor 0 50 255
SetBorderColor 0 50 255
SetBackgroundColor 249 150 25 255
PlayAlertSound 2 300
PlayEffect Yellow

Show
Class "Currency"
BaseType "Catalyst" "Flesh" "Carapace" "Adaptive" "Xoph's" "Tul's" "Esh's" "Uul-Netol's" "Reaver" "Sibilant" "Chayula's" "Skittering" "Neural"
SetFontSize 30
SetTextColor 128 0 128 255
SetBackgroundColor 227 158 44 210


Show
Class "Currency"
BaseType "Breach Splinter" 
SetFontSize 38
SetTextColor 128 0 128 255
SetBorderColor 128 0 128 255
SetBackgroundColor 249 150 25 255
PlayAlertSound 2 300
MinimapIcon 1 Purple Circle

Show
Class "Omen"
BaseType "Omen of"
SetTextColor 255 207 132
SetBorderColor 255 207 132
SetBackgroundColor 76 51 12
PlayAlertSound 2 300
PlayEffect White
MinimapIcon 2 White Circle
SetFontSize 40

Show
Class "Currency"
BaseType "Distilled"
SetTextColor 255 207 132
SetBorderColor 255 207 132
SetBackgroundColor 76 51 12
PlayAlertSound 2 300
PlayEffect White
MinimapIcon 2 White Circle
SetFontSize 40


# Currency Tier C: Armourer scrap, whetstone

Show
Class "Currency"
BaseType "Arcanist's Etcher" "Armourer's Scrap" "Blacksmith's Whetstone" 
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetBackgroundColor 189 159 10 255
PlayAlertSound 2 300
PlayEffect White
SetFontSize 36

Show
Class "Currency"
BaseType "Orb of Augmentation" "Orb of Transmutation" "Regal Shard" "Chance Shard"
SetTextColor 220 190 132
MinimapIcon 2 Grey Circle
SetFontSize 35

Hide
Class "Currency"
BaseType "Scroll of Wisdom" "Shard"


Show
Class "Pinnacle Keys"
SetFontSize 42
SetTextColor 255 0 0 255
SetBorderColor 255 0 0 255
SetBackgroundColor 255 255 255 255
PlayAlertSound 6 300
PlayEffect Red
MinimapIcon 0 Red Star

Show
BaseType "Tablet" 
SetTextColor 100 100 100
SetBorderColor 255 207 255
SetBackgroundColor 255 255 255
PlayAlertSound 2 300
SetFontSize 40

Show
BaseType "Simulacrum" "Breachstone" "Cowardly Fate" "Deadly Fate" "Victorious Fate" "Test of"
SetTextColor 255 207 255
SetBorderColor 255 207 255
SetBackgroundColor 65 20 80
PlayAlertSound 2 300
PlayEffect Purple
MinimapIcon 1 Purple Square
SetFontSize 45


Show
Class "Currency"
BaseType "Broken Circle Artifact" "Black Scythe" "Order Artifact" "Sun Artifact" 
SetFontSize 36
SetTextColor 255 207 255
SetBorderColor 255 207 255
SetBackgroundColor 65 20 80
PlayAlertSound 2 300
PlayEffect Purple Temp

Show
Class "Currency"
BaseType "Exotic Coinage"
SetFontSize 40
SetTextColor 255 255 255
SetBorderColor 255 207 255
SetBackgroundColor 136 66 178
PlayAlertSound 2 300
PlayEffect Purple Temp

Show
BaseType "Expedition Logbook"
SetFontSize 40
SetTextColor 255 207 255
SetBorderColor 255 207 255
SetBackgroundColor 65 20 80
PlayAlertSound 1 300
PlayEffect Purple Temp
MinimapIcon 1 Orange UpsideDownHouse

Show
BaseType "Barya" "Ultimatum"
SetTextColor 255 255 255
SetBorderColor 255 207 255
SetBackgroundColor 56 194 47
PlayAlertSound 2 300
PlayEffect Grey
MinimapIcon 1 Grey Square
SetFontSize 34

#---------------------------------
# Waystones - waystones shown tier 10 or higher (if you want to change this just change "hide" into "Show"
#---------------------------------
Hide
WaystoneTier 1
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 2
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 3
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 4
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 5
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 6
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 7
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 8
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Hide
WaystoneTier 9
BaseType "Waystone"
SetTextColor 255 255 255
SetBorderColor 255 255 255
SetFontSize 30

Show
BaseType "Waystone"
WaystoneTier > 10
SetTextColor 255 255 255
SetBorderColor 255 255 255
PlayAlertSound 4 300
PlayEffect White
MinimapIcon 1 White Square
SetFontSize 36

#---------------------------------
# Value Rares
#---------------------------------

Show
Class "Rings" "Amulets" "Belts"
BaseType  "Stellar" "Heavy" "Gold" "Prismatic" "Amethyst" "Sapphire" "Solar" "Breach"
Rarity Rare
SetTextColor 233 206 75
SetBorderColor 233 206 75
PlayEffect Purple

Show
Class "Rings" "Amulets" "Belts"
Rarity Rare
SetFontSize 40
SetTextColor 233 206 75
SetBorderColor 233 206 75

#---------------------------------
# Rings, Amulets, Belts
#---------------------------------

Show
Class "Rings" "Amulets" "Belts"
BaseType  "Gold" "Amethyst" "Solar" "Breach" 
Rarity Magic
SetTextColor 225 225 225 255
SetBackgroundColor 27 91 213 255
PlayEffect Purple

Show
Class "Rings" "Amulets" "Belts"
Rarity Magic
SetFontSize 36

Show
Class "Rings" "Amulets" "Belts"
BaseType "Ruby Ring" "Sapphire Ring" "Topaz Ring" "Prismatic"
Rarity Normal
SetFontSize 38
PlayEffect Blue

Hide 
Class "Rings" "Amulets" "Belts"
BaseType "Unset" "Lazuli" "Iron" "Pearl" "Emerald" "Jade" "Crimson" "Azure" "Lunar" "Amber" "Lapis" "Rawhide" "Utility" "Fine" "Linen" "Wide" "Long" "Plate" "Ornate" "Mail" "Double" 
Rarity Normal

#---------------------------------
# Salvagable Items
#---------------------------------

Show
Sockets > 1
Rarity Normal
SetBorderColor 200 200 200
SetFontSize 35

Show
Quality > 10
Rarity Normal
SetBorderColor 200 200 200
SetFontSize 35
PlayEffect Yellow

Show
Sockets > 1
Rarity Magic
SetBorderColor 0 0 200
SetFontSize 35

Show
Quality > 10
Rarity Magic
SetBorderColor 0 0 200
SetFontSize 35
PlayEffect Yellow

#---------------------------------
# Random Rares
#---------------------------------

Hide
Class "Body" "Helmet" "Boots" "Gloves" "Shields" "Quiver" "Mace" "Staff" "Quarter" "Bow" "Crossbow" "Wand" "Sceptre" "Focus"
BaseType "Advanced"
Rarity = Normal
SetTextColor 255 255 255 200
SetBackgroundColor 0 0 0 170


Hide
Class "Body" "Helmet" "Boots" "Gloves" "Shields" "Quiver" "Mace" "Staff" "Quarter" "Bow" "Crossbow" "Wand" "Sceptre" "Focus"
BaseType "Advanced"
Rarity = Magic
SetTextColor 136 136 255 255
SetBackgroundColor 0 0 0 170


Hide
Class "Body" "Helmet" "Boots" "Gloves" "Shields" "Quiver" "Mace" "Staff" "Quarter" "Bow" "Crossbow" "Wand" "Sceptre" "Focus"
BaseType "Expert"
Rarity = Magic
SetTextColor 136 136 255 255
SetBackgroundColor 0 0 0 170


Hide
Class "Body" "Helmet" "Boots" "Gloves" "Shields" "Quiver" "Mace" "Staff" "Quarter" "Bow" "Crossbow" "Wand" "Sceptre" "Focus"
BaseType "Advanced"
Rarity = Rare
SetTextColor 255 255 119 225
SetBackgroundColor 0 0 0 170

#---------------------------------
# Optional Rules - just add # before the rules if you want them off
#---------------------------------

Hide
Class "Body" "Helmet" "Boots" "Gloves" "Shields" "Quiver" "Mace" "Bow" "Crossbow" "QuarterStaff"
Rarity = normal
SetTextColor 255 255 119 225
SetBackgroundColor 0 0 0 170

Hide
Rarity <= Magic
Class "Flasks" 
