# billboard-hits
Pulls down Top Billboard hits from playback.fm lists, and obtains spotify URLs for each track.

The aim of this is to have a list of hits and spotify URLs, to be able to randomly select a hit and present the spotify URL for playback.
See https://github.com/stevehollx/digital-rock-expert for playing the game.

Functionally working to get a hit list, but there are some known issues:
* Will max out spotify API calls requiring a 24h pause before resuming. This seems to happen after about fetching 50 years of data.
* Returns some live tracks. Haven't found out a clean way to prevent this, so cleaning them by hand.
* Returns some erronous results for some artists/tracks. Not sure yet how to optimize--ended up cleaning these results by hand.
