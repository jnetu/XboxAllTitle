# XAT - Xbox All Titles

## Xbox Title ID Catalog

### About This Project

XAT is a public catalog of Xbox title identifiers and related title metadata.

The repository collects and normalizes title information from publicly accessible sources to support preservation, research, tooling, and cross-referencing across Xbox-related services.

## Purpose

This repository is intended to:

- Maintain an open and growing list of known Xbox Title IDs.
- Preserve title metadata for historical reference.
- Support analysis of Xbox titles, platforms, achievements, and catalog availability.
- Help developers, researchers, and enthusiasts access Title ID related metadata.
- Make cross-referencing between services, tools, and platforms easier.

## Data Format

The main dataset is stored in [XboxTitleIDs.json](XboxTitleIDs.json). It is a JSON array where each item represents one Xbox title record.

```json
[
  {
    "TitleId": "1480657335",
    "Name": "0 day Attack on Earth",
    "VuiDisplayName": "0 day Attack on Earth",
    "Type": "Game",
    "MediaItemType": "XboxArcadeGame",
    "Devices": ["Xbox360", "XboxOne", "XboxSeries"],
    "IsBundle": false,
    "IsStreamable": null,
    "XboxLiveTier": "Full",
    "XboxLiveGoldRequired": false,
    "ModernTitleId": "922610858",
    "Pfn": "",
    "BingId": "66acd000-77fe-1000-9115-d802584109b7",
    "ServiceConfigId": "6a170100-7e25-4057-b5b6-2a3436fdecaa",
    "WindowsPhoneProductId": "",
    "ProductId": "",
    "AlternateProductId": "",
    "DisplayImage": "http://store-images.s-microsoft.com/image/...",
    "DisplayImageHighQuality": "http://store-images.s-microsoft.com/image/...",
    "LocalImageFile": "images/1480657335.jpg",
    "ImageCount": 0,
    "TotalAchievements": 12,
    "TotalGamerscore": 200,
    "AchievementSourceVersion": 1,
    "HasAchievements": true,
    "IsGamePass": null,
    "HasGamePassDetail": false,
    "DeveloperName": "GULTI CO.,LTD.",
    "PublisherName": "SQUARE ENIX CO.,LTD",
    "ReleaseDate": "2009-12-23T09:00:00Z",
    "MinAge": 12,
    "ShortDescription": "Short store or catalog description.",
    "Description": "Full store or catalog description.",
    "Genres": ["Shooter"],
    "Attributes": [],
    "Capabilities": [],
    "Availabilities": [
      {
        "Actions": ["Details", "Fulfill", "Purchase", "Browse", "Curate", "Redeem"],
        "AvailabilityId": "9VHPMGPP12W7",
        "Platforms": ["Xbox"],
        "SkuId": "0001",
        "ProductId": "C02CNLRP4Q85"
      }
    ],
    "StatsSourceVersion": null,
    "ContentBoards": null,
    "Images": null,
    "TitleRecord": null,
    "AlternateTitleIds": null,
    "TitleExtras": null,
    "DetailExtras": null
  }
]
```

### Field Reference

| Field | Description |
| --- | --- |
| `TitleId` | Primary Xbox title identifier. |
| `Name` | Main title name used by the dataset. |
| `VuiDisplayName` | Voice/UI display name when available. |
| `Type` | Catalog item type, such as `Game`. |
| `MediaItemType` | Xbox media classification, such as `XboxArcadeGame` or `Application`. |
| `Devices` | Xbox device families where the title is associated or playable. |
| `IsBundle` | Indicates whether the record represents a bundle. |
| `IsStreamable` | Streaming availability flag when known. |
| `XboxLiveTier` | Xbox Live service tier value when available. |
| `XboxLiveGoldRequired` | Indicates whether Xbox Live Gold is required when known. |
| `ModernTitleId` | Modern Xbox title identifier when different from or related to `TitleId`. |
| `Pfn` | Package family name, mainly used by modern Microsoft Store titles. |
| `BingId` | Bing catalog identifier when available. |
| `ServiceConfigId` | Xbox service configuration identifier. |
| `WindowsPhoneProductId` | Windows Phone product identifier when available. |
| `ProductId` | Microsoft Store product identifier when available. |
| `AlternateProductId` | Alternate product identifier when available. |
| `DisplayImage` | Primary catalog image URL. |
| `DisplayImageHighQuality` | Higher-quality catalog image URL when available. |
| `LocalImageFile` | Expected local image path for the title image. |
| `ImageCount` | Number of associated local images recorded by the dataset. |
| `TotalAchievements` | Total achievement count when achievement data is available. |
| `TotalGamerscore` | Total Gamerscore value for the title when available. |
| `AchievementSourceVersion` | Internal version marker for the achievement data source. |
| `HasAchievements` | Indicates whether achievements are recorded for the title. |
| `IsGamePass` | Game Pass status when known. |
| `HasGamePassDetail` | Indicates whether detailed Game Pass metadata is present. |
| `DeveloperName` | Developer name from catalog metadata. |
| `PublisherName` | Publisher name from catalog metadata. |
| `ReleaseDate` | Release date in ISO 8601 format when available. |
| `MinAge` | Minimum age rating value when available. |
| `ShortDescription` | Short catalog description. |
| `Description` | Full catalog description. |
| `Genres` | List of catalog genres. |
| `Attributes` | List of catalog attributes, such as Xbox Live or cloud save support. |
| `Capabilities` | List of platform or title capabilities. |
| `Availabilities` | Store availability entries, including actions, platforms, SKU, and product identifiers. |
| `StatsSourceVersion` | Internal version marker for stats metadata when available. |
| `ContentBoards` | Rating board metadata when available. |
| `Images` | Additional image metadata when available. |
| `TitleRecord` | Extended title record metadata when available. |
| `AlternateTitleIds` | Alternate title identifiers when available. |
| `TitleExtras` | Additional title-level metadata when available. |
| `DetailExtras` | Additional detail-level metadata when available. |

## Dataset Notes

- `XboxTitleIDs.json` currently contains 13,343 title records.
- `TitleId` values are unique in the current dataset.
- Some fields may be empty strings, empty arrays, or `null` when the source data does not provide a value.
- Achievement and Gamerscore values reflect the data available at the time the dataset was generated.

## Disclaimer

This project is not affiliated with or endorsed by Microsoft, Xbox, or TrueAchievements.com.

All data is collected from publicly accessible sources and is shared for non-commercial, educational, preservation, and research purposes.

Please refer to the original services and catalogs for the most up-to-date information.
