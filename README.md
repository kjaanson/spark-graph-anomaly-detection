Kagandi Graph Anomaly implementatsioon Spark GraphX-il

Kagandi koodi allatirimiseks:
```
git clone https://github.com/Kagandi/anomalous-vertices-detection.git
```

Twitteri dataseti allatirimiseks:
```bash
(cd /data/kagandi_twitter & wget http://proj.ise.bgu.ac.il/sns/datasets/twitter_fake_ids.csv)
(cd /data/kagandi_twitter & wget http://proj.ise.bgu.ac.il/sns/datasets/twitter.csv.gz & gunzip twitter.csv.gz)
```

Et käivitada vihikut analüüsiks jooksutada juurkataloogis:
```bash
docker run --name graph-anomaly-detection-spark -e SPARK_DRIVER_MEMORY=8g -e SPARK_EXECUTOR_MEMORY=2g -v `pwd`:/home/jovyan/ -p 8888:8888 jupyter/all-spark-notebook
```

