# example-versioning-dvc

poetry run dvc init

copy the data

poetry run dvc add data/

git add .gitignore data.dvc

Configure  remote storage 

poetry run dvc remote add -d storage /Users/marco/Documents/dvc_storage_test
