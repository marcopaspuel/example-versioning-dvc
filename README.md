# example-versioning-dvc

```bash
poetry run dvc init
```

copy the data

```bash
poetry run dvc add data/
```

```bash
git add .gitignore data.dvc
```

Configure  remote storage 

```bash
poetry run dvc remote add -d storage /Users/marco/Documents/dvc_storage_test
```

```bash
poetry run dvc push
```

Remove one of the images 

```bash
rm data/0000021_00500_d_0000002.jpg
```

Remove the local dvc cache

```bash
rm -rf .dvc/cache/
```

Pull again the deleted image 

```bash
poetry run dvc pull
```

Then we can modify the data by adding one image

and then we can add this image to dvc

```bash
poetry run dvc add data/
```

Push the new version of the dataset to the remote storage

```bash
poetry run dvc push
```

Check the git log
```bash
git log --oneline
```

Checkout the previous version of the DVC file 

```bash
git checkout HEAD^1 data.dvc
```

then 

```bash
poetry run dvc checkout
```

If I want to commit the changes I can commit this with

```bash
git commit data.dvc -m "Revert dataset updates"
```
