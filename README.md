# crossplane-composite-examples

Examples of Crossplane Composite Resources and how to implement them

TODO:

* AWS RDS
* AWS EC2
    * autoscaling-group


## AWS S3

To provision an S3 bucket with a requirement for `region` and `Owner` tag.

Install composite: `kubectl apply -f aws/s3`

Example claim:

```
apiVersion: example-api.kjenney.io/v1alpha1
kind: Bucket
metadata:
  name: my-bucket
spec:
  region: eu-central-1
  owner: whoeveryoulike
```

## AWS RDS

To provision an RDS database with a requirement for `region` and `Owner` tag.

Install composite: `kubectl apply -f aws/rds`

Example claim:

```
apiVersion: example-api.kjenney.io/v1alpha1
kind: Database
metadata:
  name: whatever-you-want-to-call-me
spec:
  region: us-east-2
  owner: anownerofyourchoice
```
