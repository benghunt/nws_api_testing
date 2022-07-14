# nws_api_testing

currently this is a place for notebooks which help test NWS data products

There is a notebook for exploring NWS products: different from their gridpoint forecasts,
NWS offices publish a variety of text products used by local groups
This is a way to easily access them and read them in plaintext

Also we have a test of the NWS coordinates -> gridpoints forecast endpoint
looks like about 12-15% of the time the NWS points a lat/lon coordinate to a grid about 1-2 miles from the coordinate
not sure why this is but here you can test it on a list of the top 1000 us cities by population

#edit: have found a successful workaround: the actual grid is (gridX-1,gridY-1) for 40/40 cities that are outside the NWS grid endpoint. This test has been committed

You need to install Shapely, numplotlib, and Jupyter to run the NWS gridpoints test script

Despite the bug reports I did not find any "old data" in the gridpoints
