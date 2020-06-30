---
title: CosmosDB Setting for GeoLocation
tags:
  - Azure CosmosDB
category:
  - 資料庫庫
date: 2018-10-19 11:30:49
---
# 好像直接用這個當 CosmosDB BravoPoint 設定即可 #

```
{
    "indexingMode": "consistent",
    "automatic": true,
    "includedPaths": [
        {
            "path": "/*",
            "indexes": [
                {
                    "kind": "Range",
                    "dataType": "Number",
                    "precision": -1
                },
                {
                    "kind": "Range",
                    "dataType": "String",
                    "precision": -1
                }
            ]
        },
        {
            "path": "/Location/?",
            "indexes": [
                {
                    "kind": "Range",
                    "dataType": "Number",
                    "precision": -1
                },
                {
                    "kind": "Spatial",
                    "dataType": "Point"
                },
                {
                    "kind": "Range",
                    "dataType": "String",
                    "precision": -1
                }
            ]
        }
    ],
    "excludedPaths": [
        {
            "path": "/\"_etag\"/?"
        }
    ]
}
```