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

Push the new version of the dataset to the remote storage
poetry run dvc push

Check the git log
git log --oneline


Checkout the previous version of the DVC file 

git checkout HEAD^1 data.dvc

then 

poetry run dvc checkout


If I want to commit the changes I can commit this with

git commit data.dvc -m "Revert dataset updates"
