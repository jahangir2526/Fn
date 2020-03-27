# Build, Deploy and Run a Java Function (Local Fn Server)

This is used to demonstrate how to build, deploy and run java function in a local Fn Server. All the steps and commands have been collected from Fn Documentations.

Below are the steps to follow:
    
## 1. Make sure Fn is installed locally and Fn server is running
    fn version

## 2. Make sure docker is installed 
    docker --version
    docker ps
  
## 3. Create and initialize a java function
    fn init --runtime java javafn
    cd javafn
    cat func.yaml

## 4. Check the current context
    fn list contexts
    
## 5. Create a new Application. Function will reside in the application
    fn create app java-app
    
## 6. Deploy the function on local Fn server
     fn --verbose deploy --app java-app --local
     
## 7. Invoke the function in command line
    fn invoke java-app javafn
    echo -n 'Jahangir' | fn invoke java-app javafn

## 8. Invoke the function using cURL
    fn inspect function java-app javafn
    curl -X "POST" -H "Content-Type: application/json" http://localhost:8080/invoke/XXXXXXXXXXXXXXXXXXXXX

## 9. You can pass JSON data to our function and get the value of name passed to the function back.
    curl -X "POST" -H "Content-Type: application/json" -d '{"name":"Jahangir"}' http://localhost:8080/invoke/XXXXXXXXX

