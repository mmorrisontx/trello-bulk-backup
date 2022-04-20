# Trello Bulk Backup / Exporter

Backs up as much information about every board in your account, including
lists, attachments, custom fields, etc. Attachments are intelligently only
downloaded if changed.

This software comes with no guarantees. I use this personally, but I probably will not
implement feature requests, or possibly even bug fixes. YMMV.

Beware: This script deletes unmanaged files in the output directory. Don't
nuke your system drive by accident.

## How to run

### With Docker (HIGHLY RECOMMENDED)
```
docker run --rm \
  -v "$PWD:/app" \
  -w "/app" \
  node:16 npm install
docker run --rm \
  -v "$PWD:/app:ro" \
  -v "$PWD/data:/data" \
  -w "/app" \
  -e "KEY=mytrellokey" \
  -e "TOKEN=mytrellotoken" \
  -e "DATA_DIR=/data" \
  node:16 npm start
```

### Without Docker
(NodeJS 16 Required)
```
npm install
KEY=trellokey TOKEN=trellotoken DATA_DIR=path/to/output npm start
```
