# dotnet-core-web-api
A simple dontet core web api tutorial

# Deploying on GCP (billing must be enabled for flex environments)
dotnet publish -c Release
cd ~/src/mymicroservice 
gcloud app deploy bin/Release/netcoreapp2.0/publish/app.yaml

# Calling the API
/api/values/1
curl -i -H "Accept: application/json" -H "Content-Type: application/json" -X GET http://localhost:8080/api/values/1
