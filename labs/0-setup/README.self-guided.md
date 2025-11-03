# Setup For Self-Guided Learners

    🚨🚨🚨 TRACING ENV NEEDS MANUAL UPDATE - TODO: FIX IT 🚨🚨

Use this guide if you are exploring this workshop on your own, at home. To do this you will need:

- A personal GitHub account - [signup here for free](https://github.com/signup)
- An active Azure account -  [signup here for free](https://aka.ms/free)
- A laptop with a modern browser - we recommend Microsoft Edge
- Some familiarity with - Git, VSCode, Python & Jupyter notebooks
- Some familiarity with - Generative AI concepts and workflows

<br/>

## 1. Fork This Repo

1. If you already have a fork of the repo, just pull the latest changes to get ready.
1. If you don't have a fork already, [use this link](https://github.com/microsoft/ignite25-PREL13-observe-manage-and-scale-agentic-ai-apps-with-azure-ai-foundry/fork) to create one in your GitHub proile.
1. Open a new browser tab and navigate to that fork in the browser.

## 2. Launch GitHub Codespaces

1. Click the blue "Code" button in that GitHub page to see options
1. Select the "Codespaces" tab and click "+" to launch a new codespace
1. This opens a new tab with a VS Code IDE - wait till that loads completely

## 3. Authenticate With Azure

1. Open a new terminal session in that VS Code window - wait till ready.
1. Run this command - and complete the workflow with **your** Azure subscription

    ```bash title="" linenums="0"
    az login
    ```
1. _We can now use this for managed identity credentials in code later_.

<br/>

## 4. Provision AI Agents Template

1. The [Azure Developer CLI](https://aka.ms/azd) streamlines provsioning and deployment for AI Apps.
1. The [AI Apps Gallery](https://aka.ms/ai-apps) has a number of curated AI application templates for AZD.
1. In this repo, we have scripts to setup of the [Get Started With AI Agents](https://github.com/Azure-Samples/get-started-with-ai-agents) template

**Let's Run the scripts in order**: _we recommend the defaults below_.

1. Change working directory: `cd scripts/`
1. Run the setup script: `./1-setup.sh`
1. Enter branch name: `msignite25-lab516`
1. Enter environment name: `ignite-PREL13`
1. Enter Azure region: `swedencentral`
1. Enter Subscription ID: _your subscription id here_
1. Do you want to activate Azure AI Search? (yes/no) [no]: yes
1. Use these defaults? (yes/no) [yes]: yes
1. Proceed with deployment? (yes/no): yes

<details>
<summary> ➡️ ➡️ CLICK TO EXPAND FOR DETAILS </summary>

**By completing this step you will see:** 

1. A local folder created: `scripts/ForBeginners` - cloned from our custom repo
1. An azd template inside: `scripts/ForBeginners/.azd-setup` - with infra-as-code
1. Our azd environment: `scripts/ForBeginners/.azd-setup/ignite-PREL13` with:
    - a `config.json` - with environment configuration
    - a `.env` - with environment variables from our infra deployment
1. The deployment process will also begin - watch the console for updates.
    1. Make sure you have the required model quotas and access permissions.
    1. The process will take 10-15 minutes to complete.

    ```
    SUCCESS: Your up workflow to provision and deploy to Azure completed in 14 minutes 5 seconds.
    ✓ Infrastructure deployed successfully

    ======================================
    Setup Complete!
    ======================================
    ✓ Repository cloned
    ✓ Environment configured
    ✓ Infrastructure deployed
    ✓ Azure AI Search enabled (Index: zava-products)
    ======================================
    ```

1. Populate the `.env` file from the provisioned environment variables

    ```
    ./6-get-env.sh
    ```

    The script will automatically:
    - ✅ Extract the correct Azure AI Project name from your deployment
    - ✅ Retrieve Azure OpenAI API key programmatically
    - ✅ Retrieve Azure AI Search API key programmatically
    - ✅ Use the correct OpenAI endpoint format (`.openai.azure.com`)
    - ✅ Configure Application Insights connection string

    You should see output like:

    ```
    ✅ Successfully updated .env file!

    📋 Updated Variables:
      • Resource Group: rg-ignite-PREL13
      • Location: swedencentral
      • OpenAI Endpoint: https://aoai-XXXXXXX.openai.azure.com/
      • OpenAI API Key: ✓ Retrieved
      • AI Search Endpoint: https://srch-XXXXX.search.windows.net/
      • AI Search API Key: ✓ Retrieved
      • AI Project Name: proj-XXXXX
      • Container Registry: XXXX.azurecr.io
      • Service API URI: https://ca-api-XXX...
      • Application Insights: ✓ Connected

    💡 All API keys have been automatically retrieved from Azure!

    💡 All API keys have been automatically retrieved from Azure!

    ======================================
    ✓ Done!
    ======================================
    ```


1. Now populate products and update the search index

    ```
    python 2-add-product-index.py 
    ```

    You should see something like this:

    ```
    ======================================================================
    Add Products to Azure AI Search Index
    ======================================================================
    Using environment variables from system/default locations
    ✓ Azure CLI authentication verified
    Running RBAC update script to ensure proper permissions...
    ..
    ..
    Uploading 49 products to index 'zava-products'...
    ✓ Successfully uploaded 49 products to the search index!

    The product catalog is now ready for semantic search.
    ======================================================================
    ```

1. Now, lets add the models you need to explore customizaton.

    ```
    ./2-add-models.sh 
    ```

    You should see something like this:

    ```
    ========================================
    Add Additional Model Deployments
    ========================================

    ℹ️  Checking prerequisites...
    ✓ Prerequisites check passed
    ℹ️  Using standalone Bicep template: customization/add-models.bicep

    ========================================
    Currently Deployed Models
    ========================================

    ✓ gpt-4.1
    ✓ text-embedding-3-large

    ========================================
    Available Models to Deploy
    ========================================
    ...
    ...

    Select models to deploy (enter numbers separated by spaces, e.g., '1 3 5'):
    Or type 'all' to deploy all available models, or 'cancel' to exit:
    > all
    ...
    ...

    ✓ Additional models deployed successfully!
    ✓ Environment variable updated with deployment configuration

    ========================================
    Deployment Summary
    ========================================
    ✓ model-router deployed
    ✓ gpt-4o deployed
    ✓ gpt-4o-mini deployed
    ✓ gpt-4.1-mini deployed
    ✓ gpt-4.1-nano deployed
    ✓ o3-mini deployed
    ✓ o4-mini deployed
    ========================================

    ✓ Model deployment completed successfully!
    ```
</details>

<br/>

## 4b. Optional: Using Pre-Existing Infra

This section is relevant ONLY if you had already completed the deployment previously, and are now launching a new GitHub Codespaces to work with your pre-existing deployment. The goal is to refresh environment variables from existing infrastructure.

1. In this case, respond with `no` to the "Proceed ith deployment?" question.
1. Then switch to location containing template: `cd ForBeginners/.azd-setup`
1. Login with azd: `azd auth login` - complete workflow with Azure subscription
1. Then run the `azd env refresh` command - wait till it completes
1. Your `scripts/ForBeginners/.azd-setup/ignite-PREL13/.env` will get updated!

<br/>

## 5. Complete Your Labs

_Your infrastructure is now ready! You can now launch the instruction guide and start working through the labs!_.

1. Open a new terminal in VS Code.
1. Type `mkdocs serve` - wait a few seconds to see the pop-up dialog
1. Confirm you want to open this in browser.
1. _You should see an instruction guide for labs in website preview_. 

**Start with the Validate Setup lab - then keep going**:

1. First, run the `0-setup/00-validate-setup.ipynb` notebook
1. Verify that all required environment variables were set!
1. Then keep going down the list in the instruction guide.


<br/>

## 6. Teardown & Cleanup

When you are all done with labs, you want to tear down the infrastructure _and_ delete the cloned template sources from your repo. Make sure you are in the `scripts/` folder then run this command:

```bash title="" linenums="0"
./3-teardown.sh
```

You will see:

```bash title="" linenums="0"
Starting teardown process...
Found ForBeginners directory
Checking for AZD environments...
Found AZD environment: nitya-Ignite-PREL13
======================================
WARNING: This will delete all Azure resources
======================================
Tear down Azure infrastructure? (yes/no): 
```

Respond with "yes" - and wait till complete. This will take 15-20 minutes to unprovision the resource group and purge resources. _You can now use the `./1-setup.sh` script if you want to restart install from scratch_.