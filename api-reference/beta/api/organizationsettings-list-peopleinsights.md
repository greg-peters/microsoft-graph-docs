---
title: "List peopleInsights"
description: "Retrieve properties of an insightsSettings object for displaying or returning people insights in an organization."
author: "simonhult"
ms.localizationpriority: medium
ms.prod: "insights"
doc_type: "apiPageType"
---

# List peopleInsights

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the properties of an [insightsSettings](../resources/insightssettings.md) object for displaying or returning people insights in an organization.

To learn how to customize privacy for people insights in an organization, see [Customize people insights privacy](/graph/insights-customize-people-insights-privacy).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | User.Read.All, User.ReadWrite.All |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Not supported. |

## HTTP request
<!-- { "blockType": "ignored" } -->

```http
GET /organization/{organizationId}/settings/peopleInsights
```

## Request headers

| Name       | Description|
|:-----------|:----------|
| Authorization  | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and [insightsSettings](../resources/insightssettings.md) object in the response body.

## Example 
### Request

<!-- {
  "blockType": "request",
  "name": "get_insightssettingspeoplerequest"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/beta/organization/{organizationId}/settings/peopleInsights
```

### Response

Here is an example of the response. 
> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.insightsSettings",
  "name": "get_insightssettingspeoplerequest"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "isEnabledInOrganization": true,
  "disabledForGroup": "edbfe4fb-ec70-4300-928f-dbb2ae86c981"
}
```

## See also
[Customize item insights privacy](/graph/insights-customize-item-insights-privacy) for an organization.