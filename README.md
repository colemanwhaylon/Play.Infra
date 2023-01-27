# Play.Infra

Play Economy Infrastructure components

## Add the GitHub package source

```powershell
$owner="colemanwhaylon"
$gh_pat="[PAT HERE]"

dotnet nuget add source --username USERNAME --password $gh_pat --store-password-in-clear-text --name github "https://nuget.pkg.github.com/$owner/index.json"
```

## Creating the Azure resource group

```powershell

$appname="playeconomy01262024"
az group create --name $appname --location eastus
```

## Creating the Cosmos DB account

```powershell
as cosmosdb create --name $appname --resource-group $appname --kind MongoDB --enable-free-tier

```

## Creating the Service Bus namespace

```powershell

az servicebus namespace create --name $appname --resource-group "playeconomy" --sku Standard
```
