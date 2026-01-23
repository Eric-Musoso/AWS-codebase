
## Created our bucket
```sh 
aws s3 mb s3://prefixes-musoso-1267
```

## Created folder
```sh
aws s3api put-object --bucket="prefixes-musoso-1267" --key="hello/"
```