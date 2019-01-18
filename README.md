## terraform-gke
test guestbook app

## project structure

```
├── README.md
├── gke
│   ├── cluster.tf
│   ├── gcp.tf
│   └── variables.tf
├── k8s
│   ├── k8s.tf
│   ├── pods.tf
│   ├── services.tf
│   └── variables.tf
└── main.tf
```

How to run project

Auth and define json with credentials
```
gcloud auth application-default login
export GOOGLE_APPLICATION_CREDENTIALS="/home/terr/test-k8s-226sdf015-c2sd43rrf73c.json"
```

```
export TF_VAR_project="$(gcloud config list --format 'value(core.project)')"
export TF_VAR_region="us-east1"
export TF_VAR_user="admin"
export TF_VAR_password="pass"

```
Export project ID

```
export TF_VAR_project="test-k8s-244015"
```

Run k8s cluster with app

```
terraform init

terraform plan

terraform apply
```

For termination 

```
terraform destroy
```
