# ads_engagement_active()

*Find the video advertisement status.*

### Supported Game Maker Language

`Game Maker Language 2`

## Description

Some ad providers, for example Supersonic and AdColony, have interstitial advertisements that can take the form of an "offer wall" (essentially a page to promote several different advertising campaigns) or a video where virtual currency is rewarded to the player, so it's important to know when one of these adverts is being shown. This function will return true if such an ad is currently active or false if it is not.

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

## Examples

#### Example 1

> Check to see if there is already an advertisement active, if there is no then launch an advertisement

```
if(! ads_engagement_active()) {
  if(ads_engagement_available()) {
    ads_engagement_launch();
  }
}
```