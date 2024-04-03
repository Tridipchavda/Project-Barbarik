# Bus Transport Backend

## Prerequesites
- PostgresDB
- Go Lang
  
## Run Go Server
1. Make .env File as per .env.sample and Edit it with Your Database ,Username, Passsword etc.
2. Take the Dump File and Import in Your Local Database
   
   With Opening psql terminal
```
\i Path\to\dump.sql
```
 OR <br></br>
With Direct From Terminal In Linux
```
sudo -u postgres psql db_name < 'file_path'
```

3. Import All Modules in Go
```
go mod tidy
go get
```

4. Running Server at Given Port in Env :
```
go run main.go
```

## API STRUCTURE:
-   Bus
    |METHOD|ENDPOINT|
    |------|--------|
    |GET|/bus/ |
    |POST|/bus/ |
    |POST|/bus/{id} |
    |POST|/live/update/ |

-   Driver
    |METHOD|ENDPOINT|
    |------|--------|
    |GET|/driver/ |
    |POST|/driver/ |
    |POST|/driver/{id} |

-   Route
    |METHOD|ENDPOINT|
    |------|--------|
    |GET|/route/
    |POST|/route/
    |POST|/route/{id}

-   RouteStation
    |METHOD|ENDPOINT|
    |------|--------|
    |GET|/routeStation/
    |POST|/routeStation/
    |POST|/routeStation/{id}

-   Station
    |METHOD|ENDPOINT|
    |------|--------|
    |GET|/station/
    |POST|/station/
    |POST|/station/{id}

-   Schedule
    |METHOD|ENDPOINT|
    |------|--------|
    |GET|/schedule/
    |POST|/schedule/
    |POST|/schedule/{id}
