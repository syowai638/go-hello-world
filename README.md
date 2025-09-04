# Getting Started with Go (Golang) - Beginner's Toolkit

A simple HTTP server built with Go to help beginners learn the basics of the Go programming language.

## 🎯 Project Objective

This project demonstrates how to:
- Set up a Go development environment
- Create a basic HTTP server
- Handle routing and responses
- Run and test a Go application

## 📋 Technology Overview

**Go (Golang)** is a statically typed, compiled programming language developed by Google. It's known for:
- Simple syntax and easy learning curve
- Excellent performance
- Built-in concurrency support
- Strong standard library
- Great for web services, APIs, and CLI tools

**Real-world example:** Docker, the containerization platform, is built using Go.

## 🛠️ System Requirements

- **OS:** Linux, macOS, or Windows
- **Tools:** Text editor (VS Code recommended with Go extension)
- **Memory:** Minimum 2GB RAM
- **Storage:** Minimum 1GB free space

## 📦 Installation & Setup

### Installing Go on Ubuntu


```bash
# Update package list
sudo apt update

# Install Go using snap (recommended)
sudo snap install go --classic

# Verify installation
go version
# Expected output: go version go1.24.2 linux/amd64
```
 ## Setting Up Your Workspace

```bash
# Create project directory
mkdir ~/go-projects
cd ~/go-projects

# Create hello-world project
mkdir hello-world
cd hello-world

# Initialize Go module
go mod init hello-world
```

## 🚀 Running the Application

```bash
# Create the main.go file

nano main.go
## Paste the following code:

package main

import (
    "fmt"
    "net/http"
)

func main() {
    http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
        fmt.Fprintf(w, "Hello World from Go!")
    })

    fmt.Println("Server starting on port 8080...")
    err := http.ListenAndServe(":8080", nil)
    if err != nil {
        fmt.Printf("Server failed to start: %v\n", err)
    }
}

```
## Run the Server

```bash
go run main.go

## Expected output:
Server starting on port 8080...
```

## Test the Server

 ## Using curl:

 ```bash
curl http://localhost:8080

## Using web browser:

Navigate to http://localhost:8080

## Expected response:

Hello World from Go!
```

## 🤖 AI Prompt Journal

### Prompt 1:
"Give me a step-by-step guide to install Go on Ubuntu and create a simple Hello World web server"

**AI Response Summary:** [Briefly describe what the AI provided]

**Helpfulness:** 10/10 - Comprehensive and immediately usable.

### Prompt 2:
"What are common errors when starting with Go and how to fix them?"

**AI Response Summary:** [Briefly describe the AI's response]

**Helpfulness:** 9/10 - Anticipated problems beginners might encounter.

### Prompt 3:
"How do I structure a basic Go project and what should be in the go.mod file?"

**AI Response Summary:** [Briefly describe the AI's response]

**Helpfulness:** 9/10 - Clarified modern project structure.


## 🐛 Common Errors & Solutions

"command not found: go"

Solution: Go isn't installed or not in PATH. Reinstall using instructions above.

"cannot find module providing package"

Solution: Run go mod tidy to sync dependencies.

"port already in use"

Solution: Change port number in code or stop the other process using port 8080.

"permission denied" when binding to ports below 1024

Solution: Use port above 1024 or run with sudo (not recommended).

"expected 'package', found 'go'"

Solution: File doesn't start with package main. Recreate file correctly.

Cut buffer is empty in nano

Solution: Use system paste (Ctrl+Shift+V) instead of Nano's internal paste.


## 📚 Learning Reflections

[Add 2-3 paragraphs about your experience learning Go - what was easy/hard, surprises, etc.]

## 🔗 Reference Resources

- **Official Go Documentation:** https://golang.org/doc/
- **Go Tour:** https://tour.golang.org/
- **Go by Example:** https://gobyexample.com/
- **Awesome Go:** https://awesome-go.com/

## 📞 Support

If you encounter issues:
1. Check the "Common Errors & Solutions" section
2. Consult the official Go documentation
3. Search Stack Overflow with [go] tag

## 📄 License

This project is open source and available under the MIT License.

