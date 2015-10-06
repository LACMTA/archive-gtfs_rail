# LACMTA / gtfs_rail
This is the new home for Metro's rail-only GTFS archive.

Official releases and notes will be archived here:
  [https://github.com/LACMTA/gtfs_rail/releases](https://github.com/LACMTA/gtfs_rail/releases)

The evergreen link for our official releases will be:
  [https://github.com/LACMTA/gtfs_rail/archive/master.zip](https://github.com/LACMTA/gtfs_rail/archive/master.zip)

You may not want to monitor this site for the latest changes. To get the latest commit (or version) from the Github API:
  [https://api.github.com/repos/LACMTA/gtfs_rail/git/refs/heads/master](https://api.github.com/repos/LACMTA/gtfs_rail/git/refs/heads/master)

This returns:

    {
    "ref": "refs/heads/master",
    "url": "https://api.github.com/repos/LACMTA/gtfs_rail/git/refs/heads/master",
    "object": {
      "sha": "6676ac465a5c36c8b771787e1a6be7bf5aec0935",
      "type": "commit",
      "url": "https://api.github.com/repos/LACMTA/gtfs_rail/git/commits/6676ac465a5c36c8b771787e1a6be7bf5aec0935"
      }
    }

The commit hash (or sha) is unique and serves as an indicator of changes to the archive.

use [jq](https://stedolan.github.io/jq/) to parse out the commmit hash:

    $ curl -s https://api.github.com/repos/LACMTA/gtfs_rail/git/refs/heads/master | jq '.object.sha'
    "6676ac465a5c36c8b771787e1a6be7bf5aec0935"
