# era5get

## help info:

- era5wrf

```
usage: era5wrf [-h] [-d DATE] [-a AREA] [-p PATH] {e5pl,e5sfc,e5land}

Retrive ERA5 hourly data from cds as forcing of WRF

positional arguments:
  {e5pl,e5sfc,e5land}   Category, currently accepts the following options: e5pl
                        (ERA5 data on pressure levels) | e5sfc (ERA5 data on 
                        single level) | e5land (ERA5-land)

options:
  -h, --help            show this help message and exit
  -d DATE, --date DATE  Specify on which dates data should be retrieved 
                        acceptable formats: YYYY (days in YYYY) | YYYYMM (days 
                        in YYYYMM) | YYYYMMDD (this day) | yyyy-YYYY (days in 
                        years between yyyy and YYYY) | yyyymm-YYYYMM (days in 
                        months between yyyymm and YYYYMM) | yyyymmdd-YYYYMMDD 
                        (days between the two dates)
  -a AREA, --area AREA  Specify the area within which data should be retrieved
                        in format of NN,WW,SS,EE
  -p PATH, --path PATH  Specify the directory to store the grib files
```

- era5get

```
usage: era5get [-h] [-d DATE] [-u UPDATES] [-p PATH] opt

Retrive ERA5 data from cds according to a yaml file and modifications

positional arguments:
  opt                   Category, currently accepts the following options: e5pl
                        (ERA5 data on pressure levels) | e5sfc (ERA5 data on
                        single level) | e5land (ERA5-land) | yaml file

options:
  -h, --help            show this help message and exit
  -d DATE, --date DATE  Specify on which dates/months data should be retrieved
                        acceptable formats: YYYY (days/months in YYYY) | YYYYMM
                        (days in YYYYMM or this month) | YYYYMMDD (this day or
                        the month of this day) | yyyy-YYYY (days/months in
                        years between yyyy and YYYY) | yyyymm-YYYYMM (days in
                        months between yyyymm and YYYYMM or these months) |
                        yyyymmdd-YYYYMMDD (days/months between the two dates)
  -u UPDATES, --updates UPDATES
                        Update the second argument to c.retrieve() in format of
                        key0:value0,value1,...;key2:value0,value1,... . f.ex:
                        area:NN,WW,SS,EE
  -p PATH, --path PATH  Specify the directory to store the grib files

```

## what you will need:

```python
import cdsapi
```

## what else you will need:

refer to [cds.climate.copernicus.eu/api-how-to](https://cds.climate.copernicus.eu/api-how-to) 
for help on cdsapi (the Climate Data Store Application Program Interface).
