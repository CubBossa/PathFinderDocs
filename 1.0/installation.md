# Installation

## Dependencies

To get started, you first require to install the following dependencies:

- [ProtocolLib](https://www.spigotmc.org/resources/protocollib.1997/) (Make sure to use the appropriate version)
- Thats it for now :D

::: Tip
While the last Minecraft is quite new, ProtocolLib might not have released
an according version. Follow their instructions about development builds, which
are not quite as save to use but mostly work.
This also applies to ProtocolLib for 1.19 at the moment.
:::

## First launch

With all dependencies installed you are good to go and run your server.
If the plugin is listed in ``/pl``, it has successfully been started.

You will find, that no roadmaps, visualizers, nodegroups or playerdata exist yet,
which is fine. You can discover the commands by yourself or read more in the wiki.

## Backups and Data-Reset

To reset your data to the initial point, stop your server and delete the data directory within
the PathFinder directory in your plugins folder.
Assuming that you use a local datastorage (yml, sqlite), this will clear all
data. For remote datastorages (mongodb, mysql) you need to delete the data in the
database manually.

To backup a state of the plugin, you have to disable the plugin by stopping the server.
Then you can put, exchange or modify the local data and start the server.
Make sure not to break relations between objects. For example, a visualizer
could reference another visualizer as child. Deleting the child in the raw datastorage will cause
problems while loading the parent visualizer.