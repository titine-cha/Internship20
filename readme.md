# Metals in biota data

This repo contains data on metal concentrations in biota as collected by NRM in Swedish lakes, for more information see [this report](http://nrm.diva-portal.org/smash/record.jsf?pid=diva2%3A1343153&dswid=5544).

### File `LIMN_metals.csv`

This contains the measurements.

| Column| Contents|
|-------|---------|
|`ACCNR` | Accession number, unique identifier assigned to individual (fish).|
|`PARAMETER_NAME` |  Name of substance (SWE).|
|`PARAMETER_CODE`| Code of substance according to [this list](http|//gis-services.metria.se/kodlistor/index.htm).|
|`PARAMETER_CODE_NRM`| Code of substance used by NRM. Note that this also contains info on lab, e.g. HGFS and HGFSI both refer to mercury but with concentration measured by different labs.|
|`YEAR`| Year of accession.|
|`DATE_COLLECTED`| Date individual was collected/caught.|
|`STATION_CODE_NRM`| Lake, as coded by NRM. See `LIMN_stations.csv`.|
|`GENUS`| Species (ESOX = Pike, PERC = Perch, RUTI = Roach, SALV = Arctic char).|
|`ORGAN`| Part of fish analysed (muscle for mercury and liver for other metals).|
|`LAB`| Laboratory performing the analysis.|
|`VALUE`| Measured concentration. If the concentration is below the level of quantification (LOQ) this is reported as a negative number (-LOQ).|
|`VALUE_UNIT`| Unit of measurement.|
|`LIVER_DW_PRC`| Dry-weight percentage, liver sample.|
|`MUSCLE_DW_PRC`| Dry-weight percentage, muscle sample.|
|`LENGTH`| Length of fish.|
|`WEIGHT`| Weight of fish.|
|`AGE`| Age of fish.|
|`SEX`| Sex of fish.|

### File `LIMN_metals.csv`

This contains information on the lakes/stations.

| Column| Contents|
|-------|---------|
|`STATION_CODE_NRM`| NRM code of lake, key to join with `LIMN_metals.csv`|
|`STATION_NAME` | Name of lake|
|`STATION_CODE`| Code of sampling location as listed in [stationsregistret](https://stationsregister.miljodatasamverkan.se/stationsregister/composer/). This could possibly be used to link with other sources, but larger lakes most likely have multiple locations.|
|`POS_SWEREF_TM_N`| Position, see [SWEREF](https://www.lantmateriet.se/sv/Kartor-och-geografisk-information/gps-geodesi-och-swepos/referenssystem/tvadimensionella-system/sweref-99-projektioner/)|
|`POS_SWEREF_TM_E`| Position, see [SWEREF](https://www.lantmateriet.se/sv/Kartor-och-geografisk-information/gps-geodesi-och-swepos/referenssystem/tvadimensionella-system/sweref-99-projektioner/)|