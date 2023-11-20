---
title: Routes
description: API routes for managing districts in Uganda.
weight: 1
---

## Overview

This section provides information about the API routes related to districts in Uganda. Ensure that the `X-Requested-With` header is set with `XMLHttpRequest` and include the bearer token in the `Authorization` header for authentication.

## Get Districts

#### Endpoint

```plaintext
GET /districts
```

## Description

Get a list of districts in Uganda.

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

### Example - Success Response

```json
{
  "data": [
    {
      "uuid": "a3daf61e-f8d3-43a1-a628-1071165abb12",
      "districtName": "ABIM"
    },
    {
      "uuid": "10f70fa0-f5af-4e4c-aedf-bffc5bcd320c",
      "districtName": "ADJUMANI"
    }
  ],
  "pagination": {
    "current_page": 1,
    "per_page": "2",
    "total": 135
  },
  "version": "1.0.0"
}
```

### Example - Failed Response

```json
{
  "message": "Unauthenticated."
}
```

## GET DISTRICTS BY UUID

```plaintext
GET /district/{uuid}
```

### Description

Get details of a specific district by UUID.

### Headers

- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters

- **uuid**: UUID of the district

### Response

- **data**: District details
- **version**: API version

### Example - Success Response

```json
{
  "data": {
    "uuid": "a3daf61e-f8d3-43a1-a628-1071165abb12",
    "districtName": "ABIM"
  },
  "version": "1.0.0"
}
```

### Example - Failed Response

```json
{
  "message": "Unauthenticated."
}
```

## Get District Counties

```plaintext
GET /district/{uuid}/counties
```

### Description
Get counties for a specific district.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

### Parameters
- **uuid**: UUID of the district

### Response
- **district**: District details
- **counties**: Array of counties
- **version**: API version

### Example Success Response
```josn
{
    "district": {
        "uuid": "a3daf61e-f8d3-43a1-a628-1071165abb12",
        "districtName": "ABIM"
    },
    "counties": [
        {
            "uuid": "762b65f7-831b-49e8-b966-6e9d0cff69cf",
            "countyName": "LABWOR"
        }
    ],
    "version": "1.0.0"
}
```

## Get District Subcounties
```plaintext
GET /district/{uuid}/subcounties

```

### Description
Get subcounties for a specific district.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

## Parameters
- **uuid**: UUID of the district

## Response
- **district**: District details
- **subcounties**: Array of subcounties
- **version**: API version

## Get District Parishes

## Get District Subcounties
```plaintext
GET /district/{uuid}/parishes

```

### Description
Get parishes for a specific district.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

## Parameters
- **uuid**: UUID of the district

## Response
- **district**: District details
- **parishes**: Array of subcounties
- **version**: API version


## Get District Villages

## Get District Subcounties
```plaintext
GET /district/{uuid}/villages

```

### Description
Get villages for a specific district.

### Headers
- X-Requested-With: XMLHttpRequest
- Authorization: Bearer [YOUR_TOKEN]

## Parameters
- **uuid**: UUID of the district

## Response
- **district**: District details
- **villages**: Array of subcounties
- **version**: API version


