# Trello Bulk Backup / Exporter

Backs up as much information about every board in your account, including
lists, attachments, custom fields, etc. Attachments are intelligently only
downloaded if changed.

This software comes with no guarantees. I use this personally, but I probably will not
implement feature requests, or possibly even bug fixes. YMMV.

Beware: This script deletes unmanaged files in the output directory. Don't accidentally
nuke your system drive by accident. I'd highly recommend running this in docker to prevent
accidents.

## How to run

Node 16 required

```
npm install
KEY=trellokey TOKEN=trellotoken DATA_DIR=path/to/output node index
```
