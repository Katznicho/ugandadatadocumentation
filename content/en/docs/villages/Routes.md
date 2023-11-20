---
title: Routes
description: API routes for managing villages in Uganda.
weight: 4
---

## Overview

This section provides information about the API routes related to villages in Uganda. Ensure that the `X-Requested-With` header is set with `XMLHttpRequest` and include the bearer token in the `Authorization` header for authentication.

## Get Villages

#### Endpoint

```plaintext
GET /villages
```

## Description

Get a list of villages in Uganda.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Query Parameters

- **limit** (optional): Number of districts per page (default: 100)
- **page** (optional): Page number for paginated results (default: 1)
- **sort_column** (optional): Column to sort the results by (default: districtName)
- **sort_order** (optional): Sort order (asc or desc, default: asc)

### Response

- **data**: Array of villages
- **pagination**: Information about pagination (current_page, per_page, total)
- **version**: API version

## Get Village by UUID

```plaintext
GET /village/{uuid}

```

## Description
Get details of a specific village by UUID.

## Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

Parameters
- **uuid**: UUID of the village

## Response
- data: Village details
- version: API version