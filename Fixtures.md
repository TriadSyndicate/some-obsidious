Collections - fixtures
- Fixtures and fixture types with dynamic stages
- ability to change fixture stages individually, as well as order 

`fixtures:{`
`competition_id - ObjectId ref competition,`
`competition_year - String,`
`fixture_type - String, // tournament type just for the records eg. tournament || league || knockout`
`stages - Array of Objects of stage`
`}`

`stage:{`
`name - String // name of stage like knockout round, matchday 1, round 1`
`matchups - Array of ObjectIds ref Matches,`
`}`

