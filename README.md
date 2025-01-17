## Description
Updated to Python3.7
This is a updated fork of the [Deluge][1] plugin that allows you to create a list of default trackers
that will be added to new public torrents (and old ones after restarting Deluge). The
plugin will not duplicate existing trackers and does not care how the torrent
was added so it works perfectly fine with infohashes.

Private torrents are excluded on purpose, because their metadata is not
supposed to reach public trackers.

[download 2.7 here][2]

[download 3.7 here][3]

There is also a premade [config][4] for those of us that run cli/headless Based off of this [list][5] from ngosang

Besides manually creating the default tracker list, you can also load it (periodically) from a URL.

## Installation

* create the egg with

    `python setup.py bdist_egg`

(or try to use [the one from the "egg" directory][4] - be careful to install the py2.7 or py3.7 version of Deluge, if you're using Windows)

* add it to Deluge from Preferences -> Plugins -> Install Plugin

## Troubleshooting

To get Deluge's output on Windows, run this in a terminal ("cmd" works):

`"%ProgramFiles%\Deluge\deluge-debug.exe"`

## TODO:

* log the added trackers so we can remove them from torrents when they are deleted from the default list
* WebUI version

[1]: http://deluge-torrent.org/
[2]: https://github.com/BigWebstas/deluge-default-trackers/blob/master/egg/DefaultTrackers-0.1-py2.7.egg?raw=true
[3]: https://github.com/BigWebstas/deluge-default-trackers/blob/master/egg/DefaultTrackers-0.1-py3.7.egg?raw=true
[4]: https://github.com/BigWebstas/deluge-default-trackers/tree/master/egg
[5]: https://raw.githubusercontent.com/ngosang/trackerslist/master/trackers_all_ip.txt

