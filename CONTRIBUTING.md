# Contributing to MetaCall FaaS

## Windows Development

To develop and test MetaCall FaaS on Windows, please follow these steps:

### 1. Install MetaCall CLI
Run the following command in PowerShell:
```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
Invoke-WebRequest -Uri https://raw.githubusercontent.com/metacall/install/master/install.ps1 -OutFile install.ps1
.\install.ps1
```

### 2. Setup Environment
Ensure that the MetaCall installation directory is in your `PATH`. By default, it is located at `%LocalAppData%\MetaCall`.

### 3. Run Unit Tests
Unit tests are platform-agnostic and can be run on Windows:
```powershell
npm install
npm run build
npm run test
```

> [!NOTE]
> Integration tests currently rely on Docker Compose and Bash scripts, and are primarily supported on Linux environments. They are skipped in the Windows CI.
