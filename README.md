MDM Geomap Demo – Indonesia
==========================

Project Overview
----------------
This repository provides a demo dataset and reference setup for visualizing
Mobile Device Management (MDM) devices across Indonesian cities using Grafana
Geomap.

The project is designed for:
- Executive demos
- Proof of Concept (POC)
- Presales & architecture discussions
- Internal training and visualization examples

All data in this repository is 100% simulated and contains no real user,
device, or location data.


Use Case Scenario
-----------------
The main scenario demonstrated in this project is:

"How to visually monitor the distribution, compliance, and risk level of
managed Android devices across Indonesia in a single geographic dashboard."

Typical use cases include:
- Retail tablet deployment monitoring
- Field sales device visibility
- Warehouse & logistics device compliance
- Security posture overview for mobile endpoints


Dataset Description
-------------------
File name:
mdm_devices_indonesia_demo_200.csv

Total records:
200 devices

Geographic scope:
Indonesia only (major cities across multiple regions)

The dataset is suitable for direct use in Grafana Geomap panels.


CSV Columns
-----------
device_id
    Unique identifier for each device

device_name
    Human-readable device name

owner
    Business unit owning the device
    (Store / Sales / Warehouse)

city
    City where the device is located

province
    Province name

lat
    Latitude coordinate (WGS84)

lon
    Longitude coordinate (WGS84)

compliance
    Device compliance status:
    - Compliant
    - Warning
    - Non-Compliant

battery
    Battery level percentage (0–100)

os_version
    Android OS version (11–14)

device_type
    Device form factor (Tablet / Phone)

last_seen
    Last check-in time (minutes or hours)

risk_level
    Overall risk classification:
    - Low
    - Medium
    - High


Grafana Usage
-------------
Recommended setup:

1. Upload the CSV file to a public GitHub repository
2. Use the RAW file URL, for example:
   https://raw.githubusercontent.com/USERNAME/REPO/main/mdm_devices_indonesia_demo_200.csv

3. In Grafana, use one of the following data sources:
   - Infinity Plugin (recommended)
   - CSV Data Source

4. Create a Geomap panel with:
   - Latitude field: lat
   - Longitude field: lon
   - Label: device_name
   - Color by value: compliance
   - Tooltip fields:
     owner, battery, os_version, risk_level


Map & Visualization
-------------------
Base map:
OpenStreetMap (default Grafana base map)

Recommended color mapping:
- Green  : Compliant
- Yellow : Warning
- Red    : Non-Compliant

This configuration allows fast visual identification of:
- Non-compliant devices
- High-risk areas
- Device distribution by region


Data Disclaimer
---------------
- All data is fictional and generated for demo purposes only
- Coordinates represent approximate city locations
- No real tracking, monitoring, or personal data is included
- Safe for public repositories and presentations


Recommended Extensions
----------------------
This demo can be extended with:
- Executive KPI dashboards
- Compliance percentage panels
- Offline device detection
- Lost or stolen device scenarios
- Integration with real MDM platforms (API-based)


License
-------
This project is provided for demonstration and educational purposes.
Free to use, modify, and adapt for internal demos and presentations.


Author / Notes
--------------
Created as a simple, fast, and practical reference for
MDM Geomap visualization using Grafana and CSV-based data sources.
