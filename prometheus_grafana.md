# install Prometheus

```
wget https://github.com/prometheus/prometheus/releases/download/v2.37.0/prometheus-2.37.0.linux-amd64.tar.gz
tar -zxvf prometheus-2.37.0.linux-amd64.tar.gz
cd prometheus-2.37.0.linux-amd64
nohup ./prometheus  --web.enable-lifecycle &
```
Then ,visit  http://localhost:9090

# install grafana
```
sudo apt-get install -y adduser libfontconfig1
wget https://dl.grafana.com/enterprise/release/grafana-enterprise_9.0.7_amd64.deb
sudo dpkg -i grafana-enterprise_9.0.7_amd64.deb
```

then start grafana
```
sudo systemctl start grafana-server
sudo systemctl status grafana-server
```
using admin/admin to login web

# add data source
![image](https://user-images.githubusercontent.com/1063747/184475103-16c61bca-5ba3-4c62-86da-3096b0ed8fe9.png)

# install node exporter
```
wget https://github.com/prometheus/node_exporter/releases/download/v1.4.0-rc.0/node_exporter-1.4.0-rc.0.linux-amd64.tar.gz
tar -zxvf node_exporter-1.4.0-rc.0.linux-amd64.tar.gz
cd ~/node_exporter-1.4.0-rc.0.linux-amd64
nohup ./node_exporter &
```
then add target to prometheus.yml ,reload
` curl -X POST http://192.168.111.132:9090/-/reload `
