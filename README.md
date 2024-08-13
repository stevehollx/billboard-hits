# billboard-hits
Pulls down Top Billboard hits from playback.fm lists, and obtains spotify URLs for each track.

The aim of this is to have a list of hits and spotify URLs, to be able to randomly select a hit and present the spotify URL for playback.
See https://github.com/stevehollx/digital-rock-expert for playing the game.

Functionally working to get a hit list, but there are some known issues:
* Will max out spotify API calls requiring a 24h pause before the API resumes returning results. This seems to happen after about fetching 50 years of data. The queries could be chunked into requests to reduce API calls, but haven't implemented it, as I just manually stitched together adjacent runs of the appropriate years.
* Returns some live tracks in results. Haven't found out a clean way to prevent this, so cleaning them by hand.
* Returns some erronous results for some artists/tracks. Not sure yet how to optimize--ended up cleaning these results by hand.

If you find Spotify URLs that are incorrect, please submit a merge request for the changes and will gladly update. As I have reverse queried URLS for their artist & title names with fuzzy string matching, the URLs should be 99%+ accurate as I audited most low scoring matches by hand.
