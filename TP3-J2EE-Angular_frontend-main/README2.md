# TP3-J2EE-Angular_frontend

## Command lines
    
    // terminal
        npm install --save bootstrap bootstrap-icons
    
    // then add this line at angular.json
    
          "styles": [
              "src/styles.css",
              "node_modules/bootstrap/dist/css/bootstrap.min.css"
            ],
            "scripts": [
              "node_modules/bootstrap/dist/js/bootstrap.bundle.js"
            ]
     
     // to create a component
            
            ng g c products
            
     // to communicate with the api : import HttpClientModule to app.module.ts
     
     // EXPLICATION : CORS POLICY PROB :
     
        before sending (GET PUT DELETE POST) Request to an other domain name - the app send OPTION request to see if he has the authorization to communicate with the other server 
