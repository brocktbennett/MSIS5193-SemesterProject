### Course Information: MSIS 5193
# Team 6
- Yulun Wang, PhD
- Brock Taylor Bennett
- John Ramirez
- Reina Han

# NYPD Arrest Incident Level Data Footnotes

## Overview
This document provides essential footnotes regarding the NYPD Arrest Incident Level Data, as part of the MSIS 5193 Programming for Data Science semester-long project. These notes are critical for understanding the nuances and limitations of the dataset.

### Footnotes
1. **Data Accuracy**: Information is accurate as of the date it was queried from the system of record, but should be considered a close approximation of current records, due to arrest revisions and updates.

2. **Data Availability**: Data is available as of the date that technological enhancements to information systems allowed for data capture. Null values appearing frequently in certain fields may be attributed to changes on official department forms where data was previously not collected. Null values may also appear in instances where information was not available or unknown at the time of the report and should be considered as either “Unknown/Not Available/Not Reported.”

3. **Classification of Charges**: Arrests which involve multiple charges are classified according to the top charge.

4. **Location Representation**: Arrests occurring near an intersection are represented by the X coordinate and Y coordinates of the intersection. Arrests occurring anywhere other than at an intersection are geo-located to the middle of the nearest street segment where appropriate.

5. **Location Approximation**: Any attempt to match the approximate location of the incident to an exact address or link to other datasets is not recommended.

6. **Geo-coding Limitations**: Many other arrests that were not able to be geo-coded (for example, due to an invalid address) have been located as occurring at the police station house within the precinct of occurrence.

7. **Open Area Arrests**: Arrests occurring in open areas such as parks or beaches may be geo-coded as occurring on streets or intersections bordering the area.

8. **Law Codes**: Some arrests do not have specific law codes due to the voluminous amount of laws. The NYPD database contains all NYS Penal Laws but only includes commonly enforced laws from the VTL, Admin Code, etc. As a result, arrests that have law codes similar to “LOC00000UM” represent arrests associated with violations from Transit Rules and Regulations and other such categories.

9. **Transit System Arrests**: Arrests occurring on a moving train on transit systems are geo-coded as occurring at the train’s next stop (street intersection).

10. **Department of Correction Jurisdiction**: All Arrests occurring within the jurisdiction of the Department of Correction have been geo-coded as occurring on Riker’s Island.

11. **Coordinate System (X and Y)**: X and Y Coordinates are in NAD 1983 State Plane New York Long Island Zone Feet (EPSG 2263).

12. **Coordinate System (Latitude and Longitude)**: Latitude and Longitude Coordinates are provided in Global Coordinate System WGS 1984 decimal degrees (EPSG 4326).

13. **Offense Definitions**: The data represents criminal offenses according to New York State Penal Law definitions, not FBI Uniform Crime Report definitions, and are therefore not comparable to UCR reported crime.

14. **Data Transcription Errors**: Errors in data transcription may result in nominal data inconsistencies.

15. **Data Exploration Tools**: The CSV file should be opened using an appropriate tool for data exploration, e.g., SPSS, SAS, Tableau, etc. If using MS Excel, be sure to use the tools for importing external data, otherwise inconsistencies may occur when viewing the data.

16. **Valid Arrests**: Only valid arrests are included in this release. Arrests that were voided when further investigation reveals the person did not commit the offense or it is determined no offense has been committed are excluded from the data set.

17. **Field Names and Descriptions**:
    - **ARREST_KEY**: Randomly generated persistent ID for each arrest
    - **ARREST_DATE**: Exact date of arrest for the reported event
    - **PD_CD**: Three digit internal classification code (more granular than Key Code)
    - **PD_DESC**: Description of internal classification corresponding with PD code (more granular than Offense Description)
    - **KY_CD**: Three digit internal classification code (more general category than PD code)
    - **OFNS_DESC**: Description of internal classification corresponding with KY code (more general category than PD description)
    - **LAW_CODE**: Law code charges corresponding to the NYS Penal Law, VTL and other various local laws
    - **LAW_CAT_CD**: Level of offense: felony, misdemeanor, violation
    - **ARREST_BORO**: Borough of arrest. B(Bronx), S(Staten Island), K(Brooklyn), M(Manhattan), Q(Queens)
    - **ARREST_PRECINCT**: Precinct where the arrest occurred
    - **JURISDICTION_CODE**: Jurisdiction responsible for arrest. Jurisdiction codes 0(Patrol), 1(Transit) and 2(Housing) represent NYPD whilst codes 3 and more represent non NYPD jurisdictions
    - **AGE_GROUP**: Perpetrator’s age within a category
    - **PERP_SEX**: Perpetrator’s sex description
    - **PERP_RACE**: Perpetrator’s race description
    - **X_COORD_CD**: Midblock X-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet (FIPS 3104)
    - **Y_COORD_CD**: Midblock Y-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet (FIPS 3104)
    - **Latitude**: Latitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326)
    - **Longitude**: Longitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326)
