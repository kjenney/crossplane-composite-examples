# crossplane-composite-examples

Examples of Crossplane Composite Resources and how to implement them

TODO:

* AWS RDS
* AWS EC2
    * autoscaling-group


## AWS S3

To provision an S3 bucket with a requirement for `region` and `Owner` tag.

```
kubectl apply -f aws/s3/bucket_crd.yaml
kubectl apply -f aws/s3/bucket_composite.yaml
kubectl apply -f aws/s3/bucket_claim.yaml
```