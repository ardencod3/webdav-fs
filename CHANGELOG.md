# WebDAV-fs changelog

## v0.7.1
_2016-10-01_

* Fixed a bug where `readFile` would return corrupted data when used in `"binary"` mode. The issue was to do with the [node-fetch](https://github.com/bitinn/node-fetch) package which didn't have appropriate support for buffer output at the time of original implementation. node-fetch was updated in this release.

## v0.7.0
_2016-08-02_

 * Added _stat_ support to `readdir`, which can now optionally return an array of stat objects instead of just filename strings. Due to complicated configurations like this, and their unintuitive nature in their default behaviour, **webdav-fs may drift from its fs alignment** at some stage in the near future (possibly for v1.0).

## v0.6.0
_2016-04-05_

 * Added support for renaming files and directories, which also allows for the moving of items.
