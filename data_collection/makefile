all: data state_boundaries

data:
	# Write USArrests dataset built into R to a csv file
	R --no-save -e "write.csv(USArrests, 'USArrests.csv', row.names=TRUE)"

state_boundaries:
	# Collect state boundary data from US Census Bureau
	# https://www2.census.gov/geo/tiger/GENZ2021/shp/cb_2021_us_state_20m.zip
	curl "https://www2.census.gov/geo/tiger/GENZ2021/shp/cb_2021_us_state_20m.zip" -o cb_2021_us_state_20m.zip
	unzip cb_2021_us_state_20m.zip -d cb_2021_us_state_20m/
