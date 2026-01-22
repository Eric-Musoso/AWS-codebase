## Create a new s3 bucket

```md
aws s3 mb s3://checksums-examples-ms-2342
```

## Create a file that will do a checksum on
```
echo "Hallo Musoso" > myfile.txt
```

## Get a checksum of a file for md5

```
md5sum myfile.txt
## eb85307af20bd53c7b7c2b0d72647fcd  myfile.txt
```
## Upload our file and look at its etag

```
aws s3 cp myfile.txt s3://checksums-examples-ms-2342
aws s3api head-object --bucket checksums-examples-ms-2342 --key myfile.txt
```