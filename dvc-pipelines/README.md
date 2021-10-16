# DVC Data Pipelines 

Import a dataset
```bash
poetry run dvc import https://github.com/iterative/dataset-registry get-started/data.xml -o data/data.xml
```

Update the dataset to the latest version 

```bash
poetry run dvc update data/data.xml.dvc
```

# Create a DVC pipeline

```bash
poetry run dvc run -n prepare \
                   -p prepare.seed,prepare.split \
                   -d src/prepare.py -d data/data.xml \
                   -o data/prepared \
                   python src/prepare.py data/data.xml
```
