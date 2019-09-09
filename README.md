## terraform-bundle

- terraform-bundle is a helper program to create "bundle archives", which are zip files that contain both a particular version of Terraform and a number of provider plugins.

### Building
- clone a terraform repo into the following folder
```
git clone https://github.com/hashicorp/terraform.git $GOPATH/src/github.com/hashicorp/
cd $GOPATH/src/github.com/hashicorp/terraform
go install ./tools/terraform-bundle
```
- The last command will create and add to the path a 'terraform-bundle' binary, which is located into:
```
$ ll $GOPATH/bin/terraform-bundle
```
- Now we can prepare our configuration file - [Usage](https://github.com/hashicorp/terraform/tree/master/tools/terraform-bundle#usage)
- start building a bundle zip file:
```
terraform-bundle package terraform-bundle.hcl
```
- For the test I have created terraform and last aws provider:
```
terraform
terraform-provider-aws_v2.27.0_x4
```
