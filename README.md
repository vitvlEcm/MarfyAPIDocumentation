# ECM web API

## Endpoints

- [Auth](/Endpoints/Auth.md)
- [Dashboard](/Endpoints/Dashboard.md)
- [Device](/Endpoints/Device.md)
- [Notifications](/Endpoints/Notifications.md)
- [Organization](/Endpoints/Organization.md)
- [Settings](/Endpoints/Settings.md)
- [Stats](/Endpoints/Stats.md)
- [Technology](/Endpoints/Technology.md)
- [User](/Endpoints/User.md)

## Use Cases

[UseCases](/Endpoints/UseCases.md)

## Changes

### 2.4.2024

#### Dashboard

- data from object _"Data"_ in technologies moved to objects in parent object, as only a single record is used

#### Notifications

- Added endpoint _"/api/Notifications/NotificationsTypes"_

#### Device

- DeviceDashboard
  - timeseries simplified by moving to separate object
  - added parameters for device name and id

#### Technology

- TechnologyDashboard

  - timeseries simplified by moving to separate object

### 6.4.2024

- TechnologiesForNode

  - returned object was simplified as requested on call with Petr, removed nested object _"Data"_ and contents moved to parent

- removed unused parameters sourceUnit and manualUnit from multiple responses

- parameters typeId, typename => technologyId, technologyName on several places. TypeId, typename kept to avoid breaking old mappings. Should be deleted if OK
