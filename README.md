

Available at https://dash.vaex.io/

```
$ python app.py
```

```
$ python getdata.py
```


Run in production mode (make sure the data is downloaded if you stream from s3):
```
$ VAEX_NUM_THREADS=8 gunicorn -w 16 app:server -b 0.0.0.0:8050
```

## Settings
Change settings in the dash app
```
$ export TAXI_PATH=/data/taxi/yellow_taxi_2012_zones.hdf5  # change the default s3 file
$ export VAEX_NUM_THREADS=16     # change the number of threads per process/worker
$ export DASH_CACHE_TIMEOUT=240  # increase cache timeout to 4 minutes
$ export DASH_CACHE_TIMEOUT=-1  # disable cache (useful for benchmarking)
```
