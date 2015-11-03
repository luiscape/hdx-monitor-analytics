### HDX Monitor Analytics
Analytics application to analyze data from a CKAN instance. Designed to use [`Metabase`](https://github.com/metabase/metabase) as its front end. This application contains a container that fetches data from a CKAN instance, creating a `PostgreSQL` database with relevant objects for analysis. This is easily deployable and doesn't neet sysadmin priviledges to the CKAN database.

### Usage
This repository only contains the `docker-compose.yml` instructions to setting up the applicaton. To deploy the application in your envirionment, please run:

```shell
$ git clone [THIS_REPOSITORY] && cd [FOLDER]
$ docker-compose up -d
```

Docker will download the necessary images from the registry and start the application. Navigate to `localhost:4000` to setup `Metabase` and start using the appliction. However, keep in mind that the `hdx-monitor-sql-collector` will take about an hour to collect all the data from the CKAN instance configured on the `CKAN_URL` environment variable of the `docker-compose.yml` file.
