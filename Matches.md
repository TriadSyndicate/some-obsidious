Collections - matches
- inclusion of injuries, penalties, extra-time match_events
`matches:{`
`competition_id - ObjectId ref competition,`
`home_team - ObjectId ref child-team,`
`away_team - ObjectId ref child-team,`
`date - datetime Object,`
`venue - String,`
`home_stats - Array of objects *match_stats*,`
`away_stats - Array with match_stats,`
`data_entered - Boolean,`
`formation - Object of Home Team and Away Team as strings // formation, 4-3-3 [dropdownList on the frontend]`
`match_events - Array with match_event`,
`video - Array of String AWS video codes`,
`documents - Array of Links to documents stored on storage server like scoresheets etc`
`}`


`match_stats:{`
`match_id - ObjectId ref match,`
`player_id - ObjectId ref ghost_player_id,`
`starter - Boolean,`
`min_played - int,`
`goals - Array of goal, goal_minute,`
`assists - int,`
`yellow_cards - int,` 
`red_cards - int,`
`own_goals - int`
`}`

`match_event:{`
`event_type - String,`
`event_type_data_object - Object with specific event *// yellow_card, red_card, own_goal, goal_with_assist, goal_no_assist, penalty, injuries, extra-time*`
`player_id - ObjectId ref ghost_player_id,`
`match_id - ObjectId ref match,`
`minute - int`
`}`
**common attr [minute, player_id, extra-time]**
`yellow_card_event:{`
`double_yellow - Boolean,`
`minute - int,`
`yellow_card - Boolean,`
`player_id - ObjectId ref ghost_player,`
`extratime - Boolean`
`}`

`red_card:{`
`red_card - Boolean,`
`extratime - Boolean`
`}`

`own_goal:{`
`own_goal: Boolean,`
`extratime - Boolean`
`}`

`goal_with_assist:{`
`goal - Boolean,`
`assisted - Boolean,`
`assisterId - ObjectId ref ghost_player,`
`scorerId - ObjectId ref ghost_player,`
`extratime - Boolean`
`}`

`goal_no_assist:{`
`goal - Boolean,`
`assisted - Boolean,`
`extratime - Boolean`
`}`

`penalty:{`
`penalty - Boolean,`
`scorerId - ObjectId ref ghost_player,`
`extratime - Boolean`
`}`

`injury:{`
`injured - Boolean,`
`injured_player_id - ObjectId ref ghost_player,`
`extratime - Boolean`
`}`