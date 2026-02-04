# antigravity-wsl
안티 그래비티 WSL 환경에서 사용 검증

## .NET 10 Setup in WSL (Ubuntu 24.04)

This project verifies running .NET 10 applications in a WSL environment.

### Prerequisites
- **WSL Version**: 2
- **Distribution**: Ubuntu 24.04 LTS
- **Dependency**: `dotnet-install.sh` script needed for .NET 10 (as it's not in default repo yet).

### Installation Steps
1.  **Install .NET 10 SDK**:
    ```bash
    curl -L https://dot.net/v1/dotnet-install.sh -o dotnet-install.sh
    chmod +x dotnet-install.sh
    ./dotnet-install.sh --channel 10.0
    ```
    *Installed Path*: `~/.dotnet/`

2.  **Configure Environment**:
    Add the following to your shell configuration (or run before executing):
    ```bash
    export DOTNET_ROOT=$HOME/.dotnet
    export PATH=$DOTNET_ROOT:$PATH
    ```

3.  **Run Hello World**:
    ```bash
    cd hello-wsl
    dotnet run
    ```

### Current Status
- [x] Verified WSL Connection
- [x] Installed .NET 10 SDK
- [x] Created & Ran "Hello World" Console App
