# Spotify-Like Music Recommender

Building a music recommender system that suggests music artists using collaborative filtering and Alternating Least Squares.

## Dataset
### Description
This dataset contains social networking, tagging, and music artist listening information from a set of 2K users from Last.fm online music system.
http://www.last.fm 

### Statistics
- 1892 users
- 17632 artists
- 12717 bi-directional user friend relations, i.e. 25434 (user_i, user_j) pairs avg. 13.443 friend relations per user
- 92834 user-listened artist relations, i.e. tuples [user, artist, listeningCount] avg. 49.067 artists most listened by each user avg. 5.265 users who listened each artist
- 11946 tags
- 186479 tag assignments (tas), i.e. tuples [user, tag, artist]
         avg. 98.562 tas per user
         avg. 14.891 tas per artist
         avg. 18.930 distinct tags used by each user
         avg. 8.764 distinct tags used for each artist

### Files
- artists.dat
 
	This file contains information about music artists listened and tagged by the users.
 
 - tags.dat
 
	This file contains the set of tags available in the dataset.

 - user_artists.dat
 
	This file contains the artists listened by each user.
	
	It also provides a listening count for each [user, artist] pair.

 - user_taggedartists.dat - user_taggedartists-timestamps.dat
 
	These files contain the tag assignments of artists provided by each particular user.
	
	They also contain the timestamps when the tag assignments were done.
 
 - user_friends.dat
 
	These files contain the friend relations between users in the database.

### Format
The data is formatted one entry per line as follows (tab separated, "\t"):

* artists.dat

		id \t name \t url \t pictureURL

		Example:
		707	Metallica	http://www.last.fm/music/Metallica	http://userserve-ak.last.fm/serve/252/7560709.jpg

* tags.dat

		tagID \t tagValue
		1	metal

* user_artists.dat

		userID \t artistID \t weight
		2	51	13883

* user_taggedartists.dat

		userID \t artistID \t tagID \t day \t month \t year
		2	52	13	1	4	2009  

* user_taggedartists-timestamps.dat

		userID \t artistID \t tagID \t timestamp
		2	52	13	1238536800000

* user_friends.dat

		userID \t friendID
		2	275
