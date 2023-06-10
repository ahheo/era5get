# era5get
## help info
```
usage: era5get [-h] [-d DATE] [-a AREA] [-p PATH] {e5pl,e5sfc,e5land}

Retrive ERA5 hourly data from cds as forcing of WRF

positional arguments:
  {e5pl,e5sfc,e5land}   Category, currently accepts the following options: e5pl (ERA5 data on pressure
                        levels) | e5sfc (ERA5 data on single level) | e5land (ERA5-land)

options:
  -h, --help            show this help message and exit
  -d DATE, --date DATE  Specify on which dates data should be retrieved acceptable formats: YYYY (days 
                        in YYYY) | YYYYMM (days in YYYYMM) | YYYYMMDD (this day) | yyyy-YYYY (days in 
                        years between yyyy and YYYY) | yyyymm-YYYYMM (days in months between yyyymm and
                        YYYYMM) | yyyymmdd-YYYYMMDD (days between the two dates)
  -a AREA, --area AREA  Specify the area wiothin which data should be retrieved: NN,WW,SS,EE
  -p PATH, --path PATH  Specify the directory to store the grib files
```
