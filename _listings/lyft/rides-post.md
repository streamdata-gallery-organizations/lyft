---
swagger: "2.0"
info:
  title: Lyft
  description: Drive your app to success with Lyft's API
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
  /rides:
    post:
      summary: Request a Lyft
      description: Request a Lyft come pick you up at the given location
      operationId: NewRide
      parameters:
      - in: body
        name: request
        description: Ride request information
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - transportation
definitions:
  PricingDetails:
    properties:
      base_charge:
        description: This is a default description.
        type: put
      cancel_penalty_amount:
        description: This is a default description.
        type: put
      cost_minimum:
        description: This is a default description.
        type: put
      cost_per_mile:
        description: This is a default description.
        type: put
      cost_per_minute:
        description: This is a default description.
        type: put
      currency:
        description: This is a default description.
        type: put
      trust_and_service:
        description: This is a default description.
        type: put
  RideType:
    properties:
      display_name:
        description: This is a default description.
        type: put
      seats:
        description: This is a default description.
        type: put
      image_url:
        description: This is a default description.
        type: put
  SandboxRideType:
    properties:
      lat:
        description: This is a default description.
        type: put
      lng:
        description: This is a default description.
        type: put
      ride_types:
        description: This is a default description.
        type: put
  SandboxPrimetime:
    properties:
      lat:
        description: This is a default description.
        type: put
      lng:
        description: This is a default description.
        type: put
      primetime_percentage:
        description: This is a default description.
        type: put
  SandboxDriverAvailability:
    properties:
      lat:
        description: This is a default description.
        type: put
      lng:
        description: This is a default description.
        type: put
      driver_availability:
        description: This is a default description.
        type: put
  LatLng:
    properties:
      lat:
        description: This is a default description.
        type: put
      lng:
        description: This is a default description.
        type: put
  Tip:
    properties:
      amount:
        description: This is a default description.
        type: put
      currency:
        description: This is a default description.
        type: put
  PassengerDetail:
    properties:
      first_name:
        description: This is a default description.
        type: put
      last_name:
        description: This is a default description.
        type: put
      phone_number:
        description: This is a default description.
        type: put
  DriverDetail:
    properties:
      first_name:
        description: This is a default description.
        type: put
      phone_number:
        description: This is a default description.
        type: put
      rating:
        description: This is a default description.
        type: put
      image_url:
        description: This is a default description.
        type: put
      user_id:
        description: This is a default description.
        type: put
  VehicleDetail:
    properties:
      make:
        description: This is a default description.
        type: put
      model:
        description: This is a default description.
        type: put
      year:
        description: This is a default description.
        type: put
      license_plate:
        description: This is a default description.
        type: put
      license_plate_state:
        description: This is a default description.
        type: put
      color:
        description: This is a default description.
        type: put
      image_url:
        description: This is a default description.
        type: put
  Cost:
    properties:
      amount:
        description: This is a default description.
        type: put
      currency:
        description: This is a default description.
        type: put
      description:
        description: This is a default description.
        type: put
  CancellationRequest:
    properties:
      cancel_confirmation_token:
        description: This is a default description.
        type: put
  LineItem:
    properties:
      type:
        description: This is a default description.
        type: put
      amount:
        description: This is a default description.
        type: put
      currency:
        description: This is a default description.
        type: put
  Charge:
    properties:
      amount:
        description: This is a default description.
        type: put
      currency:
        description: This is a default description.
        type: put
      payment_method:
        description: This is a default description.
        type: put
  Eta:
    properties:
      display_name:
        description: This is a default description.
        type: put
      eta_seconds:
        description: This is a default description.
        type: put
      eta_seconds_max:
        description: This is a default description.
        type: put
      is_valid_estimate:
        description: This is a default description.
        type: put
  CostEstimate:
    properties:
      display_name:
        description: This is a default description.
        type: put
      currency:
        description: This is a default description.
        type: put
      estimated_cost_cents_min:
        description: This is a default description.
        type: put
      estimated_cost_cents_max:
        description: This is a default description.
        type: put
      estimated_distance_miles:
        description: This is a default description.
        type: put
      estimated_duration_seconds:
        description: This is a default description.
        type: put
      primetime_percentage:
        description: This is a default description.
        type: put
      primetime_confirmation_token:
        description: This is a default description.
        type: put
      cost_token:
        description: This is a default description.
        type: put
      is_valid_estimate:
        description: This is a default description.
        type: put
  SandboxRideUpdate:
    properties:
      ride_id:
        description: This is a default description.
        type: put
  RideRequest:
    properties:
      ride_id:
        description: This is a default description.
        type: put
      destination:
        description: This is a default description.
        type: put
      origin:
        description: This is a default description.
        type: put
  Ride:
    properties:
      ride_id:
        description: This is a default description.
        type: put
      primetime_confirmation_token:
        description: This is a default description.
        type: put
      cost_token:
        description: This is a default description.
        type: put
      destination:
        description: This is a default description.
        type: put
      origin:
        description: This is a default description.
        type: put
  RideDetail:
    properties:
      ride_id:
        description: This is a default description.
        type: put
      primetime_percentage:
        description: This is a default description.
        type: put
      line_items:
        description: This is a default description.
        type: put
      can_cancel:
        description: This is a default description.
        type: put
      canceled_by:
        description: This is a default description.
        type: put
      rating:
        description: This is a default description.
        type: put
      feedback:
        description: This is a default description.
        type: put
      route_url:
        description: This is a default description.
        type: put
      requested_at:
        description: This is a default description.
        type: put
      beacon_color:
        description: This is a default description.
        type: put
  RideReceipt:
    properties:
      ride_id:
        description: This is a default description.
        type: put
      line_items:
        description: This is a default description.
        type: put
      charges:
        description: This is a default description.
        type: put
      requested_at:
        description: This is a default description.
        type: put
      price:
        description: This is a default description.
        type: put
      ride_profile:
        description: This is a default description.
        type: put
  NearbyDriver:
    properties:
      locations:
        description: This is a default description.
        type: put
  NearbyDriversByRideType:
    properties:
      ride_type:
        description: This is a default description.
        type: put
      drivers:
        description: This is a default description.
        type: put
  Error:
    properties:
      error:
        description: This is a default description.
        type: put
      error_detail:
        description: This is a default description.
        type: put
      error_description:
        description: This is a default description.
        type: put
  ErrorDetail:
    properties:
      field_name:
        description: This is a default description.
        type: put
  RideRequestError:
    properties:
      error:
        description: This is a default description.
        type: put
      error_detail:
        description: This is a default description.
        type: put
      error_description:
        description: This is a default description.
        type: put
      primetime_percentage:
        description: This is a default description.
        type: put
      primetime_confirmation_token:
        description: This is a default description.
        type: put
      token_duration:
        description: This is a default description.
        type: put
      cost_token:
        description: This is a default description.
        type: put
      error_uri:
        description: This is a default description.
        type: put
      primetime_multiplier:
        description: This is a default description.
        type: put
  RatingRequest:
    properties:
      rating:
        description: This is a default description.
        type: put
      feedback:
        description: This is a default description.
        type: put
      tip:
        description: This is a default description.
        type: put
  ApiError:
    properties:
      error:
        description: This is a default description.
        type: put
      error_description:
        description: This is a default description.
        type: put
      error_detail:
        description: This is a default description.
        type: put
  Profile:
    properties:
      first_name:
        description: This is a default description.
        type: put
      has_taken_a_ride:
        description: This is a default description.
        type: put
      id:
        description: This is a default description.
        type: put
      last_name:
        description: This is a default description.
        type: put
  SandboxRideStatus:
    properties: []
  UserDetail:
    properties:
      first_name:
        description: This is a default description.
        type: put
      image_url:
        description: This is a default description.
        type: put
      rating:
        description: This is a default description.
        type: put
x-collection-name: Lyft
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