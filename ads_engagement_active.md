# ads_engagement_active()

*Find the video advertisement status.*

### Supported Game Maker Language
`Game Maker Language 2`

## Syntax

```
bool ads_engagement_active();
```

## Arguments

```
N/A
```

## Returns

boolean

## Description

Some ad providers, for example Supersonic and AdColony, have interstitial advertisements that can take the form of an "offer wall" (essentially a page to promote several different advertising campaigns) or a video where virtual currency is rewarded to the player, so it's important to know when one of these adverts is being shown. This function will return true if such an ad is currently active or false if it is not.

## Examples

#### Example 1

*code checks to see if there is currently and interstitial ad active and if not, then it will check to see if one is available and that the variable "show" returns true. If both conditions are met, an interstitial ad will be launched and the variable set to false, so that when the add is finished the check will take the player to the next room.*
```
if(! ads_engagement_active()) {
  if(ads_engagement_available() && show) {
    ads_engagement_launch();
    show = false;
  } else {
    room_goto(rm_MainMenu);
  }
}
```