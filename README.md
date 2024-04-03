# ECM web API

## Endpoints

1. [Dashboard](/Endpoints/Dashboard.md)
1. [Device](/Endpoints/Device.md)
1. [Notifications](/Endpoints/Notifications.md)
1. [Organization](/Endpoints/Organization.md)
1. [Settings](/Endpoints/Settings.md)
1. [Stats](/Endpoints/Stats.md)
1. [Technology](/Endpoints/Technology.md)
1. [User](/Endpoints/User.md)

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
