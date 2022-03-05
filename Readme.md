## Instructions

### Step 1:
Open this project in Visual Studio Code (VSCode).
Ensure you have the Azure Functions extension installed.

https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azurefunctions

Open the Azure icon (in the activity tab) and under the Functions sidebar drawer it should detect the configuration files in this project.

### Step 2:
Install sintra (a ruby micro web framework) using ruby's package manager bundler.

```
bundle install
```

### Step 3:

Use the install script to download portable ruby, an embedded build of ruby for linux x86 architectures.
```
./install.sh
```

### Step 4:

Intall the Azure Functions Core Tools

https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local?tabs=v4%2Clinux%2Ccsharp%2Cportal%2Cbash

