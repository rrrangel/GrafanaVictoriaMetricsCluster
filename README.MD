# Docker Compose for Grafana and Victoria Metrics

This repository contains a Docker Compose file that sets up Grafana and Victoria Metrics.

## Services

The `docker-compose.yml` file defines the following services:

### VictoriaMetrics

VictoriaMetrics is a fast, cost-effective, and scalable time series database. It's compatible with Prometheus querying, long-term storage, and Grafana dashboarding.

In our setup, VictoriaMetrics is configured to store its data in a Docker volume named `victoria-metrics-data`.

### Grafana

Grafana is a multi-platform open-source analytics and interactive visualization web application. It provides charts, graphs, and alerts for the web when connected to supported data sources.

In our setup, Grafana is configured to store its data in a Docker volume named `grafana-storage`.

## Usage

To start the services, navigate to the directory containing the `docker-compose.yml` file and run the following command:

### bash </br>
`docker-compose up -d`

After starting the services, you can access Grafana at http://localhost:3000 and add Victoria Metrics as a data source using the URL http://victoriametrics:8428.

Please note that you might need to adjust this configuration according to your specific needs. For example, you might want to add environment variables for setting up Grafana or use a custom configuration file.

## Conclusion
This README provides a brief overview of the services defined in the Docker Compose file and instructions on how to use them. You can add more details based on your specific needs and setup.

Let me know if you need further assistance! 😊


## TO DO
- Look into persistance in volumes
    - Grafana does not persist at the moment
- Document VMAgent and ingestion