# Spark-Databrick-Community

### Pré-requisitos:
- [Azure CLI](https://learn.microsoft.com/pt-br/cli/azure/)
- [Visual Studio Code](https://code.visualstudio.com/download)
- [Terraform](https://www.terraform.io/downloads)
- Conta de e-mail Microsoft específica para esta atividade


### Roteiro:


#### 1
```bash  copy
az login
```

#### 2. Consultar o nome do Resource Group criado para a sua conta do Concierge Subscription
```bash copy
az group list -o table
```
#### 3. Ajustar a variável *resource_group_name* do arquivo `variables.tf` com o nome do Resource Group informado no passo anterior
```terraform
variable "resource_group_name" {
  default = "learn-877e311a-66ab-401b-9372-06326c9bd083"
}
```

#### 4. Criar os recursos na assinatura Azure selecionada

##### 4.1.
```bash copy
terraform init
```
##### 4.2.
```bash copy
terraform validate
```
##### 4.3.
```bash copy
terraform fmt
```
##### 4.4.
```bash copy
terraform plan
```
##### 4.5.
```bash copy
terraform apply
```
##### 4.6. 
5. Logar no [portal.azure.com](https://portal.azure.com/) e conferir o deploy do ADLS.

#### 6
Configurar no seu DataBricks a conexão com o Conteiner da Azure

#### 7
I,portar e rodar arquivo .dbc deste repositório dentro de um notebook

