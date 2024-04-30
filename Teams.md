Collections - mainTeam, childTeam, Category, subCategory, Countries, Territories
- linked main-team to specific country ObjectId
`main-team:{`
`name - String,`
`on_contract_players - Array of main-playerIds,`
`category - ObjectId ref category,`
`child-teams - Array of childteamIds,`
`linked_country - ObjectId of Country document`
`}`

`child-team:{`
`name - String,`
`type - ObjectId ref subCategory,`
`roster - Array of ghost_player_ids,`
==`**comps - Array of competitionIds //old version with compsIds`==
`}`

`category:{`
`name - String, // Club, national`
`}`
`subCategory:{`
`name - String, // u17, U21`
`}`

`countries:{`
`name - String of Country,`
`countryCode - String of Country Code`
`}`

`territories:{`
`name - String of specified region,`
`countries - Array of countries ObjectId`
`}`

- Bodies, sub-bodies, teams registered to bodies
- country bodies and regional bodies
- Territories x WAFU - westAfrica, East Africa, Africa
- Bodies to countries
- 