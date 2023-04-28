# Mini-projet
Mini-projet : Déployez une infra complète
Description
Ce mini-projet consiste à déployer une infrastructure AWS complète à l'aide de modules Terraform. L'infrastructure comprend une instance EC2 avec un volume EBS, une adresse IP publique, un groupe de sécurité et une installation de Nginx sur l'instance EC2.

# Structure du projet
app/
│── main.tf
│── variables.tf
│── providers.tf
module/
├── ec2/
│   ├── ec2.tf
│   ├── variables.tf
│   └── outputs.tf
├── ip_publique/
│   ├── eip.tf
│   ├── variables.tf
│   └── outputs.tf
├── security_group/
│   ├── securitygroup.tf
│   ├── outputs.tf
├── ebs/
│   ├── ebs.tf
│   │── variables.tf

# Utilisation
Clonez le projet à l'aide de la commande suivante :
git clone https://github.com/yassinejab/mini-projet.git
Accédez au répertoire cloné :
cd mini-projet/app
Initialisez Terraform :
terraform init
Vérifiez le plan d'exécution :
terraform plan
Exécutez le plan :
terraform apply
Après l'exécution réussie de Terraform, l'adresse IP publique de l'instance EC2 sera enregistrée dans un fichier nommé ip_ec2.txt situé dans le répertoire "..\Mini Projet\app"
Vous pouvez également détruire l'infrastructure à l'aide de la commande suivante :
terraform destroy

# Notes
Le projet a été testé avec Terraform version 1.0.5 et la dernière version d'Ubuntu Bionic.
Il est recommandé de ne pas stocker les fichiers de configuration .tfvars et les fichiers d'état Terraform dans votre dépôt Git public.




