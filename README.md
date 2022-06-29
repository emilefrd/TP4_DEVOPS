## DEVOPS - TP4 - DEVOPS  - Terraform 101
## FARAMOND Emile - EFREI - M1 BDIA APP


![logo_terraform](https://img-0.journaldunet.com/5dyx1x7c8hipe3JS92vWnli_LIc=/1500x/smart/f628d3865a7f4ba4ab1f125beba18a58/ccmcms-jdn/19946149.jpg)

### Objectifs  

> Créer une machine virtuelle Azure (VM) avec une adresse IP publique

> Utiliser Terraform  

> Se connecter à la VM avec SSH  

> Comprendre les différents services Azure (ACI vs. AVM)  

> Mettre à disposition son code dans un repository Github

>   Aide :  [Terraform Providers](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/guides/azure_cli#loggin )

### Pré-requis : 
> Installer Azure CLI : La documentation est dispo au lien : [Install Azure CLI](https://docs.microsoft.com/fr-fr/cli/azure/install-azure-cli-linux?pivots=apt)

Pour ma part, sur ubuntu : 
```bash
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```
puis pour s'identifier sur azure :
```
az login
```
> Installer Terraform : La documentation est dispo au lien : [Install Terraform](https://learn.hashicorp.com/tutorials/terraform/install-cli)

Attention : il faut s'asurer d'avoir la bonne version de Terraform (Terraform v0.14.3)


### Exécution

````bash
terraform init 
````
![alt text](screenshots/init.png)

````bash
terraform plan 
````
![alt text](screenshots/plan.png)


````bash
terraform apply
````
![alt text](screenshots/apply.png)
![alt text](screenshots/apply2.png)

````bash
terraform output
````
![alt text](screenshots/output.png)

### 8. Connexion à la VM Azure avec SSH

````bash
ssh -i privateKey.txt devops@<ma_clé_publique_VM> cat /etc/os-release
````

````bash
$ terraform destroy
````
