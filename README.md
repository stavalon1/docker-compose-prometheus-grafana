## docker-compose is sample.
### Prometheus & Grafana
Project structure:</br>
.
</br>├── docker-compose.yml</br>
├── grafana</br>
   └── datasource.yml</br>
├── prometheus</br>
    └── prometheus.yml</br>
└── README.md

## Deploy with docker-compose
<p>$ docker-compose up -d</br>
Creating network "prometheus-grafana_default" with the default driver</br>
Creating volume "prometheus-grafana_prom_data" with default driver</br>
...</br>
Creating grafana    ... done</br>
Creating prometheus ... done</br>
Attaching to prometheus, grafana
</p>

### Expected result

Navigate to http://localhost:3000 in your web browser and use the login credentials specified in the compose file to access Grafana. It is already configured with prometheus as the default datasource.

![output](https://user-images.githubusercontent.com/66349803/184905903-04d38017-f047-4efa-8805-7ac689398d27.jpg)

Navigate to http://localhost:9090 in your web browser to access directly the web interface of prometheus.
Stop and remove the containers. Use -v to remove the volumes if looking to erase all data.<br>
$ docker-compose down -v
