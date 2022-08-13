# install Prometheus

```
wget https://github.com/prometheus/prometheus/releases/download/v2.37.0/prometheus-2.37.0.linux-amd64.tar.gz
tar -zxvf prometheus-2.37.0.linux-amd64.tar.gz
cd prometheus-2.37.0.linux-amd64
nohup ./prometheus &
```
Then ,visit  http://localhost:9090

# install grafana
```
sudo apt-get install -y adduser libfontconfig1
wget https://dl.grafana.com/enterprise/release/grafana-enterprise_9.0.7_amd64.deb
sudo dpkg -i grafana-enterprise_9.0.7_amd64.deb
```
