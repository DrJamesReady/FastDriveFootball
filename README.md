# FastDriveFootball
Enhancement utilities to the Fast Drive Football (https://www.fastdrivefootball.com/) cards and dice Game developed by 3dGaming (https://3d6-gaming.store/). The purpose of this repository is to provide tools for the game player and provide enhancements  to add 'immersive flavor' to the game experience.

## Team Card Card Maker
A single-file HTML tool for making printable team cards for the tabletop game Fast Drive Football. Open the file in any modern browser, fill in each team’s card, and print to PDF on card stock. There is nothing to install, no server and no login.

### What it does
_Six cards per sheet_. Cards print on US Letter landscape with dashed cut lines. Add as many sheets as your league needs.
_Pull-down menus for team qualities_. Each card has 7 offense and 6 defense quality slots, KR/PR ratings, Front Office and Head Coach grades, and Ownership Qualities. Semi (•) and super (double-underlined) forms are supported.
_Scoring designator_. Click the OFFENSE label to set [P], [R], [P+] or [R+].
_Color shading_. Positive qualities show green and negative ones pink, on screen and optionally in print.
_League branding_. Set the league/season label once and it appears on every card. You can add one league logo, which is scaled to fit and centered on each card. Each team’s name color is saved as hex and RGB.
_Save and share leagues_. Work auto-saves in your browser. Export the whole league, including the logo, as JSON and load it later or share it. Older files load unchanged.

### How to use it
Download FDF_Team_Card_Maker_1_013.html and open it in a browser.
Set the league/season label and, if you like, add a logo.
Fill in each team’s card with the pull-down menus.
Print: Ctrl/⌘+P → Save as PDF → Landscape → Letter → Margins None → Scale 100%.

## Team Matcher
A single-file HTML helper for Fast Drive Football players. Describe a team's strengths and weaknesses using the game's quality tags, and the tool ranks every NFL team-season from 1999 to 2025 by how closely it fits that profile. No install, no server, no build step: download `fdf_team_matcher_v1_1.html` and open it in a browser.

### What it does

**Team Matcher tab**
- Set 13 qualities (7 offense, 6 defense) to Full, Semi, Average, Semi negative
  or Full negative, e.g. PROLIFIC / DULL for points per game.
- See the 5 closest historical team-seasons, each with its record, points for and
  against, and a match %.
- Adjust the weight on the qualities you listed, and limit the range of seasons.

**League tab**
- Load a `.json` file exported from the Team Card Maker.
- Get a league list with the league name and each team's listed qualities, plus its
  closest historical matches (1, 3 or 5 per team).

### How matching works

Every statistic is ranked within its own season, so each team is compared only
with its own league year. Your chosen tier for each quality maps to a target
percentile, and each season is scored by its weighted distance from that target.
Qualities you set above or below Average count more heavily, controlled by the
"Weight on listed qualities" slider (x1 to x4). The distance is converted to a
match %.

