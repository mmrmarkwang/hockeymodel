# NHL grip reference study — 2026-09-20

## References inspected

- Connor McDavid action photo on his Elite Prospects profile: https://www.eliteprospects.com/player/183442/connor-mcdavid
  Photo viewed in-browser: https://files.eliteprospects.com/layout/players/d7d24-img-2664.png
  Visible left-shot example: right hand at the butt end, left hand below; flexed elbows and knees, hands in front of the torso. The photograph is an action moment, not a universal neutral stance.
- NHL Seattle Kraken, *When Left is Right*: https://www.nhl.com/kraken/news/when-left-is-right-317014698
  MacKinnon photo inspected for contrasting handedness and extended reach; not used as a neutral-pose template.
- USA Hockey, *10U+: PVC Pipe Stickhandling*: https://www.usahockey.com/news_article/show/791982-10u-pvc-pipe-stickhandling
  Top hand controls the shaft with a firmer grip; bottom hand stays loose; arms remain free of the torso and wrists roll.
- USA Hockey, *Puck Handling — Expansion of Reach*: https://mobilecoach.usahockey.com/USAH/Drill0048/pg00001.html
  Lower-hand sliding changes reach, so one fixed hand spacing is insufficient for gameplay animations.

## Previous model errors

Closing four fingers alone did not establish a hockey grip. The previous procedural gloves used the same longitudinal thumb arrangement for both hands; top-hand end placement and cuff/forearm orientation were not based on an observed hockey reference. Two rigid closed grips also do not model the lower hand's sliding role.

## Revised static prototype

`hockey-reference-grip.blend` is a left-shot version with right hand at the shaft butt, left hand lower, and a visible butt-end knob. The top glove's longitudinal orientation is reversed relative to the bottom glove so the thumb/index side and little-finger side are distinguished. The stick is on the player's left side, and lower grip placement is checked against arm reach without stretching. Spacing and glove geometry are design approximations, not measurements extracted from the photo.

This is a reference-informed revision, not a claim of NHL technique validation. Remaining work includes anatomical glove/finger refinement, forearm twist weights, lower-hand sliding IK, wrist roll and forehand/backhand blade control. The blade remains a simple blockout and is not a modeled left-shot curve. Earlier files are retained for comparison.
