# Fn - Quick installation on a Linux Host

  Below are the steps to follow:
  
  - Make sure docker is installed in the host
  - Download and Install Fn
  - Start the Fn Server
    
## 1. Make sure docker is installed in the host
    docker --version
    docker ps
  
## 2. Download and Install Fn
    curl -LSs https://raw.githubusercontent.com/fnproject/cli/master/install | sh

## 3. Start the Fn Server
    fn start
