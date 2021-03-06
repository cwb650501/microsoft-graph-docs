---
author: learafa
description: "List the sites that have been followed by the signed in user."
title: List followed sites
localization_priority: Normal
ms.prod: "SharePoint"
doc_type: apiPageType
---
# List followed sites

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

List the [sites](../resources/site.md) that have been followed by the signed in user.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Sites.Read.All, Sites.ReadWrite.All  |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Sites.Read.All, Sites.ReadWrite.All |

## HTTP request

This method is accessible only through OneDrive for Business.

<!-- { "blockType": "ignored" } -->

```http
POST /me/followedSites
```

## Optional query parameters
This method supports the [OData query parameters](/graph/query_parameters) to help customize the response.

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization  | Bearer {code}. Required.|

## Request Body

Do not supply a request body for this method.

## Response

This method returns a collection of [site](../resources/site.md) resources that the user is following.
If no sites were found, an empty collection is returned.

## Example

### Request

<!-- { "blockType": "request", "name": "get-analytics" } -->

```msgraph-interactive
POST /me/followedSites
```
### Response
<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.site)", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
        {
            "id": "contoso.sharepoint.com,2C712604-1370-44E7-A1F5-426573FDA80A,2D2244C3-251A-49EA-93A8-39E1C3A060FE",
            "displayName": "OneDrive Team Site",
            "webUrl": "https://contoso.sharepoint.com/teams/1drvteam",
            "sharepointIds": {
                "listItemId": "1",
                "siteId": "2C712604-1370-44E7-A1F5-426573FDA80A",
                "siteUrl": "https://contoso.sharepoint.com/teams/1drvteam",
                "webId": "2D2244C3-251A-49EA-93A8-39E1C3A060FE"
            },
            "siteCollection": {
                "hostname": "contoso.sharepoint.com"
            }
        },
        {
            "id": "contoso.sharepoint.com,1C712604-1370-44E7-A1F5-426573FDA80A,1D2244C3-251A-49EA-93A8-39E1C3A060FE",
            "displayName": "OneDrive Team Site1",
            "webUrl": "https://contoso.sharepoint.com/teams/2drvteam",
            "sharepointIds": {
                "listItemId": "1",
                "siteId": "1C712604-1370-44E7-A1F5-426573FDA80A",
                "siteUrl": "https://contoso.sharepoint.com/teams/2drvteam",
                "webId": "1D2244C3-251A-49EA-93A8-39E1C3A060FE"
            },
            "siteCollection": {
                "hostname": "contoso.sharepoint.com"
            }
        }
  ]
}
```

<!--
{
  "type": "#page.annotation",
  "description": "List the sites a user is following.",
  "keywords": "site,onedrive.site,list followed sites, followedSites",
  "section": "documentation",
  "tocPath": "Sites/List followed sites",
  "suppressions": [
  ]
}
-->
