# example-versioning-dvc

poetry run dvc init

copy the data

poetry run dvc add data/

git add .gitignore data.dvc

Configure  remote storage 

poetry run dvc remote add -d storage /Users/marco/Documents/dvc_storage_test

poetry run dvc push

Remove one of the images 

rm data/0000021_00500_d_0000002.jpg

Remove the local dvc cache

rm -rf .dvc/cache/

Pull again the deleted image 
poetry run dvc pull

Then we can modify the data by adding one image

and then we can add this image to dvc

poetry run dvc add data/
