# tf-learning

resource "type" "name"
using the provider, create type of resource. Name is how we refer to it internally within terraform code

```
terraform init
terraform plan
terraform apply
terraform destroy
```

### Why is the state file so important?
keeps track of everything you've created and will be used when you delete things (e.g. `terraform destroy`)

### Securely storing AWS keys
Technically you can pass them in code:
provider "aws"{
    region = "ap-southeast-2"
    access_key = "123"
    secret_key = "abc"
}

Better options:
- Env vars (AWS_ACCESS_KEY_ID & AWS_SECRET_ACCESS_KEY)
- AWS CLI
- Vault provider

### Dynamic imports
Don't use too many, makes code complicated

#### vscode plugins to potentially remove
- terraform autocomplete
