# Data Flow Summary

## Old Models

### Player Model
- **Inputs:** Player information such as name, date of birth, nationality, etc.
- **Outputs:** Player data stored in the database.

### Team Model
- **Inputs:** Team name, roster of players, match information, competition information.
- **Outputs:** Team data stored in the database.

### Match Model
- **Inputs:** Match details including competition ID, home and away teams, date, venue, etc.
- **Outputs:** Match data stored in the database.

### Fixture Model
- **Inputs:** Fixture details such as competition ID, competition year, fixture type, stages, etc.
- **Outputs:** Fixture data stored in the database.

### Body Model
- **Inputs:** Body details like name, competitions, national competitions, etc.
- **Outputs:** Body data stored in the database.

## New Models

### Main Player Model
- **Inputs:** Player information such as name, date of birth, nationality, performance stats, etc.
- **Outputs:** Main player data stored in the database.

### Ghost Player Model
- **Inputs:** Main player ID, fake date of birth, team information, performance stats, etc.
- **Outputs:** Ghost player data stored in the database.

### Parent Team Model
- **Inputs:** Parent team name, on-contract players, category, child teams, linked country, etc.
- **Outputs:** Parent team data stored in the database.

### Child Team Model
- **Inputs:** Child team name, type, roster, past players, competitions, matches, etc.
- **Outputs:** Child team data stored in the database.

### Stage Model
- **Inputs:** Stage name, matchups.
- **Outputs:** Stage data stored in the database.

### Subcategory Model
- **Inputs:** Subcategory name.
- **Outputs:** Subcategory data stored in the database.

## Data Flow Relationships

- Player data can be associated with teams through roster assignments.
- Team data can be associated with matches and competitions.
- Match data can be associated with fixtures and competitions.
- Fixture data can be associated with competitions and stages.
- Body data can be associated with competitions and national competitions.
- Main player data can be associated with ghost player data through the main player ID.
- Parent team data can be associated with child team data.
- Child team data can be associated with matches, competitions, and subcategories.
- Stage data can be associated with matches.
- Subcategory data can be associated with child teams.


### Old Model
                         +-----------+
                         |   Team    |
                         +-----------+
                               |
                               |
                     +-------------------+
                     |   Competition    |
                     +-------------------+
                               |
                      +---------------------+
                      |         Match       |
                      +---------------------+
                               |
                      +-------------------+
                      |       Fixture      |
                      +-------------------+
                               |
                     +---------------------+
                     |         Body        |
                     +---------------------+


### New Model

                         +---------------------+
                         |     ParentTeam      |
                         +---------------------+
                                  |
                     +---------------------------+
                     |          ChildTeam        |
                     +---------------------------+
                               |
                     +-----------------------------+
                     |        MainPlayer            |
                     +-----------------------------+
                                  |
                     +---------------------------+
                     |         GhostPlayer        |
                     +---------------------------+
