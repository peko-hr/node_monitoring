# ethereum-monitoring

## 完成物
- Grafana container

- prometheus container
  - 各サーバのnode exporterの監視
  - Geth(EC) metricsの監視
  - Prysm(CC) metricsの監視
  - Prysm(VC) metricsの監視

- alertmanager container

## Grafana,Prometheusを構築し、起動する

- git cloneします
```sh
git clone https://github.com/peko-hr/ethereum-monitoring.git
```

- `compose.yml`を編集します
```sh
cd monitoring
vi compose.yml
```
`extra_hosts`に監視対象を設定します。


- configを変更します
```sh
cd /prometheus/config
vi prometheus.yml
```
各targetを変更しましょう。
targetはIPアドレスでの指定も可能です。
