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

## Changes

### 2.4.2024

#### Dashboard

- data from object _"Data"_ in technologies moved to objects in parent object, as only a single record is used

#### Notifications

- Added endpoint _"/api/Notifications/NotificationsTypes"_

<!-- #### Device

- DeviceDashboard
  - timeseries simplified by moving to separate object -->

#### Technology

- TechnologyDashboard
  - timeseries simplified by moving to separate object
