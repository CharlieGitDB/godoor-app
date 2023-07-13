# godoor-app
A property and event management app

## Setup
### Forking
*If you're not forking this repo then skip this portion.*  

**Prerequisites**
1. An Azure Subscription
2. The az cli installed  

**Secret Setup**  
You will need to create a service principal to be able to run the Github Actions (CI/CD).  
1. Run in your terminal `az ad sp create-for-rbac --name myApp --role contributor --scopes /subscriptions/{subscription-id} --sdk-auth`
2. Copy the output
3. Go to Settings > Secrets and variables > Actions > New Repository Secret
4. Paste the output into a secret with the value `AZURE_CREDENTIALS`
5. Create a secret called `AZURE_RG` that is the name of your resource group
6. Create a secret called `AZURE_SUBSCRIPTION` that is the value of your subscription id
