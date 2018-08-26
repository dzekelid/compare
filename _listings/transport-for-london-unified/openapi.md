---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 1
info:
  title: Transport for London Unified
  description: our-unified-api-brings-together-data-across-all-modes-of-transport-into-a-single-restful-api--this-api-provides-access-to-the-most-highly-requested-realtime-and-status-infomation-across-all-the-modes-of-transport-in-a-single-and-consistent-way--access-to-the-developer-documentation-is-available-at-httpsapi-tfl-gov-uk
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /TravelTimes/compareOverlay/{z}/mapcenter/{mapCenterLat}/{mapCenterLon}/pinlocation/{pinLat}/{pinLon}/dimensions/{width}/{height}
  : get:
      summary: Travel Times compare Overlay z mapcenter map Center Lat map Center
        Lon pinlocation pin Lat pin Lon dimensions wth height
      description: Gets the traveltime overlay..
      operationId: TravelTime_GetCompareOverlay
      x-api-path-slug: traveltimescompareoverlayzmapcentermapcenterlatmapcenterlonpinlocationpinlatpinlondimensionswidthheight-get
      parameters:
      - in: query
        name: compareType
      - in: query
        name: compareValue
      - in: query
        name: direction
        description: The direction of travel
      - in: path
        name: height
        description: The height of the requested overlay
      - in: path
        name: mapCenterLat
        description: The map center latitude
      - in: path
        name: mapCenterLon
        description: The map center longitude
      - in: query
        name: modeId
        description: The id of the mode
      - in: path
        name: pinLat
        description: The latitude of the pin
      - in: path
        name: pinLon
        description: The longitude of the pin
      - in: query
        name: scenarioTitle
        description: The title of the scenario
      - in: query
        name: timeOfDayId
        description: The id for the time of day (AM/INTER/PM)
      - in: query
        name: travelTimeInterval
        description: The total minutes between the travel time bands
      - in: path
        name: width
        description: The width of the requested overlay
      - in: path
        name: z
        description: The zoom level
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Times
      - Compare
      - Overlay
      - Z
      - Mapcenter
      - Map
      - Center
      - Lat
      - Map
      - Center
      - Lon
      - Pinlocation
      - Pin
      - Lat
      - Pin
      - Lon
      - Dimensions
      - Wth
      - Height
---