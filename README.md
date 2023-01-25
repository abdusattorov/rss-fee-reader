# RSS Feed Reader

`rss-reader` is a command-line interface program to parse, process and save RSS Feeds.


## Installation and usage
1. Clone github repository:

       git clone https://github.com/abdusattorov/rss-reader

2. Change directory to `.../rss-reader`.

       cd .../rss-reader

3. Install necessary dependencies:

       pip install -r requirements.txt

After finishing the installation process and assuming your current directory is `.../rss-feed-reader`, you can run `rss_reader` as a
package:

    python rss_reader

or, provided, your current directory is `/rss-feed-reader/rss_reader`, you can directly run the
module:

    python rss_reader.py
    python -m rss_reader


## Functionality

To see help message, please, use `-h/--help` argument: `rss-feed-reader -h`.

    usage: rss_reader.py [-h] [--version] [--json] [--table] [--verbose] [--limit LIMIT]
                     source

    Pure Python command-line RSS reader.

    positional arguments:
    source         the link to the rss feed

    optional arguments:
    -h, --help     show this help message and exit
    --version      an optional argument
    --json         Print result as JSON in stdout
    --verbose      an optional argument
    --limit LIMIT  Limit news topics if this parameter provided
    --table        Print result as table


## Parsing XML

XML is parsed by parser implemented from scratch, it exploits the idea of XML *tokenization*, dom-tree is created from
tokens.


## Tested RSS links

+ Channels like these are parsed correctly:

  https://realpython.com/atom.xml

  https://news.yahoo.com/rss/

  https://daryo.uz/uz/feed/


  ## Testing

 Tests are yet to be written.

***Test coverage is xx%.***


## Known problems:

+ Some problems with a certain type of links exist:

    + http://feeds.feedburner.com/welikedota error parsing data from such links; this error happens because
      of the way xml file of the rss feed is structured; this issue will be fixed in upcoming versions;

    + If you notice any bugs or other issues please let me know. You can reach me out at https://t.me/BackendEngineer