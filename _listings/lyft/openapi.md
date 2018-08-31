swagger: "2.0"
x-collection-name: Lyft
x-complete: 1
info:
  title: Lyft
  description: drive-your-app-to-success-with-lyfts-api
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
  /profile:
    get:
      summary: The user's general info
      description: The v1 of this endpoint returns the user's ID, v2 will return more
        general info about the user. We require authentication for this endpoint,
        so we extract the user ID from the access token.
      operationId: GetProfile
      x-api-path-slug: profile-get
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
  /rides:
    get:
      summary: List rides
      description: Get a list of past & current rides for this passenger.
      operationId: GetRides
      x-api-path-slug: rides-get
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
    post:
      summary: Request a Lyft
      description: Request a Lyft come pick you up at the given location.
      operationId: NewRide
      x-api-path-slug: rides-post
      parameters:
      - in: body
        name: request
        description: Ride request information
        schema:
          $ref: '#/definitions/holder'
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
  /rides/{id}:
    get:
      summary: Get the ride detail of a given ride ID
      description: Get the status of a ride along with information about the driver,
        vehicle and price of a given ride ID
      operationId: GetRide
      x-api-path-slug: ridesid-get
      parameters:
      - in: path
        name: id
        description: The ID of the ride
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
  /rides/{id}/cancel:
    post:
      summary: Cancel a ongoing requested ride
      description: Cancel a ongoing ride which was requested earlier by providing
        the ride id.
      operationId: CancelRide
      x-api-path-slug: ridesidcancel-post
      parameters:
      - in: path
        name: id
        description: The ID of the ride
      - in: body
        name: request
        schema:
          $ref: '#/definitions/holder'
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
  /rides/{id}/destination:
    put:
      summary: Update the destination of the ride
      description: Add or update the ride's destination. Note that the ride must still
        be active (not droppedOff or canceled), and that destinations on Lyft Line
        rides can not be changed.
      operationId: SetRideDestination
      x-api-path-slug: ridesiddestination-put
      parameters:
      - in: path
        name: id
        description: The ID of the ride
      - in: body
        name: request
        description: The coordinates and optional address of the destination
        schema:
          $ref: '#/definitions/holder'
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
  /rides/{id}/rating:
    put:
      summary: Add the passenger's rating, feedback, and tip
      description: Add the passenger's 1 to 5 star rating of the ride, optional written
        feedback, and optional tip amount in minor units and currency. The ride must
        already be dropped off, and ratings must be given within 24 hours of drop
        off. For purposes of display, 5 is considered the default rating. When this
        endpoint is successfully called, payment processing will begin.
      operationId: SetRideRating
      x-api-path-slug: ridesidrating-put
      parameters:
      - in: path
        name: id
        description: The ID of the ride
      - in: body
        name: request
        description: The rating and optional feedback
        schema:
          $ref: '#/definitions/holder'
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
  /rides/{id}/receipt:
    get:
      summary: Get the receipt of the rides.
      description: Get the receipt information of a processed ride by providing the
        ride id. Receipts will only be available to view once the payment has been
        processed. In the case of canceled ride, cancellation penalty is included
        if applicable.
      operationId: GetRideReceipt
      x-api-path-slug: ridesidreceipt-get
      parameters:
      - in: path
        name: id
        description: The ID of the ride
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
  /ridetypes:
    get:
      summary: Types of rides
      description: The ride types endpoint returns information about what kinds of
        Lyft rides you can request at a given location.
      operationId: GetRideTypes
      x-api-path-slug: ridetypes-get
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
  /sandbox/primetime:
    put:
      summary: Preset Prime Time percentage
      description: Preset a Prime Time percentage in the region surrounding the specified
        location. This Prime Time percentage will be applied when requesting cost,
        or when requesting a ride in sandbox mode.
      operationId: SetPrimeTime
      x-api-path-slug: sandboxprimetime-put
      parameters:
      - in: body
        name: request
        description: Prime Time to be preset in the region surrounding the lat, lng
        schema:
          $ref: '#/definitions/holder'
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
  /sandbox/rides/{id}:
    put:
      summary: Propagate ride through ride status
      description: Propagate a sandbox-ride through various ride status
      operationId: SetRideStatus
      x-api-path-slug: sandboxridesid-put
      parameters:
      - in: path
        name: id
        description: The ID of the ride
      - in: body
        name: request
        description: status to propagate the ride into
        schema:
          $ref: '#/definitions/holder'
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
  /sandbox/ridetypes:
    put:
      summary: Preset types of rides for sandbox
      description: The sandbox-ridetypes endpoint allows you to preset the ridetypes
        in the region surrounding the specified latitude and longitude to allow testing
        different scenarios
      operationId: SetRideTypes
      x-api-path-slug: sandboxridetypes-put
      parameters:
      - in: body
        name: request
        description: Ridetypes to be preset in the region surrounding the lat, lng
        schema:
          $ref: '#/definitions/holder'
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
  /sandbox/ridetypes/{ride_type}:
    put:
      summary: Driver availability for processing ride request
      description: Set driver availability for the provided ride_type in the city/region
        surrounding the specified location
      operationId: SetRideTypeAvailability
      x-api-path-slug: sandboxridetypesride-type-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: request
        description: Driver availability to be preset in the region surrounding the
          lat, lng
        schema:
          $ref: '#/definitions/holder'
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