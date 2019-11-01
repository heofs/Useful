# Google Cloud Platform


## Change active account

`gcloud auth list`

`gcloud config set account 'ACCOUNT'`

## Change active project

`gcloud projects list`

`gcloud config set project 'PROJECT ID'`

## Set default region

For function deploy

`gcloud config set functions/region europe-west1`

## Cloud Functions

Deploying http function

`gcloud functions deploy myFunction --runtime nodejs10 --trigger-http`
