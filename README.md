# Rubytify
In this PR the following endpoints where added:
api/v1/artists
￼
api/v1/artists/:id/albums
￼
api/v1/albums/:id/songs
￼
api/v1/genres/:genre_name/random_song
￼

Only three of them are working on Heroku
https://cami-ayenda.herokuapp.com/api/v1/artists
https://cami-ayenda.herokuapp.com/api/v1/artists/2/albums
https://cami-ayenda.herokuapp.com/api/v1/albums/1/songs

I had some troubles with the albums and songs, I got RestClient::TooManyRequests: 429 Too Many Requests and probably not all the albums and songs were saved

You can check all the endpoints locally, running:
Rake db:migrate
Rake db:spotify to charge all the database.

if you want to charge only the artists, you can use db:artists, for only albums use db:albums, and songs db:songs. Just make sure that the artists are created before the albums and the albums before the songs.

I added some tests you can run them using rspec.
