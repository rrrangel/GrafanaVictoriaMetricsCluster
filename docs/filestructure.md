# FileStructure

## Local System Side
On your local system, you should have the following files and directories:

``` /my_project
├── docker-compose.yml
└── README.md
```
- `my_project`: This is the root directory of your project. It can be named anything you like.
- `docker-compose.yml`: This is the Docker Compose file that defines your services.
- `README.md`: This is the README file that documents your project.

## Container Side
Inside the Docker containers, the file structure will look like this:

### VictoriaMetrics Container

```
/
└── victoria-metrics-data
```

- `/`: This is the root directory of the VictoriaMetrics container.
- `victoria-metrics-data`: This is the directory where VictoriaMetrics stores its data. It’s mapped to a Docker volume for data persistence.

### Grafana Container

```
/
└── var
    └── lib
        └── grafana
```

- `/`: This is the root directory of the Grafana container.
- `var/lib/grafana`: This is the directory where Grafana stores its data. It’s mapped to a Docker volume for data persistence.
Please note that these are the basic file structures based on the Docker Compose file. Depending on your specific needs and configuration, you might have additional files and directories.