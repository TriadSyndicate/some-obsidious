collections - mainPlayer, ghostPlayer inclusion of contracts and injuries as well as parent team and child team affiliations
`main-player:{`
`name - String,`
`real_dob - Date Object,`
`nationality - Array of CountryIds`
`stats - Object (ref Stats)`
`parent_teams - Array of TeamObjects {reg_date, parent_team_id, end_date, contract_type},`
`matches - Array of MatchIds,`
`foot - String,`
`positions - Array // List of positions`
`gender -  String,`
`performance - Obj ref Perf,`
`ghost_player_ids - Array GhostPlayerIds,`
`injuries - Array of injuryObjects`
`}`

`ghost-player:{`
`main_player_id - ref ObjectId main-player,`
`fake_dob - Date Object,`
`child_team - Team Object {reg_date, child_team_id, end_date, contract_type}`
`jersey_num - Int`
`Video - String`
`Stats - ref Stats Objects`
`Matches - array of child team matches`
`performance - Object Ref Perf,`
`}`

`stats:{`
`match_day_squad - int,`
`starter - int,`
`min_played - int,`
`starter_minutes - int,`
`sub_minutes - int,`
`goals - int,`
`assists - int,`
`yellow_cards - int,`
`red_cards - int,`
`own_goals - int,`
`clean_sheets - int`
`}`

`performance :{`
`team_matches - int,`
`appearances - int,`
`matches_started - int,`
`mins - int,`
`mins_90 - Decimal,`
`percent_matches - Decimal,`
`percent_potential_mins - Decimal,`
`goals - int,`
`goals_per_90 - Decimal,`
`mins_per_goal - Decimal,`
`penalties - int,`
`assists - int,`
`assists_per_90 - Decimal,`
`goal_contributions - int,`
`goal_contributions_per_90 - Decimal,`
`conceded - int,`
`conceded_per_90 - Decimal,`
`clean_sheets - int,`
`}`

`PlayerTeamsObject :{`
`team_id - ObjectId,`
`reg_date - date object,`
`end_date - date object,`
`contractType - String,`
`on_team - Boolean,`
`}`

```
injuryObject:{
date_of_injury - Date Object,
type_of_injury - String,
status - String // Back in training, Recovering, Recovered, Unknown
recovery_date - Date Object
}
```