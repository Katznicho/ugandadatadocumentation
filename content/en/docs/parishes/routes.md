---
title:  Routes
description: API routes for managing parishes in Uganda.
weight: 3
---

## Overview

This section provides information about the API routes related to parishes in Uganda. Ensure that the `X-Requested-With` header is set with `XMLHttpRequest` and include the bearer token in the `Authorization` header for authentication.

## Get Parishes

#### Endpoint

```plaintext
GET /parishes
```

## Description

Get a list of parishes in Uganda.

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

## Get Parish by UUID

```plaintext
GET /parish/{uuid}

```

### Description
Get details of a specific parish by UUID.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters
- **uuid**: UUID of the parish

### Response
- **data**: Parish details
- **version**: API version


### GET Parish Villages

```plaintext
GET /parish/{uuid}/villages

```
### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters
- **uuid**: UUID of the parish

### Response
- **parish**: Parish details
-- **villages**:An array of villages
- **version**: API version
