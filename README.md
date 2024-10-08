# set_studio_metadata
A script to set Eluvio Studio metadata, extracting only titles and the latest hashes.

## Installation
```
git clone https://github.com/eluv-io/elv-utils-js
cd elv-utils-js
npm install
```

## Configuration Setup

```
{
    "config_url": "Config URL",
    "private_key": "Private key",
    "mez_lib_id": "Mezzanine library ID",
    "utilities_path": "/path/to/utilities",
    "media_catalog_id": "Media catalog ID"
}
```

## Command

```
python studio_set_metadata.py
```
Copy the output metadata from `media.json` and paste it into the Media Catalog, or use the MetaSet utility to set the metadata.

## Process
* Extract and store titles of all content IDs in `title.json`
* Extract and store latest hashes of all content IDs in `latest_hash.json`
* Create and store metadata in `media.json`
```
{
    "asset_metadata": {
        "info": {
            "description": "",
            "id": "iq__4GTwdvyifajEUfnJMc8g4sX5iyCv",
            "media": {
                "mvid12FCjEU254BsRpzqe97VS7cmcUZ": {
                    "associated_media": [],
                    "attributes": {},
                    "catalog_title": "The Wild Bunch (4/10) - 1969",
                    "clip": false,
                    "description": "",
                    "description_rich_text": "",
                    "headers": [],
                    "id": "mvid12FCjEU254BsRpzqe97VS7cmcUZ",
                    "label": "The Wild Bunch (4/10) - 1969",
                    "live_video": false,
                    ...

                "mvid12YFwoq4xprd1FwY1f7B1TL1jTc": {
                    "associated_media": [],
                    "attributes": {},
                    "catalog_title": "Holy Smoke (10/12) - 1999",
                    "clip": false,
                    "description": "",
                    "description_rich_text": "",
                    "headers": [],
                    "id": "mvid12YFwoq4xprd1FwY1f7B1TL1jTc",
                    "label": "Holy Smoke (10/12) - 1999",
                    "live_video": false,
                    ...

            "media_collections": {},
            "media_lists": {},
            "name": "music_green_main",
            "permission_sets": [],
            "tags": [],
            "title": "music_green_main"
        }
    },
    "description": "",
    "name": "Media Catalog - music_green_main"
}
```
