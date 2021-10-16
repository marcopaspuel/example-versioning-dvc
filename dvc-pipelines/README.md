# DVC Data Pipelines 

Import a dataset
```bash
poetry run dvc import https://github.com/iterative/dataset-registry get-started/data.xml -o data/data.xml
```

Update the dataset to the latest version 

```bash
poetry run dvc update data/data.xml.dvc
```
