---
swagger: "2.0"
x-collection-name: Lyft
x-complete: 0
info:
  title: Lyft Pickup ETAs
  description: The ETA endpoint lets you know how quickly a Lyft driver can come get
    you
  contact:
    name: Lyft
    url: http://developer.lyft.com
    email: api-support@lyft.com
  version: 1.0.0
host: api.lyft.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /cost:
    get:
      summary: Cost estimates
      description: Estimate the cost of taking a Lyft between two points.
      operationId: GetCost
      x-api-path-slug: cost-get
      parameters:
      - in: query
        name: end_lat
        description: Latitude of the ending location
      - in: query
        name: end_lng
        description: Longitude of the ending location
      - in: query
        name: No Name
      - in: query
        name: start_lat
        description: Latitude of the starting location
      - in: query
        name: start_lng
        description: Longitude of the starting location
      responses:
        1:
          description: User not found
        100:
          description: Invalid API Key - The API key passed was not valid or has expired
        105:
          description: Service currently unavailable - The requested service is temporarily
            unavailable
        106:
          description: Write operation failed - The requested operation failed due
            to a temporary issue
        111:
          description: Format "xxx" not found - The requested response format was
            not found
        112:
          description: Method "xxx" not found - The requested method was not found
        114:
          description: Invalid SOAP envelope - The SOAP envelope send in the request
            could not be parsed
        115:
          description: Invalid XML-RPC Method Call - The XML-RPC request document
            could not be parsed
        116:
          description: Bad URL found - One or more arguments contained a URL that
            has been used for abuse on Flickr
      tags:
      - Transportation
  /drivers:
    get:
      summary: Available drivers nearby
      description: The drivers endpoint returns a list of nearby drivers' lat and
        lng at a given location.
      operationId: GetDrivers
      x-api-path-slug: drivers-get
      parameters:
      - in: query
        name: No Name
      responses:
        1:
          description: User not found
        100:
          description: Invalid API Key - The API key passed was not valid or has expired
        105:
          description: Service currently unavailable - The requested service is temporarily
            unavailable
        106:
          description: Write operation failed - The requested operation failed due
            to a temporary issue
        111:
          description: Format "xxx" not found - The requested response format was
            not found
        112:
          description: Method "xxx" not found - The requested method was not found
        114:
          description: Invalid SOAP envelope - The SOAP envelope send in the request
            could not be parsed
        115:
          description: Invalid XML-RPC Method Call - The XML-RPC request document
            could not be parsed
        116:
          description: Bad URL found - One or more arguments contained a URL that
            has been used for abuse on Flickr
      tags:
      - Transportation
  /eta:
    get:
      summary: Pickup ETAs
      description: The ETA endpoint lets you know how quickly a Lyft driver can come
        get you
      operationId: GetETA
      x-api-path-slug: eta-get
      parameters:
      - in: query
        name: No Name
      responses:
        1:
          description: User not found
        100:
          description: Invalid API Key - The API key passed was not valid or has expired
        105:
          description: Service currently unavailable - The requested service is temporarily
            unavailable
        106:
          description: Write operation failed - The requested operation failed due
            to a temporary issue
        111:
          description: Format "xxx" not found - The requested response format was
            not found
        112:
          description: Method "xxx" not found - The requested method was not found
        114:
          description: Invalid SOAP envelope - The SOAP envelope send in the request
            could not be parsed
        115:
          description: Invalid XML-RPC Method Call - The XML-RPC request document
            could not be parsed
        116:
          description: Bad URL found - One or more arguments contained a URL that
            has been used for abuse on Flickr
      tags:
      - Transportation
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---