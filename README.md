#bom-api#

node wrapper for BOM (bereau of meteorology) api

Takes 

#Use#

    npm install bom-api 

    var bom = require('bom-api');

Example:

    bom.getBomDataByLatitudeLongitude(lat, lng, functions(data){
        //do stuff with data;
    });

Takes latitude and longitude parameters and returns an array of recent climate data.

    bom.getBomDataBySiteNumberState(siteNumber, stateName, function(error, data)){
        // do stuff with data
    });

Takes a BoM site number (http://www.bom.gov.au/climate/cdo/about/site-num.shtml) and state code (eg: 'qld' ) and returns an array of recent climate data.



Example of the returned data from bomInfoArray.

    [{
        air_temp: 24.5,
        apparent_t: 25.8,
        rel_hum: 60,
        local_date_time_full: "20140522120000",
        utc_date_time_full: "20140522020000"
    },
    {
        air_temp: 24.9,
        apparent_t: 26.5,
        rel_hum: 61,
        local_date_time_full: "20140522113000",
        utc_date_time_full: "20140522013000"
    },
    {
        air_temp: 23.1,
        apparent_t: 24.1,
        rel_hum: 66,
        local_date_time_full: "20140522110000",
        utc_date_time_full: "20140522010000"
    }........