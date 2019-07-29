# Fetch district names using (amend REGD16NM to name of county):
https://services1.arcgis.com/ESMARspQHYMw9BZ9/arcgis/rest/services/WD16_REGD16_LAD16_EW_LU/FeatureServer/0/query?where=REGD16NM+like+%27%25Cambridgeshire%25%27&objectIds=&time=&resultType=none&outFields=LAD16NM&returnIdsOnly=false&returnCountOnly=false&returnDistinctValues=true&orderByFields=&groupByFieldsForStatistics=&outStatistics=&resultOffset=&resultRecordCount=&sqlFormat=none&f=pjson&token=

# Fetch district geometries using lad16nm:
https://ons-inspire.esriuk.com/arcgis/rest/services/Administrative_Boundaries/Local_Authority_Districts_December_2016_Boundaries/MapServer/2/query?where=UPPER(lad16nm)%20like%20%27%25CAMBRIDGE%25%27&outFields=objectid,lad16cd,lad16nm,lad16nmw,bng_e,bng_n,long,lat&outSR=4326&f=json

# Fetch ward names within a district (amend LAD16NM):
https://services1.arcgis.com/ESMARspQHYMw9BZ9/arcgis/rest/services/WD16_REGD16_LAD16_EW_LU/FeatureServer/0/query?where=LAD16NM+like+%27%25Broadland%25%27&objectIds=&time=&resultType=none&outFields=*&returnIdsOnly=false&returnCountOnly=false&returnDistinctValues=false&orderByFields=&groupByFieldsForStatistics=&outStatistics=&resultOffset=&resultRecordCount=&sqlFormat=none&f=pjson&token=

# Fetch ward geometries using wd16nm:
https://ons-inspire.esriuk.com/arcgis/rest/services/Administrative_Boundaries/Wards_December_2016_Boundaries/MapServer/2/query?where=UPPER(wd16nm)%20like%20%27%25THORPE%20ST%20ANDREW%20SOUTH%20EAST%25%27&outFields=objectid,wd16cd,wd16nm,wd16nmw,lad16cd,lad16nm,long,lat&outSR=4326&f=json

# Fetch ward geometries using wd16cd:
https://ons-inspire.esriuk.com/arcgis/rest/services/Administrative_Boundaries/Wards_December_2016_Boundaries/MapServer/2/query?where=UPPER(wd16cd)%20like%20%27%25E05005758%25%27&outFields=objectid,wd16cd,wd16nm,wd16nmw,lad16cd,lad16nm,long,lat&outSR=4326&f=json