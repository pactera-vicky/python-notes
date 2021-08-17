# step of deploy terraform on GCP

## install terraform on GCP VM
1.[link](https://www.terraform.io/downloads.html)

2.steps(MACos)

    `curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -`

    `sudo apt-add-repository "deb [arch=$(dpkg --print-architecture)] https://apt.releases.hashicorp.com $(lsb_release -cs) main"

    `sudo apt-get install terraform`
3. download your code

4. modify **.tf

5.cd terraform directory and execute the commands

    `terraform init`
    `terraform plan`
    `terraform apply`


  
