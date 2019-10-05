# ads_engagement_launch()

*Launch an interstitial video/offerwall.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

Some ad providers, for example Supersonic and AdColony, have interstitial advertisements that can take the form of an "offer wall" (essentially a page to promote several different advertising campaigns) or a video where virtual currency is rewarded to the player. If such an advert is available, this function can be used to launch it at a specific moment within your game.

## Syntax

```
void ads_engagement_launch();
```

## Arguments

```
N/A
```

## Returns

N/A

## Examples

#### Example 1

> The above code checks to see if there is currently and interstitial ad active and if not, then it will check to see if one is available and that the variable "show" returns true. If both conditions are met, an interstitial ad will be launched and the variable set to false, so that when the add is finished the check will take the player to the next room.

```
if(!ads_engagement_active()) {
  if(ads_engagement_available() && show) {
      ads_engagement_launch();
      show = false;
   } else {
      room_goto(rm_MainMenu);
   }
}
```