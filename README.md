# Upcoming-Media-Card



<b>New Interactive Features! ⭐</b>
<br>
<p style="margin-top: 20px;"></p>
Note: &nbsp;Remember to clear your web browser cache if you can't get a new 
feature to work after upgrading to a new version.

<p style="margin-top: 40px;"></p>

### I. Collapse Filter

Group items with common attributes together, e.g., group&nbsp;&nbsp;<b><i>Unwatched</i></b>&nbsp;&nbsp;<img src="./images/Unwatched.png" alt="Unwatched" style="width: 20px; height: auto;">&nbsp;&nbsp;items first. The rest of the items can be collapsed/expanded:



<p align="center">
  <img src="./images/umc-expand-collapse-filter.gif" alt="Collapse Filter GIF" style="margin-bottom: -22px;">
</p>

#### Example YAML:
```yaml
title: TV
type: custom:upcoming-media-card
entity: sensor.recently_added_tv
image_style: fanart
collapse: flag=true
sort_by: number
enable_tooltips: true
```
By setting `collapse: flag=true`, items not yet watched are prioritized and grouped at the top. You can expand/collapse the rest of the items. Alternatively, you can specify, I.E., `collapse: 2` to collapse/expand everything after 2 items (regardless of what items are displayed).

Note: You can also leverage the new `sort_by` setting as a secondary sort method (season/episode) sort order.

<br>

### II. Clickable Links

Navigate directly to the respective TV episode, movie, game, etc. with a single click or touch! Made possible with the new `deep_link` attribute (supported in the following integrations): [sensor.plex_recently_added](https://github.com/custom-components/sensor.plex_recently_added), [sensor.radarr_upcoming_media](https://github.com/custom-components/sensor.radarr_upcoming_media), [sensor.sonarr_upcoming_media](https://github.com/custom-components/sensor.sonarr_upcoming_media), [steam-wishlist](https://github.com/boralyl/steam-wishlist), [epic_games](https://github.com/hudsonbrendon/ha_epic_games).


<p align="center">
  <img src="./images/umc-deep_link.gif" alt="Clickable Links GIF">
</p>

<br>

### III. Sorting

We can finally sort items by any attribute. `sort_by: airdate` will sort media items by their respective airdates. You can also reverse the sort order using `sort_ascending: false`.

<br>

### IV. General Filtering

Filter items by partial or full attribute value. `filter: flag=true`. Similar to `collapse:` setting, except discards the rest of the items.

<br>

### IV. Show & Movie Trailer Playback

When using `enable_trailers:true` setting, any item with a trailer attribute value will playback the respective video trailer when clicked or touched. Trailer playback will take precedence over deep_link hyperlinks.  Currently only _[plex_recently_added](https://github.com/custom-components/sensor.plex_recently_added)_, [sensor.sonarr_upcoming_media](https://github.com/custom-components/sensor.sonarr_upcoming_media), _[radarr_upcoming_media](https://github.com/custom-components/sensor.radarr_upcoming_media)_ and _[trakt](https://github.com/dylandoamaral/trakt-integration)_ integrations are compatible.  These integrations have <b>trailer</b> attributes defined in their sensors. &nbsp;_Note: Home Assistant Companion app requires you to enable "Autoplay videos" under Companion App settings._

<p align="center">
  <img src="./images/umc_trailers.gif" alt="Tooltips GIF">
</p>

<br>

### V. Tooltips

To enable tooltips, use `enable_tooltips: true`. To change the default delay, use I.E., `tooltip_delay: 2000` (default 750ms). For touchscreens, hold your finger down to see the tooltip. This feature was possible with the new `summary` attribute (supported in the following integrations): [sensor.plex_recently_added](https://github.com/custom-components/sensor.plex_recently_added), [sensor.radarr_upcoming_media](https://github.com/custom-components/sensor.radarr_upcoming_media), [sensor.sonarr_upcoming_media](https://github.com/custom-components/sensor.sonarr_upcoming_media).

<p align="center">
  <img src="./images/tooltips.gif" alt="Tooltips GIF">
</p>

<br>

### VI. Transparency Effect

Activate with `enable_transparency: true` for a transparent gradient effect instead of the default opaque gradient background.

<p align="left">
  <img src="image.png" alt="Transparency Effect Image">
</p>

<br>
<br>

<br>
<br>

| Poster View | Fan Art View
| ---- | ---- 
| <img src="https://i.imgur.com/tdSBZZQ.png" alt="Screenshot 1" width="298"> | <img src="https://i.imgur.com/hWAcUuS.png" alt="Screenshot 1" width="320"> 

**Requires a custom-component:**<br/>
This card will only work if you've installed one of the custom-component's below to feed it.

### Current custom-components for this card:

| Component |  Author |
|:---------------|----------:|
|[CouchPotato](https://github.com/youdroid/home-assistant-couchpotato)|[youdroid](https://github.com/youdroid)
|[Emby_Upcoming_Media](https://github.com/gcorgnet/sensor.emby_upcoming_media)|[gcorgnet](https://github.com/gcorgnet)
|[Kodi Recently Added](https://github.com/boralyl/kodi-recently-added)|[boralyl](https://github.com/boralyl)
|[Plex Recently Added](https://github.com/custom-components/sensor.plex_recently_added)|[mayker](https://github.com/maykar)
|[Radarr Upcoming Media](https://github.com/custom-components/sensor.radarr_upcoming_media)|[mayker](https://github.com/maykar)
|[Sonarr Upcoming Media](https://github.com/custom-components/sensor.sonarr_upcoming_media)|[mayker](https://github.com/maykar)
|[Trakt](https://github.com/dylandoamaral/trakt-integration)|[dylandoamaral](https://github.com/dylandoamaral)
|[Mylar](https://github.com/DarkSir23/sensor.mylar)|[DarkSir23](https://github.com/DarkSir23)
|[Lidarr Upcoming Media](https://github.com/JackJPowell/sensor.lidarr_upcoming_media)|[JackJPowell](https://github.com/JackJPowell)|
|[SickChill](https://github.com/youdroid/home-assistant-sickchill)|[youdroid](https://github.com/youdroid)
|[Steam Wishlist](https://github.com/boralyl/steam-wishlist)|[boralyl](https://github.com/boralyl)|
|[Epic Games](https://github.com/hudsonbrendon/ha_epic_games)|[hudsonbrendon](https://github.com/hudsonbrendon)|

### Issues
Read through these two resources before posting issues to GitHub or the forums.
* [troubleshooting guide](https://github.com/custom-cards/upcoming-media-card/blob/master/troubleshooting.md)
* [@thomasloven's lovelace guide](https://github.com/thomasloven/hass-config/wiki/Lovelace-Plugins).

## Installation:

* Install the custom component by following it's instructions.
* Install this card by copying `upcoming-media-card.js` to your `www/custom-lovelace/` folder. If you're copy/pasting the code always copy from raw files on github (button on top right when viewing code).
* Include it in its own folder like so: `www/custom-lovelace/upcoming-media-card/upcoming-media-card.js`

This goes into ui-lovelace.yaml under "resources:"

```
resources:
- url: /local/custom-lovelace/upcoming-media-card/upcoming-media-card.js?v=0.1.1
  type: js
```

This goes into one of your views under "cards:" in the same file

```
  - type: custom:upcoming-media-card
    entity: sensor.sonarr_upcoming_media
```

If you're not updating using [tracker-card](https://github.com/custom-cards/tracker-card) and/or [custom-updater](https://github.com/custom-components/custom_updater) be sure that you are adding to a version number at the end of your lovelace resources when you update your cards, like so:

```
resources:
- url: /local/custom-lovelace/upcoming-media-card/upcoming-media-card.js?v=0.1.2
  type: js
```

You may need to have `javascript_version: latest` in your `configuration.yaml` under `frontend:`.

## Options:

This card has many customization options, but none are required to use the card. The card is fully functional with minimal configuration, like the installation example above.

# Main Config:

|NAME|TYPE|DEFAULT|DESCRIPTION|
|-|-|-|-|
|type|string|**REQUIRED**|**`custom:upcoming-media-card`**|
|entity|string|**REQUIRED**|The entity id of the custom component. Example **`sensor.sonarr_upcoming_media`**|
|title|string|optional|Title displayed at top of card.|
|date|string|ddmmyy|Format for displaying dates. Examples: **`date: mmdd`**, **`date: ddmmyy`**, **`date: yyddmm`**|
|clock|number|12|Display times as either 12 hour  **`"clock: 12"`** or 24 hour **`"clock: 24"`**|
|max|number|5|Maximum number of items to show.|
|image_style|string|poster|There are currently two different styles for the card: poster and fanart.|
|hide_empty|boolean|false|Hide card when there are no episodes to show.|
|hide_flagged|boolean|false|Hide items that get an indicator flag. Useful to hide downloaded episodes for sonarr/radarr components.|
|hide_unflagged|boolean|false|Hide items that don't have an indicator flag. Useful to hide watched items for plex component.|
|flag|boolean|true|Display or hide indicator flag.|
|text_shadows|boolean|true|Display or hide shadows behind text.|
|box_shadows|boolean|true|Display or hide shadows behind objects.|
|all_shadows|boolean|no default|Turns both text and object shadows on or off.|
|enable_transparency|boolean|false|Turns on gradient transparency effect.|
|url|string|no default|Makes entire card clickable with specified hyperlink. You can use [keywords](#text-content) to build a custom link for each episode. Example: **`url: http://google.com?q=$title $number`** |
|collapse|string|no default|Prioritize/group by attribute value (collapsing the rest of the items). Example: **`collapse: flag=true`** |
|collapse|number|no default|Collapses all items after the specified number of items. Example: **`collapse: 2`**|
|filter|string|no default|Filter items by attribute value (including partial matches). Example: **`filter: flag=true`**.  The rest of the items will be discarded.|
|sort_by|string|no default|Attribute used for sorting items. Example: **`sort_by: airdate`** sorts items by airdate.|
|sort_ascending|boolean|true|Sort order. Set to false for descending order.|
|enable_tooltips|boolean|false|Display respective summary of item (if supported by integration).|
|disable_hyperlinks|boolean|false|Prevents hyperlinks from being clickable (for items with deep_link attributes).|

# Style Options:

|NAME|POSTER&nbsp;DEFAULTS&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|FANART&nbsp;DEFAULTS&nbsp;|DESCRIPTION|
|-|-|-|-|
|title_text<br/>line1_text<br/>line2_text<br/>line3_text<br/>line4_text|Defalts set by component|Defaults set by component|The text contents for the line. More info below.|
|title_size<br/>line1_size<br/>line2_size<br/>line3_size<br/>line4_size|large<br/>medium<br/>small<br/>small<br/>small|large<br/>medium<br/>small<br/>small<br/>small|Text size for each line. small, medium, or large|
|line_size|no default|no default|Text size of lines below title. More info below.|
|title_color<br/>line1_color<br/>line2_color<br/>line3_color<br/>line4_color|var(--primary-text-color)<br/>var(--primary-text-color)<br/>var(--primary-text-color)<br/>var(--primary-text-color)<br/>var(--primary-text-color) |'#fff'<br/>'#fff'<br/>'#fff'<br/>'#fff'<br/>'#fff'|The color of each line. Any valid CSS color. Hex values must be in quotes.|
|line_color|no default|no default|Color of lines below title. Any valid CSS color. Hex values must be in quotes. More info below.|
|border_color|'#fff'|'#000'|Color of the outside border in fanart view and border around image in poster view.|
|accent_color|var(--primary-color)|'#000'|Color of the ribbon in poster view and background in fanart view.|
|flag_color|var(--primary-color)|var(--primary-color)|Changes the color of indicator flag.|
|icon|Default set by component|Default set by component|Changes the icon in the indicator flag, uses mdi icons. <code>**"icon: mdi:arrow-down"**</code></br>Set <code>**"icon: none**"</code> to hide.|
|icon_color|var(--primary-color)|var(--primary-color)|Changes the color of the icon in the indicator flag.|
<br/>

Text color options can be any valid CSS value. This includes color names like <code>red</code>, rgb values like <code>rgba(255, 0, 0, 0.6)</code>, variable names for HA like <code>var(--primary-color)</code>, hex values like <code>'#ff6347'</code>, you can even use <code>transparent</code>. If using hex values, encase in quotes. This is the only time quotes are required in the cards configuration.

There are 2 space saving configuration options: <code>line_color</code> and <code>line_size</code>. These two options affect all lines of text below the title. These options can be overwritten as well. For example: if you set <code>line_color: white</code> and <code>line2_color: blue</code> then lines 1 & 3 will be white while line 2 will be blue.

# Text Content:

You can build your own strings for each line of text, including title by using keywords. Each keyword is replaced with its relevant content, listed below. Encase this option in quotes.

|KEYWORD|AVAILABILITY|DESCRIPTION|
|-|-|-|
|$title|All|Item's title|
|$release|All|A formatted version of the release time from the component. Particularly helpful for displaying different kinds of releases. Radarr for instance needs to distinguish between theater releases and physical releases. Radarr's release changes dynamically and is "In Theaters $day, $date" if theater release and more than a week away or "Available $day" if physical release and within a week.|
|$episode|TV Only|Episode Title|
|$number|TV Only|Season and episode number "S01E05"|
|$genres|All|List of genres|
|$rating|All|Rating of episode, source depends on component|
|$studio|All|Production Studio|
|$price|Games|Price of games meant for "Steam Wishlist UMC" and "Epic Games UMC" integrations|
|$day|All|Day of "release" (release date, download date, etc.) depending on component. This item changes from long form if within a week "Monday" to short form "Mon" if further than a week.|
|$date|All|Date of release or download, etc., depending on component. Formatted with "date" in config.|
|$time|All*|Time of release or download. * Movies generally dont have a time for release.|
|$aired|Plex|Date that the media item originally aired.
|$album|Accomodate music-related integrations such as Lidarr Upcoming Media integration.
|$artist|Accomodate music-related integrations such as Lidarr Upcoming Media integration.
|$runtime|All|Displays runtime as either "01:23" for > an hour and "23 min" otherwise.
|$empty|All|Displays line as empty space. Useful to create a break in the lines that can be sized. 
</br>

You can add in custom text to your string, only keywords are replaced. As an example you could add this to your config <code>line1_text: 'Runtime: $runtime'</code> to have line one display as "Runtime: 01:30". You can use as many keywords in your string as you like, you're only limited by what will fit. In some cases a keyword can return nothing, like when using radarr and a movie is in theaters. Occasionally not all info has been released yet, causing something like runtime to be empty. This isn't a problem when it's the only keyword in a line as the card just hides the line, but it can be an issue when you're using multiple keywords in a line. In this case you can use a hyphen to seperate the them. <code>line1_text: 'Rating: $rating - Runtime: $runtime - $number'</code> will display as "Rating: &#x2605; 7.1 - Runtime: 01:23 - S01E09" when all are available or "Rating: &#x2605; 7.1 - S01E09" if runtime is not.


# Developers

**If you'd like to make your own component to feed the upcoming media card:**

1. Component needs an attribute named "data" that contains a JSON string or OBJ.
2. The first item in your JSON must contain these keys to set your defaults: `title_default`, `line1_default`, `line2_default`, `line3_default`, `line4_default`, and `icon`. The default text contents are set exactly like the card's text content config and use the same keywords. The default icon takes an mdi icon `mdi:arrow-down`.
3. Each item must contain an 'airdate', if none exists the item is skipped. This and a poster image are the only required items.
4. If an included item is null it needs to be an empty string in the JSON `''`.
5. Items should be in descending order according to 'airdate'.
6. Be aware that the card strips parentheses and anything contained in them. This is to remove things like (US). Since we can see the art for the show/movie there is no need for that info.

## JSON items:

|KEY|DESCRIPTION|
|-|-|
|airdate|Must be UTC ISO 8601 format. Example <code>2018-10-25T01:00:00Z</code>. This is how the card creates date, day, and time. Doesn't have to be air date, just a date associated with the item. It could be download date for example.
|title|Item's title|
|release|This is a formatted version of the release time from the component. Particularly helpful for displaying different kinds of releases. Radarr for instance needs to distinguish between theater releases and physical releases, so 'release' is changed dynamically by the component and is "In Theaters $day, $date" if theater release and more than a week away or "Available $day" if physical release and within a week.|
|episode|Episode Title|
|number|Season and episode number "S01E05"|
|season_num|Season number only
|episode_num|Episode number only
|genres|List of genres|
|rating|Rating of item|
|studio|Producing Studio|
|aired|When media originally aired, useful for when airdate is set as download date etc.
|runtime|Must be number of minutes as integer, the card then formats as needed.
|poster|Direct link to items poster image
|fanart|Direct link to items fanart image. If fanart is an empty string the card will zoom in and shift the poster image as a fallback.
|flag|Display indicator or not, boolean.
|deep_link|direct URL link to respective TV Episode or Movie on Plex, Radarr, Sonarr.

## Example from Sonarr component with 3 episodes. Notice the defaults set in first item

<code>[{"title_default": "$title", "line1_default": "$episode", "line2_default": "$release", "line3_default": "$rating - $runtime", "line4_default": "$number - $studio", "icon": "mdi:arrow-down-bold-circle"}, {"title": "Modern Family", "episode": "Good Grief", "flag": false, "airdate": "2018-10-25T01:00:00Z", "number": "S10E05", "runtime": 25, "studio": "ABC (US)", "rating": "\u2605 8.8", "release": "$day, $date $time", "poster": "https://www.thetvdb.com/banners/_cache/posters/5bb9375cb2c5e.jpg", "fanart": "https://www.thetvdb.com/banners/_cache/fanart/original/5b300bbae5cd2.jpg", "genres": "Comedy"}, {"title": "American Horror Story", "episode": "Traitor", "flag": false, "airdate": "2018-10-25T02:00:00Z", "number": "S08E07", "runtime": 45, "studio": "FX (US)", "rating": "\u2605 8.4", "release": "$day, $date $time", "poster": "https://www.thetvdb.com/banners/_cache/posters/5b9983440d320.jpg", "fanart": "https://www.thetvdb.com/banners/_cache/fanart/original/5b9f15a15a9c1.jpg", "genres": "Drama, Horror, Thriller"}, {"title": "It's Always Sunny in Philadelphia", "episode": "Charlie's Home Alone", "flag": false, "airdate": "2018-10-25T02:00:00Z", "number": "S13E08", "runtime": 25, "studio": "FXX", "rating": "\u2605 9.1", "release": "$day, $date $time", "poster": "https://www.thetvdb.com/banners/_cache/posters/5ba7c2b687091.jpg", "fanart": "https://www.thetvdb.com/banners/_cache/fanart/original/5b48ef958034c.jpg", "genres": "Comedy"}]</code>
  
  
Please inform me if you create one and I'll add it to the list.</br>
Include what your components defaults are in the components readme.</br>
If you need special styling or edits to the card to accomidate your component, just ask or submit a PR.</br></br>

Thanks!
