---
name: Lyft
x-slug: lyft
description: Lyft is a peer-to-peer transportation platform that connects passengers
  who need rides with drivers willing to provide rides using their own personal vehicles.
  Lyft was started in 2012 with the mission of building a peer-to-peer transportation
  solution that would help make cities safer, more affordable and better connected.
  Lyft now operates in 68 cities across the U.S.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
x-kinRank: "8"
x-alexaRank: ""
tags: Lyft
created: "2018-05-22"
modified: "2018-05-22"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/apis.md
specificationVersion: "0.14"
apis:
- name: Lyft Cost estimates
  x-api-slug: lyft
  description: Estimate the cost of taking a Lyft between two points.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//cost
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/cost-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/cost-get-openapi.md
- name: Lyft Available drivers nearby
  x-api-slug: lyft
  description: The drivers endpoint returns a list of nearby drivers' lat and lng
    at a given location.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//drivers
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/drivers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/drivers-get-openapi.md
- name: Lyft Pickup ETAs
  x-api-slug: lyft
  description: The ETA endpoint lets you know how quickly a Lyft driver can come get
    you
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//eta
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/eta-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/eta-get-openapi.md
- name: Lyft The user's general info
  x-api-slug: lyft
  description: The v1 of this endpoint returns the user's ID, v2 will return more
    general info about the user. We require authentication for this endpoint, so we
    extract the user ID from the access token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//profile
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/profile-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/profile-get-openapi.md
- name: Lyft List rides
  x-api-slug: lyft
  description: Get a list of past & current rides for this passenger.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/rides-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/rides-get-openapi.md
- name: Lyft Request a Lyft
  x-api-slug: lyft
  description: Request a Lyft come pick you up at the given location.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/rides-post-openapi.md
- name: Lyft Get the ride detail of a given ride ID
  x-api-slug: lyft
  description: Get the status of a ride along with information about the driver, vehicle
    and price of a given ride ID
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides/{id}
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesid-get-openapi.md
- name: Lyft Cancel a ongoing requested ride
  x-api-slug: lyft
  description: Cancel a ongoing ride which was requested earlier by providing the
    ride id.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides/{id}/cancel
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesidcancel-post-openapi.md
- name: Lyft Update the destination of the ride
  x-api-slug: lyft
  description: Add or update the ride's destination. Note that the ride must still
    be active (not droppedOff or canceled), and that destinations on Lyft Line rides
    can not be changed.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides/{id}/destination
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesiddestination-put-openapi.md
- name: Lyft Add the passenger's rating, feedback, and tip
  x-api-slug: lyft
  description: Add the passenger's 1 to 5 star rating of the ride, optional written
    feedback, and optional tip amount in minor units and currency. The ride must already
    be dropped off, and ratings must be given within 24 hours of drop off. For purposes
    of display, 5 is considered the default rating. When this endpoint is successfully
    called, payment processing will begin.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides/{id}/rating
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesidrating-put-openapi.md
- name: Lyft Get the receipt of the rides.
  x-api-slug: lyft
  description: Get the receipt information of a processed ride by providing the ride
    id. Receipts will only be available to view once the payment has been processed.
    In the case of canceled ride, cancellation penalty is included if applicable.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//rides/{id}/receipt
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesidreceipt-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridesidreceipt-get-openapi.md
- name: Lyft Types of rides
  x-api-slug: lyft
  description: The ride types endpoint returns information about what kinds of Lyft
    rides you can request at a given location.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//ridetypes
  tags: Transportation
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridetypes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/ridetypes-get-openapi.md
- name: Lyft Preset Prime Time percentage
  x-api-slug: lyft
  description: Preset a Prime Time percentage in the region surrounding the specified
    location. This Prime Time percentage will be applied when requesting cost, or
    when requesting a ride in sandbox mode.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//sandbox/primetime
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/sandboxprimetime-put-openapi.md
- name: Lyft Propagate ride through ride status
  x-api-slug: lyft
  description: Propagate a sandbox-ride through various ride status
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//sandbox/rides/{id}
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/sandboxridesid-put-openapi.md
- name: Lyft Preset types of rides for sandbox
  x-api-slug: lyft
  description: The sandbox-ridetypes endpoint allows you to preset the ridetypes in
    the region surrounding the specified latitude and longitude to allow testing different
    scenarios
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//sandbox/ridetypes
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/sandboxridetypes-put-openapi.md
- name: Lyft Driver availability for processing ride request
  x-api-slug: lyft
  description: Set driver availability for the provided ride_type in the city/region
    surrounding the specified location
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1//sandbox/ridetypes/{ride_type}
  tags: Transportation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/sandboxridetypesride-type-put-openapi.md
- name: Lyft
  x-api-slug: lyft
  description: Lyft is a peer-to-peer transportation platform that connects passengers
    who need rides with drivers willing to provide rides using their own personal
    vehicles. Lyft was started in 2012 with the mission of building a peer-to-peer
    transportation solution that would help make cities safer, more affordable and
    better connected. Lyft now operates in 68 cities across the U.S.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/lyft-logo.png
  humanURL: https://www.lyft.com/
  baseURL: https://api.lyft.com//v1
  tags: Lyft
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/lyft/master/_listings/lyft/openapi.md
x-common:
- type: x-authentication
  url: https://developer.lyft.com/docs/authentication
- type: x-blog
  url: http://blog.lyft.com/
- type: x-blog-rss
  url: http://blog.lyft.com/posts?format=RSS
- type: x-branding
  url: https://developer.lyft.com/docs/brand-guidelines
- type: x-developer
  url: https://www.lyft.com/developers
- type: x-documentation
  url: http://petstore.swagger.io/?url=https://api.lyft.com/v1/spec
- type: x-github
  url: https://github.com/lyft
- type: x-manage-applications
  url: https://www.lyft.com/developers/manage
- type: x-openapi-spec
  url: https://api.lyft.com/v1/spec
- type: x-partners
  url: https://www.lyft.com/partnerships
- type: x-rate-limits
  url: https://developer.lyft.com/docs/rate-limits
- type: x-twitter
  url: https://twitter.com/lyft
- type: x-website
  url: https://www.lyft.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---