#SQLITE3 alpine based image

This was just something I built quickly to test out the alpine image. To use
it:

Simply mount your database to /db/db.db. I run my image like so:

docker run --rm -it -v ~/Path/To/My/Db/database.db:/db/db.db spartakode/sqlite3:latest
