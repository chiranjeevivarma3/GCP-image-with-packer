create a service account in GCP with permission Compute Instance Admin (v1) & Service Account User and editor 
Then download the json file which has crendatials
copy the service account name 
install packer on your machine
fill the vars.json file ( understanding about variables  https://www.packer.io/docs/builders/googlecompute)
verfiy package.json file
change shell script name in package.json
validate the script with below command
    packer validate -var-file=vars.json package.json (output should be succesfully)
To Build image below command
    packer build  -var-file=vars.json package.json
To Debug 
    packer build -debug -var-file=vars.json package.json