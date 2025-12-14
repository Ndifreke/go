# The Go Programming Language

Go is an open source programming language that makes it easy to build simple,
reliable, and efficient software.

## ⚙️ Go Language: Unrestricted Compiler Fork

This repository contains a customized fork of the official Go Programming Language source code based off v1.26.

**Key Difference:** This version has the compiler's strict checks for **unused imports and unused variables** intentionally disabled.

### ⚠️ IMPORTANT NOTE

The standard Go compiler normally enforces these checks to promote clean, maintainable, and efficient code. This fork sacrifices those checks, allowing code with unused elements to compile successfully. Use this version only if you understand and accept the potential trade-offs.


### 🛠️ Building from Source

To use this unrestricted version of Go, you must compile the toolchain from the source code.

1.  **Clone the Repository:**

    ```bash
    git clone https://github.com/Ndifreke/go.git
    cd go
    ```

2.  **Navigate to Source and Build:**
    Use an existing Go installation (Go 1.4+ is required for bootstrapping) to build the new toolchain.

| Operating System | Command |
| :--- | :--- |
| **Unix or Mac** | `cd src && ./make.bash` |
| **Windows** | `cd src && make.bat` |

### 🚀 Usage

After a successful build, the new Go executables will be located in the `bin` directory of your cloned repository.

To use this version, set the `GOROOT` and update your `PATH` environment variable:

```bash
# Example for Linux/macOS
export GOROOT=$(pwd)  # Point to the root of this repo
export PATH=$GOROOT/bin:$PATH

# Verify the version:
go version
```

This setup ensures that when you run `go build` or `go run`, you are using the modified compiler that ignores unused imports and variables.
