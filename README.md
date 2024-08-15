# billboard-hits
Pulls down Top Billboard hits from playback.fm lists, and obtains spotify URLs for each track.

The aim of this is to have a list of hits and spotify URLs, to be able to randomly select a hit and present the spotify URL for playback.
See https://github.com/stevehollx/digital-rock-expert for playing the game.

Functionally working to get a hit list, but there are some known issues:
* Spotify has a daily API call limit, so after about 60-70 years of calls it may pause fetching for 24 hours. Keep the script running and it will continue when spotify lifts the halt on responses.
* It it returning some results from a prior query in the next row on the third search pass. I haven't looked into fixing yet, and just cleaned those results by hand by finding where artist or track title didnt match or there was a URL in adjacent rows.

If you find Spotify URLs that are incorrect, please submit a merge request for the changes and will gladly update. As I have reverse queried URLS for their artist & title names with fuzzy string matching, the URLs should be 99%+ accurate as I audited most low scoring matches by hand.
