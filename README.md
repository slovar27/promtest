# promtest

docker run -p 9090:9090 -v /path/to/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus

docker run -d --name prom1 -p 9090:9090 --network mynet --ip 192.168.0.30 -v /zz/promtest/prometheus/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus:v2.31.1

# reload new configuration
docker exec prom1 killall -HUP prometheus


https://jenkins1.alexeytools.com/job/metrics1/lastSuccessfulBuild/artifact/metrics1.txt

# HELP prometheus_tsdb_head_samples_appended_total Total number of appended samples.
# TYPE prometheus_tsdb_head_samples_appended_total counter
prometheus_tsdb_head_samples_appended_total 1832
# HELP prometheus_tsdb_head_series Total number of series in the head block.
# TYPE prometheus_tsdb_head_series gauge
prometheus_tsdb_head_series 556

# HELP car speed

