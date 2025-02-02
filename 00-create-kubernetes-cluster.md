# Installing Pulumi CLI

To start with Pulumi, you need to install the CLI. Go to https://www.pulumi.com/docs/iac/download-install/ 
and follow the instructions that apply to your machine. 

Once you have installed the CLI, verify that it works via the following command:
```shell
> pulumi version
v3.147.0
```
You are now ready to create your first Pulumi application. 

# Create a Pulumi account

When using infrastructure as code tools, we typically keep track of deployed resources in some sort of _state_ backend. 
Pulumi CLI saves the state of your program in our own Pulumi Cloud backend where you can manage your projects, collaborate with teammates and use shared secrets.

The Pulumi Cloud backend is optional and can be replaced with other state backends such as an S3 bucket on AWS, a blob storage on Azure or even locally on your machine
but in this workshop we will be using Pulumi Cloud. 

Start by running `pulumi login` and follow the instructions to connect the CLI with your Pulumi Cloud account after you've created it.

# Creating A New Project

Once the CLI is installed and your account connected, you can create a new project
```
pulumi new <language>
```
Where `<language>` is your language of choice for writing your infrastructure code.

You will need to run this command in an empty directory and `cd` into it so the command become:
```shell
mkdir digitalocean-pulumi-workshop
cd digitalocean-pulumi-workshop
pulumi new typescript
```
The snippet above creates an empty project in the TypeScript language, but you can choose another language such as 
`go`, `python`, `csharp`, `go` or `yaml`. Pulumi supports all of these. We will have snippets in all of these languages.

