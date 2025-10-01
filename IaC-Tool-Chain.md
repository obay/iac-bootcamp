# IaC Tool Chain Setup

## PowerShell 7

Download & install from the following link:
- https://github.com/PowerShell/PowerShell/releases/download/v7.4.5/PowerShell-7.4.5-win-x64.msi

## Microsoft Terminal

Download & install from the following link:
- https://github.com/microsoft/terminal/releases/download/v1.21.2701.0/Microsoft.WindowsTerminal_1.21.2701.0_x64.zip

## Windows Subsystem for Linux (WSL): Ubuntu

Install WSL from the following link:
- [Install WSL | Microsoft Learn](https://learn.microsoft.com/en-us/windows/wsl/install)

Or using the command below:
```bash
wsl --install -d Ubuntu-24.04
```

## Scoop.sh (PowerShell)

Website: https://scoop.sh/

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

## Brew (WSL)

Download & install from the following link:
- [Homebrew — The Missing Package Manager for macOS (or Linux)](https://brew.sh/)

Or directly using the following command:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Azure CLI

Download & install from the following link:
- [Install the Azure CLI for Windows | Microsoft Learn](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows)

Or directly using the following link:
- https://azcliprod.blob.core.windows.net/msi/azure-cli-2.64.0-x64.msi

### Azure CLI - Commands

To login to Azure:
```bash
az login
```

To login to specific Azure tenant:
```bash
az login --tenant <tenant_id>
```

To see logged in subscription:
```bash
az account show
```

To set working subscription:
```bash
az account set --subscription <subscription_name>
```

### Azure CLI – Setup SSL Certificate

You can specify a custom SSL certificate when using the Azure CLI by setting the `REQUESTS_CA_BUNDLE` environment variable to point to your certificate file. This allows the Azure CLI to use your custom certificate authority (CA) bundle for SSL validation instead of skipping it altogether.

Here's how you can set it up:

**Linux / macOS:**
```bash
export REQUESTS_CA_BUNDLE=/path/to/your/certificate.crt
```

**Windows (PowerShell):**
```powershell
$env:REQUESTS_CA_BUNDLE="C:\path\to\your\certificate.crt"
```

After setting this environment variable, the Azure CLI will use the specified certificate for SSL validation. Ensure that the path points to a valid certificate file in `.crt` or `.pem` format. This method is more secure than disabling SSL verification entirely, as it allows you to control which certificates are trusted.

## Azure PowerShell Module

Download & install from the following link:
- [Install Azure PowerShell on Windows | Microsoft Learn](https://learn.microsoft.com/en-us/powershell/azure/install-azps-windows)

Or directly using the following command:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Install-Module -Name Az -Repository PSGallery -Force
```

## jq

**On Windows:** Install using the following command:
```powershell
scoop install jq
```

**On Linux:** Install using the following command:
```bash
brew install jq
```

## Terraform

**On Windows:** Install using the following command:
```powershell
scoop install terraform
```

**On Linux:** Install using the following command:
```bash
brew install terraform
```

## Git

**On Windows:** Install using the following command:
```powershell
scoop install git
```

**On Linux:** Install using the following command:
```bash
brew install git
```

## OpenTofu

**On Windows:** Install using the following command:
```powershell
scoop install opentofu
```

**On Linux:** Install using the following command:
```bash
brew install opentofu
```

## Visual Studio Code

Download & install from the following link:
- [Download Visual Studio Code - Mac, Linux, Windows](https://code.visualstudio.com/download)

Or directly from:
- https://vscode.download.prss.microsoft.com/dbazure/download/stable/d78a74bcdfad14d5d3b1b782f87255d802b57511/VSCodeUserSetup-x64-1.94.0.exe

## Cursor

Download & install Cursor from the following link:
- https://downloader.cursor.sh/windows/nsis/x64

## Notepad++

Download & install from the following link:
- [Downloads | Notepad++](https://notepad-plus-plus.org/downloads/)

## GitHub Copilot for Visual Studio

Download & install from the following link:
- [GitHub Copilot overview (visualstudio.com)](https://visualstudio.microsoft.com/github-copilot/)

## ChatGPT

- Create an account in ChatGPT and use it to get code samples and command line help
- Creating an account allows you to go back to your history and allows ChatGPT to give you results based on your previous search if you choose to.

## Configuration

### AZ CLI

- Make sure AZ CLI is logged in to Azure with required access (`az login`)
- Make sure you can see the subscription you are currently logged in to (`az account show`)
- Make sure you see all subscriptions you have access to (`az account list`)

### Azure PowerShell Module

- Make sure Azure PowerShell module is logged in to Azure with required access (`Connect-AzAccount`)
- Make sure you can see the subscription you are currently logged in to (`Get-AzContext`)
- Make sure you see all subscriptions you have access to (`Get-AzContext -ListAvailable`)
