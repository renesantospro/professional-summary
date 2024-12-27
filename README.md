# home_page

https://cloud.google.com/storage/docs/hosting-static-website#command-line_1

https://cloud.google.com/storage/docs/hosting-static-website-http#command-line_1


gcloud storage managed-folders create gs://renesantos_pro/site/
gcloud storage managed-folders add-iam-policy-binding gs://renesantos_pro/site --member=allUsers --role=roles/storage.legacyObjectReader


gcloud storage buckets add-iam-policy-binding  gs://my-static-assets --member=allUsers --role=roles/storage.objectViewer
gcloud storage buckets add-iam-policy-binding  gs://my-static-assets --member=allUsers --role=roles/storage.legacyObjectReader


http://storage.googleapis.com/BUCKET_NAME/OBJECT_NAME
https://storage.googleapis.com/renesantos_pro/site/index.html