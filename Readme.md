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

### Step 5

A local.settings.json file needs to be created.
```
{
    "IsEncrypted": false,
    "Values": {
        "AzureWebJobsStorage": "connection-string-url"
    }
}
```
You need to supply a connection string url to a Storage Account.

### Step 6

In hte bin.real/bundler the path to ruby needs to be updated.
```
#!/workspace/azure-functions-ruby-sample/portableruby/bin/ruby
```

### Step 7

Download the precompiled ruby version you want:
https://rubies.travis-ci.org/

The version we are using is 3.1.0
curl -O https://rubies.travis-ci.org/ubuntu/20.04/x86_64/ruby-3.1.0

untar the ruby archive
```
tar -xvjf ruby-3.1.0.tar.bz2 
```

```
ruby-3.1.0/bin/bundle exec 'ruby-3.1.0/bin/bundle' install
```

### Step 8:

```
func start --custom
```