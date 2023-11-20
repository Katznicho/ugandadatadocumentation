---
title: Routes
description: API routes for managing subcounties in Uganda.
weight: 3
---

## Overview

This section provides information about the API routes related to subcounties in Uganda. Ensure that the `X-Requested-With` header is set with `XMLHttpRequest` and include the bearer token in the `Authorization` header for authentication.

## Get Subcounties

#### Endpoint

```plaintext
GET /subcounties
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

- **data**: Array of subcounties
- **pagination**: Information about pagination (current_page, per_page, total)
- **version**: API version

## Get Subcounty by UUID
```plaintext
GET /subcounty/{uuid}

```

### Description

Get details of a specific sub county by UUID.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters

- **uuid**: UUID of the sub county

### Response

- **data**: County details
- **version**: API version

## Get Subcounty Parishes
```plaintext
GET /subcounty/{uuid}/parishes

```

### Description
 Get parishes for a specific subcounty.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters
- **uuid**: UUID of the subcounty

### Response
- **subcounty**: Subcounty details
- **parishes**: Array of parishes
- **version**: API version

## Get Subcounty Villages

```plaintext
GET /subcounty/{uuid}/villages

```

### Description
 Get villages for a specific subcounty.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters
- **uuid**: UUID of the subcounty

### Response
- **subcounty**: Subcounty details
- **parishes**: Array of parishes
- **version**: API version
