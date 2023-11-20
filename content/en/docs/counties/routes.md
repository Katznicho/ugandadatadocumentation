---
title:  Routes
description: API routes for managing counties in Uganda.
weight: 2
---

## Overview

This section provides information about the API routes related to counties in Uganda. Ensure that the `X-Requested-With` header is set with `XMLHttpRequest` and include the bearer token in the `Authorization` header for authentication.

## Get Counties

#### Endpoint

```plaintext
GET /counties
```

## Description

Get a list of counties in Uganda.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Query Parameters

- **limit** (optional): Number of districts per page (default: 100)
- **page** (optional): Page number for paginated results (default: 1)
- **sort_column** (optional): Column to sort the results by (default: districtName)
- **sort_order** (optional): Sort order (asc or desc, default: asc)

### Response

- **data**: Array of districts
- **pagination**: Information about pagination (current_page, per_page, total)
- **version**: API version

## GET COUNTIES BY UUID

```plaintext
GET /county/{uuid}
```

### Description

Get details of a specific county by UUID.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters

- **uuid**: UUID of the district

### Response

- **data**: County details
- **version**: API version

## Get District Subcounties
```plaintext
GET /county/{uuid}/subcounties

```
## Get County Subcounties

### Description
Get subcounties for a specific county.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

## Parameters
- **uuid**: UUID of the district

## Response
- **county**: County details
- **subcounties**: Array of subcounties
- **version**: API version

## Get County Parishes

```plaintext
GET /county/{uuid}/parishes

```

### Description
Get parishes for a specific county.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

## Parameters
- *uuid*: UUID of the district

## Response
- **county**: County details
- **parishes**: Array of parishes
- **version**: API version

## Get County Villages

## Get District Subcounties
```plaintext
GET /county/{uuid}/villages

```

### Description
Get villages for a specific county.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

## Parameters
- **uuid**: UUID of the county

## Response
- **county**: County details
- **villages**: Array of subcounties
- **version**: API version
