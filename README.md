# Moonraker - API Web Server for Klipper

This project still in bata

### The `zip` and `webui` depoly file format 

``` json
{
    "name": "v1.0.0",
    "assets": [
        {
            "content_type": "application/zip",
            "download_url": "< url to download >",
            "size": < release file size in bytes >
        }
    ],
    "prerelease": false 
}
```

### Example file structure for server depoly 

``` 
/server
    /example-release
        /releases
            latest
            /tags
                v1.0.0
                v1.0.1
                v1.0.2

        # this can be in different server or cdn
        # it control by the release file
        /release-file 
            /v1.0.0
                file.zip
            /v1.0.1
                file.zip
            /v1.0.2
                file.zip
```

### update manager `zip` and `webui` example 

```
[update_manager mainsail]
type: web
channel: stable
repo: < full url to depoly file >
path: ~/mainsail
```

### update manager for `klipper` and `moonraker`

```
[update_manager moonraker]
origin: < git repo >

[update_manager klipper]
origin: < git repo >
```
