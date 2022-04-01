# kata-test
test of unvt/kata using NaturalEarth data

# Source data
Small scale data from Natural Earth https://www.naturalearthdata.com/ (Downloaded on 2022-03-31)

* ne_110m_admin_0_boundary_lines_land.shp
* ne_110m_coastline.shp
* ne_110m_graticules_30.shp
* ne_110m_lakes.shp
* ne_110m_land.shp
* ne_110m_ocean.shp
* ne_110m_populated_places.shp
* ne_110m_rivers_lake_centerlines.shp


# Flow
1. Convert geojson from shapefile (ogr2ogr)
2. apply kata filter
3. use tippecanoe-json-tool to remove FeatureCollecation wrap
4. Forward geojson into tippecanoe


# Progress
Because filterd ndjson is wrapped as FeatureCollection, I have some challenges now (as of 2022-3-31)