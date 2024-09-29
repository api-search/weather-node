---
name: Calculators
description: Needs a description.
image: https://kinlane-productions2.s3.amazonaws.com/apis-json-icons/calculators.png
url: https://example.com/apis/calculators.yml
created: 2024/4/8
modified: 2024/4/8
specificationVersion: '0.16'
tags:
  - Calculators
apis:
  - name: location
    description: >-
      <p>"Suite of geospatial services including Maps, Places, Routes, Tracking,
      and Geofencing"</p>
    image: https://kinlane-productions2.s3.amazonaws.com/apis-json/apis-json-logo.jpg
    humanURL: https://example.com
    baseURL: https://example.com
    tags: []
    properties:
      - type: Documentation
        url: https://example.com
      - type: OpenAPI
        data:
          openapi: 3.1.0
          info:
            title: location
          paths:
            /tracking/v0/trackers/{TrackerName}/consumers:
              POST:
                summary: AssociateTrackerConsumer
                description: >-
                  <p>Creates an association between a geofence collection and a
                  tracker resource. This allows the tracker resource to
                  communicate location data to the linked geofence collection.
                  </p> <p>You can associate up to five geofence collections to
                  each tracker resource.</p> <note> <p>Currently not supported —
                  Cross-account configurations, such as creating associations
                  between a tracker resource in one account and a geofence
                  collection in another account.</p> </note>
                tags:
                  - Associate
                  - Trackers
                  - Consumer
                  - Trackers
                  - Names
                  - Consumers
            /tracking/v0/trackers/{TrackerName}/delete-positions:
              POST:
                summary: BatchDeleteDevicePositionHistory
                description: >-
                  <p>Deletes the position history of one or more devices from a
                  tracker resource.</p>
                tags:
                  - Batches
                  - Delete
                  - Device
                  - Positions
                  - History
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
            /geofencing/v0/collections/{CollectionName}/delete-geofences:
              POST:
                summary: BatchDeleteGeofence
                description: >-
                  <p>Deletes a batch of geofences from a geofence
                  collection.</p> <note> <p>This operation deletes the resource
                  permanently.</p> </note>
                tags:
                  - Batches
                  - Delete
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
            /geofencing/v0/collections/{CollectionName}/positions:
              POST:
                summary: BatchEvaluateGeofences
                description: >-
                  <p>Evaluates device positions against the geofence geometries
                  from a given geofence collection.</p> <p>This operation always
                  returns an empty response because geofences are asynchronously
                  evaluated. The evaluation determines if the device has entered
                  or exited a geofenced area, and then publishes one of the
                  following events to Amazon EventBridge:</p> <ul> <li> <p>
                  <code>ENTER</code> if Amazon Location determines that the
                  tracked device has entered a geofenced area.</p> </li> <li>
                  <p> <code>EXIT</code> if Amazon Location determines that the
                  tracked device has exited a geofenced area.</p> </li> </ul>
                  <note> <p>The last geofence that a device was observed within
                  is tracked for 30 days after the most recent device position
                  update.</p> </note> <note> <p>Geofence evaluation uses the
                  given device position. It does not account for the optional
                  <code>Accuracy</code> of a
                  <code>DevicePositionUpdate</code>.</p> </note> <note> <p>The
                  <code>DeviceID</code> is used as a string to represent the
                  device. You do not need to have a <code>Tracker</code>
                  associated with the <code>DeviceID</code>.</p> </note>
                tags:
                  - Batches
                  - Evaluate
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
            /tracking/v0/trackers/{TrackerName}/get-positions:
              POST:
                summary: BatchGetDevicePosition
                description: >-
                  <p>Lists the latest device positions for requested
                  devices.</p>
                tags:
                  - Batches
                  - Get
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
            /geofencing/v0/collections/{CollectionName}/put-geofences:
              POST:
                summary: BatchPutGeofence
                description: >-
                  <p>A batch request for storing geofence geometries into a
                  given geofence collection, or updates the geometry of an
                  existing geofence if a geofence ID is included in the
                  request.</p>
                tags:
                  - Batches
                  - Put
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
            /tracking/v0/trackers/{TrackerName}/positions:
              POST:
                summary: BatchUpdateDevicePosition
                description: >-
                  <p>Uploads position update data for one or more devices to a
                  tracker resource (up to 10 devices per batch). Amazon Location
                  uses the data when it reports the last known device position
                  and position history. Amazon Location retains location data
                  for 30 days.</p> <note> <p>Position updates are handled based
                  on the <code>PositionFiltering</code> property of the tracker.
                  When <code>PositionFiltering</code> is set to
                  <code>TimeBased</code>, updates are evaluated against linked
                  geofence collections, and location data is stored at a maximum
                  of one position per 30 second interval. If your update
                  frequency is more often than every 30 seconds, only one update
                  per 30 seconds is stored for each unique device ID.</p>
                  <p>When <code>PositionFiltering</code> is set to
                  <code>DistanceBased</code> filtering, location data is stored
                  and evaluated against linked geofence collections only if the
                  device has moved more than 30 m (98.4 ft).</p> <p>When
                  <code>PositionFiltering</code> is set to
                  <code>AccuracyBased</code> filtering, location data is stored
                  and evaluated against linked geofence collections only if the
                  device has moved more than the measured accuracy. For example,
                  if two consecutive updates from a device have a horizontal
                  accuracy of 5 m and 10 m, the second update is neither stored
                  or evaluated if the device has moved less than 15 m. If
                  <code>PositionFiltering</code> is set to
                  <code>AccuracyBased</code> filtering, Amazon Location uses the
                  default value <code>{ "Horizontal": 0}</code> when accuracy is
                  not provided on a <code>DevicePositionUpdate</code>.</p>
                  </note>
                tags:
                  - Batches
                  - Update
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
            /routes/v0/calculators/{CalculatorName}/calculate/route:
              POST:
                summary: CalculateRoute
                description: >-
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/calculate-route.html">Calculates
                  a route</a> given the following required parameters:
                  <code>DeparturePosition</code> and
                  <code>DestinationPosition</code>. Requires that you first <a
                  href="https://docs.aws.amazon.com/location-routes/latest/APIReference/API_CreateRouteCalculator.html">create
                  a route calculator resource</a>.</p> <p>By default, a request
                  that doesn't specify a departure time uses the best time of
                  day to travel with the best traffic conditions when
                  calculating the route.</p> <p>Additional options include:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/departure-time.html">Specifying
                  a departure time</a> using either <code>DepartureTime</code>
                  or <code>DepartNow</code>. This calculates a route based on
                  predictive traffic data at the given time. </p> <note> <p>You
                  can't specify both <code>DepartureTime</code> and
                  <code>DepartNow</code> in a single request. Specifying both
                  parameters returns a validation error.</p> </note> </li> <li>
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/travel-mode.html">Specifying
                  a travel mode</a> using TravelMode sets the transportation
                  mode used to calculate the routes. This also lets you specify
                  additional route preferences in <code>CarModeOptions</code> if
                  traveling by <code>Car</code>, or
                  <code>TruckModeOptions</code> if traveling by
                  <code>Truck</code>.</p> <note> <p>If you specify
                  <code>walking</code> for the travel mode and your data
                  provider is Esri, the start and destination must be within
                  40km.</p> </note> </li> </ul>
                tags:
                  - Calculate
                  - Routes
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
            /routes/v0/calculators/{CalculatorName}/calculate/route-matrix:
              POST:
                summary: CalculateRouteMatrix
                description: >-
                  <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/calculate-route-matrix.html">
                  Calculates a route matrix</a> given the following required
                  parameters: <code>DeparturePositions</code> and
                  <code>DestinationPositions</code>.
                  <code>CalculateRouteMatrix</code> calculates routes and
                  returns the travel time and travel distance from each
                  departure position to each destination position in the
                  request. For example, given departure positions A and B, and
                  destination positions X and Y,
                  <code>CalculateRouteMatrix</code> will return time and
                  distance for routes from A to X, A to Y, B to X, and B to Y
                  (in that order). The number of results returned (and routes
                  calculated) will be the number of
                  <code>DeparturePositions</code> times the number of
                  <code>DestinationPositions</code>.</p> <note> <p>Your account
                  is charged for each route calculated, not the number of
                  requests.</p> </note> <p>Requires that you first <a
                  href="https://docs.aws.amazon.com/location-routes/latest/APIReference/API_CreateRouteCalculator.html">create
                  a route calculator resource</a>.</p> <p>By default, a request
                  that doesn't specify a departure time uses the best time of
                  day to travel with the best traffic conditions when
                  calculating routes.</p> <p>Additional options include:</p>
                  <ul> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/departure-time.html">
                  Specifying a departure time</a> using either
                  <code>DepartureTime</code> or <code>DepartNow</code>. This
                  calculates routes based on predictive traffic data at the
                  given time. </p> <note> <p>You can't specify both
                  <code>DepartureTime</code> and <code>DepartNow</code> in a
                  single request. Specifying both parameters returns a
                  validation error.</p> </note> </li> <li> <p> <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/travel-mode.html">Specifying
                  a travel mode</a> using TravelMode sets the transportation
                  mode used to calculate the routes. This also lets you specify
                  additional route preferences in <code>CarModeOptions</code> if
                  traveling by <code>Car</code>, or
                  <code>TruckModeOptions</code> if traveling by
                  <code>Truck</code>.</p> </li> </ul>
                tags:
                  - Calculate
                  - Routes
                  - Matrix
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
            /geofencing/v0/collections:
              POST:
                summary: CreateGeofenceCollection
                description: >-
                  <p>Creates a geofence collection, which manages and stores
                  geofences.</p>
                tags:
                  - Create
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
            /metadata/v0/keys:
              POST:
                summary: CreateKey
                description: >-
                  <p>Creates an API key resource in your Amazon Web Services
                  account, which lets you grant actions for Amazon Location
                  resources to the API key bearer.</p> <note> <p>For more
                  information, see <a
                  href="https://docs.aws.amazon.com/location/latest/developerguide/using-apikeys.html">Using
                  API keys</a>.</p> </note>
                tags:
                  - Create
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
            /maps/v0/maps:
              POST:
                summary: CreateMap
                description: >-
                  <p>Creates a map resource in your Amazon Web Services account,
                  which provides map tiles of different styles sourced from
                  global location data providers.</p> <note> <p>If your
                  application is tracking or routing assets you use in your
                  business, such as delivery vehicles or employees, you must not
                  use Esri as your geolocation provider. See section 82 of the
                  <a href="http://aws.amazon.com/service-terms">Amazon Web
                  Services service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
            /places/v0/indexes:
              POST:
                summary: CreatePlaceIndex
                description: >-
                  <p>Creates a place index resource in your Amazon Web Services
                  account. Use a place index resource to geocode addresses and
                  other text queries by using the
                  <code>SearchPlaceIndexForText</code> operation, and reverse
                  geocode coordinates by using the
                  <code>SearchPlaceIndexForPosition</code> operation, and enable
                  autosuggestions by using the
                  <code>SearchPlaceIndexForSuggestions</code> operation.</p>
                  <note> <p>If your application is tracking or routing assets
                  you use in your business, such as delivery vehicles or
                  employees, you must not use Esri as your geolocation provider.
                  See section 82 of the <a
                  href="http://aws.amazon.com/service-terms">Amazon Web Services
                  service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Places
                  - Index
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
            /routes/v0/calculators:
              POST:
                summary: CreateRouteCalculator
                description: >-
                  <p>Creates a route calculator resource in your Amazon Web
                  Services account.</p> <p>You can send requests to a route
                  calculator resource to estimate travel time, distance, and get
                  directions. A route calculator sources traffic and road
                  network data from your chosen data provider.</p> <note> <p>If
                  your application is tracking or routing assets you use in your
                  business, such as delivery vehicles or employees, you must not
                  use Esri as your geolocation provider. See section 82 of the
                  <a href="http://aws.amazon.com/service-terms">Amazon Web
                  Services service terms</a> for more details.</p> </note>
                tags:
                  - Create
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
            /tracking/v0/trackers:
              POST:
                summary: CreateTracker
                description: >-
                  <p>Creates a tracker resource in your Amazon Web Services
                  account, which lets you retrieve current and historical
                  location of devices.</p>
                tags:
                  - Create
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
            /geofencing/v0/collections/{CollectionName}:
              PATCH:
                summary: UpdateGeofenceCollection
                description: >-
                  <p>Updates the specified properties of a given geofence
                  collection.</p>
                tags:
                  - Update
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
            /metadata/v0/keys/{KeyName}:
              PATCH:
                summary: UpdateKey
                description: >-
                  <p>Updates the specified properties of a given API key
                  resource.</p>
                tags:
                  - Update
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
            /maps/v0/maps/{MapName}:
              PATCH:
                summary: UpdateMap
                description: >-
                  <p>Updates the specified properties of a given map
                  resource.</p>
                tags:
                  - Update
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
            /places/v0/indexes/{IndexName}:
              PATCH:
                summary: UpdatePlaceIndex
                description: >-
                  <p>Updates the specified properties of a given place index
                  resource.</p>
                tags:
                  - Update
                  - Places
                  - Index
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /routes/v0/calculators/{CalculatorName}:
              PATCH:
                summary: UpdateRouteCalculator
                description: >-
                  <p>Updates the specified properties for a given route
                  calculator resource.</p>
                tags:
                  - Update
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /tracking/v0/trackers/{TrackerName}:
              PATCH:
                summary: UpdateTracker
                description: >-
                  <p>Updates the specified properties of a given tracker
                  resource.</p>
                tags:
                  - Update
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
            /tracking/v0/trackers/{TrackerName}/consumers/{ConsumerArn}:
              DELETE:
                summary: DisassociateTrackerConsumer
                description: >-
                  <p>Removes the association between a tracker resource and a
                  geofence collection.</p> <note> <p>Once you unlink a tracker
                  resource from a geofence collection, the tracker positions
                  will no longer be automatically evaluated against
                  geofences.</p> </note>
                tags:
                  - Disassociate
                  - Trackers
                  - Consumer
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
            /tracking/v0/trackers/{TrackerName}/devices/{DeviceId}/positions/latest:
              GET:
                summary: GetDevicePosition
                description: >-
                  <p>Retrieves a device's most recent position according to its
                  sample time.</p> <note> <p>Device positions are deleted after
                  30 days.</p> </note>
                tags:
                  - Get
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
            /tracking/v0/trackers/{TrackerName}/devices/{DeviceId}/list-positions:
              POST:
                summary: GetDevicePositionHistory
                description: >-
                  <p>Retrieves the device position history from a tracker
                  resource within a specified range of time.</p> <note>
                  <p>Device positions are deleted after 30 days.</p> </note>
                tags:
                  - Get
                  - Device
                  - Positions
                  - History
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
            /geofencing/v0/collections/{CollectionName}/geofences/{GeofenceId}:
              PUT:
                summary: PutGeofence
                description: >-
                  <p>Stores a geofence geometry in a given geofence collection,
                  or updates the geometry of an existing geofence if a geofence
                  ID is included in the request. </p>
                tags:
                  - Put
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
            /maps/v0/maps/{MapName}/glyphs/{FontStack}/{FontUnicodeRange}:
              GET:
                summary: GetMapGlyphs
                description: <p>Retrieves glyphs used to display labels on a map.</p>
                tags:
                  - Get
                  - Maps
                  - Glyphs
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
            /maps/v0/maps/{MapName}/sprites/{FileName}:
              GET:
                summary: GetMapSprites
                description: >-
                  <p>Retrieves the sprite sheet corresponding to a map resource.
                  The sprite sheet is a PNG image paired with a JSON document
                  describing the offsets of individual icons that will be
                  displayed on a rendered map.</p>
                tags:
                  - Get
                  - Maps
                  - Sprites
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
            /maps/v0/maps/{MapName}/style-descriptor:
              GET:
                summary: GetMapStyleDescriptor
                description: >-
                  <p>Retrieves the map style descriptor from a map resource.
                  </p> <p>The style descriptor contains speciﬁcations on how
                  features render on a map. For example, what data to display,
                  what order to display the data in, and the style for the data.
                  Style descriptors follow the Mapbox Style Specification.</p>
                tags:
                  - Get
                  - Maps
                  - Styles
                  - Descriptions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
            /maps/v0/maps/{MapName}/tiles/{Z}/{X}/{Y}:
              GET:
                summary: GetMapTile
                description: >-
                  <p>Retrieves a vector data tile from the map resource. Map
                  tiles are used by clients to render a map. they're addressed
                  using a grid arrangement with an X coordinate, Y coordinate,
                  and Z (zoom) level. </p> <p>The origin (0, 0) is the top left
                  of the map. Increasing the zoom level by 1 doubles both the X
                  and Y dimensions, so a tile containing data for the entire
                  world at (0/0/0) will be split into 4 tiles at zoom 1 (1/0/0,
                  1/0/1, 1/1/0, 1/1/1).</p>
                tags:
                  - Get
                  - Maps
                  - Tiles
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
            /places/v0/indexes/{IndexName}/places/{PlaceId}:
              GET:
                summary: GetPlace
                description: >-
                  <p>Finds a place by its unique ID. A <code>PlaceId</code> is
                  returned by other search operations.</p> <note> <p>A PlaceId
                  is valid only if all of the following are the same in the
                  original search request and the call to
                  <code>GetPlace</code>.</p> <ul> <li> <p>Customer Amazon Web
                  Services account</p> </li> <li> <p>Amazon Web Services
                  Region</p> </li> <li> <p>Data provider specified in the place
                  index resource</p> </li> </ul> </note>
                tags:
                  - Get
                  - Places
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /tracking/v0/trackers/{TrackerName}/list-positions:
              POST:
                summary: ListDevicePositions
                description: <p>A batch request to retrieve all device positions.</p>
                tags:
                  - Lists
                  - Device
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /geofencing/v0/list-collections:
              POST:
                summary: ListGeofenceCollections
                description: >-
                  <p>Lists geofence collections in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Geofences
                  - Collections
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /geofencing/v0/collections/{CollectionName}/list-geofences:
              POST:
                summary: ListGeofences
                description: <p>Lists geofences stored in a given geofence collection.</p>
                tags:
                  - Lists
                  - Geofences
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /metadata/v0/list-keys:
              POST:
                summary: ListKeys
                description: >-
                  <p>Lists API key resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Keys
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /maps/v0/list-maps:
              POST:
                summary: ListMaps
                description: >-
                  <p>Lists map resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Maps
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /places/v0/list-indexes:
              POST:
                summary: ListPlaceIndexes
                description: >-
                  <p>Lists place index resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Places
                  - Indexes
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /routes/v0/list-calculators:
              POST:
                summary: ListRouteCalculators
                description: >-
                  <p>Lists route calculator resources in your Amazon Web
                  Services account.</p>
                tags:
                  - Lists
                  - Routes
                  - Calculators
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
            /tags/{ResourceArn}:
              DELETE:
                summary: UntagResource
                description: >-
                  <p>Removes one or more tags from the specified Amazon Location
                  resource.</p>
                tags:
                  - Untag
                  - Resources
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /tracking/v0/trackers/{TrackerName}/list-consumers:
              POST:
                summary: ListTrackerConsumers
                description: >-
                  <p>Lists geofence collections currently associated to the
                  given tracker resource.</p>
                tags:
                  - Lists
                  - Trackers
                  - Consumers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /tracking/v0/list-trackers:
              POST:
                summary: ListTrackers
                description: >-
                  <p>Lists tracker resources in your Amazon Web Services
                  account.</p>
                tags:
                  - Lists
                  - Trackers
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
            /places/v0/indexes/{IndexName}/search/position:
              POST:
                summary: SearchPlaceIndexForPosition
                description: >-
                  <p>Reverse geocodes a given coordinate and returns a legible
                  address. Allows you to search for Places or points of interest
                  near a given position.</p>
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Positions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
            /places/v0/indexes/{IndexName}/search/suggestions:
              POST:
                summary: SearchPlaceIndexForSuggestions
                description: >-
                  <p>Generates suggestions for addresses and points of interest
                  based on partial or misspelled free-form text. This operation
                  is also known as autocomplete, autosuggest, or fuzzy
                  matching.</p> <p>Optional parameters let you narrow your
                  search results by bounding box or country, or bias your search
                  toward a specific position on the globe.</p> <note> <p>You can
                  search for suggested place names near a specified position by
                  using <code>BiasPosition</code>, or filter results within a
                  bounding box by using <code>FilterBBox</code>. These
                  parameters are mutually exclusive; using both
                  <code>BiasPosition</code> and <code>FilterBBox</code> in the
                  same command returns an error.</p> </note>
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Suggestions
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
                  - Suggestions
            /places/v0/indexes/{IndexName}/search/text:
              POST:
                summary: SearchPlaceIndexForText
                description: >-
                  <p>Geocodes free-form text, such as an address, name, city, or
                  region to allow you to search for Places or points of
                  interest. </p> <p>Optional parameters let you narrow your
                  search results by bounding box or country, or bias your search
                  toward a specific position on the globe.</p> <note> <p>You can
                  search for places near a given position using
                  <code>BiasPosition</code>, or filter results within a bounding
                  box using <code>FilterBBox</code>. Providing both parameters
                  simultaneously returns an error.</p> </note> <p>Search results
                  are returned in order of highest to lowest rele
                tags:
                  - Search
                  - Places
                  - Index
                  - For
                  - Text
                  - Trackers
                  - Names
                  - Consumers
                  - Delete
                  - Positions
                  - Collections
                  - Geofences
                  - Get
                  - Put
                  - Calculators
                  - Calculate
                  - Routes
                  - Matrix
                  - Geofencing
                  - V0
                  - Collections
                  - Metadata
                  - Keys
                  - Maps
                  - Places
                  - Indexes
                  - Routes
                  - Calculators
                  - Tracking
                  - Trackers
                  - Keys
                  - Maps
                  - Index
                  - Consumer
                  - ARN
                  - Devices
                  - Device
                  - Identifiers
                  - Latest
                  - Lists
                  - Geofences
                  - Glyphs
                  - Fonts
                  - Stack
                  - Unicode
                  - Ranges
                  - Sprites
                  - File
                  - Styles
                  - Descriptions
                  - Tiles
                  - Places
                  - Resources
                  - Search
                  - Positions
                  - Suggestions
                  - Te
    overlays:
      - type: APIs.io Search
        url: overlays/location-openapi-search.yml
      - type: API Evangelist Ratings
        url: overlays/location-openapi-api-evangelist-ratings.yml
    aid: amazon-web-services:location
maintainers:
  - FN: API Evangelist
    email: info@apievangelist.com
---