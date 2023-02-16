# TP_J2EE_Micro_Services
- Première partie : (Customer-Service, Inventory-Service, Spring Cloud Gateway, Eureka Discovery) - 
- Deuxième Partie : Billing Service avec Open Feign Rest Client
- Troisième Partie :      Créer un Client Angular, 

Créer une application basée sur une architecture micro-service qui permet de gérer les factures contenant des produits et appartenant à un client.

Travail à faire :


1.Créer le micro-service customer-service qui permet de gérer les client

![Service_Customer_Service](https://user-images.githubusercontent.com/74791123/206469138-e046e9cd-7ca8-4374-a34d-26f2251ef9a7.PNG)

2.Créer le micro-service inventory-service qui permet de gérer les produits

![Service_Inventory_Service](https://user-images.githubusercontent.com/74791123/206469581-41b923b1-6a4b-4b65-9d68-db1e12731e71.PNG)

3. Créer la Gateway Spring cloud Gateway avec une Configuration statique du système de routage
      ==>Extrait de code qui montre la Configuration statique
      
      ![Code_Service_Gateway](https://user-images.githubusercontent.com/74791123/206472850-9347d7ec-42eb-44c4-a24c-b02ff65ddb4b.PNG)
      
      ==>Capture d'ecran qui montre l'execution de la Gateway (voir URL)
                                **** Inventory Service ****
                                
      ![Gateway_Service_Products](https://user-images.githubusercontent.com/74791123/206473722-8399293e-fa89-4949-95e8-db8827e881bf.PNG)
      
                                **** Customer Service ****
                                
      ![Gateway_Service_Customers](https://user-images.githubusercontent.com/74791123/206474730-551c1175-f0ce-4fab-a723-6b8e4a29c92f.PNG)

4. Créer l'annuaire Eureka Discrovery Service

![Spring_Eureka](https://user-images.githubusercontent.com/74791123/206470101-48dd7129-50dc-4be3-ad36-c8fd0d331e46.PNG)

5. Faire une configuration dynamique des routes de la gateway

        ==>Extrait de code qui montre la Configuration dynamique
        
![Gateway_Dynamic](https://user-images.githubusercontent.com/74791123/206479030-7529e3a9-7cfe-46a2-bdab-6e579f5e8975.PNG)


        ==>Capture d'ecran qui montre l'execution de la Gateway Dynamiquement (voir URL)
        
                                        **** Inventory Service ****
                                        
![Inventory_Dynamique_Gateway](https://user-images.githubusercontent.com/74791123/206479091-6b02e8d3-0e02-4387-b9be-de5b57165566.PNG)

                                        **** Customers Service ****
                                        
![Customers_Dynamique_Gateway](https://user-images.githubusercontent.com/74791123/206479204-98c98886-6538-4c6a-8b5e-f759e21ceb87.PNG)


6. Créer le service de facturation Billing-Service en utilisant Open Feign

![Billing_Service](https://user-images.githubusercontent.com/103313351/217521924-eabf07dd-7e9e-45aa-ba5c-71c56fcc0f40.PNG)


7. Créer un client Web Angular (Clients, Produits, Factures)



8. Déployer le serveur keycloak :
     - Telecharger et demarrer Keycloak
     
     
     ![1  Télécharger Keycloak](https://user-images.githubusercontent.com/103313351/219461512-b755fbbd-c520-4d15-b575-9dfce60cc6d7.PNG)


![2  Démarrer Keycloak](https://user-images.githubusercontent.com/103313351/219461544-5f090573-95e4-4ba1-90e4-132263af70de.PNG)
      
      -Créer un admin
      
      ![3  creer cpt admin](https://user-images.githubusercontent.com/103313351/219461645-0f36a434-3943-4344-85ed-5f27ca8bb0fc.PNG)

      ![3  Créer un compte Admin](https://user-images.githubusercontent.com/103313351/219461742-370f8c56-b0ba-4d61-8ef7-ea714550bd20.PNG)


     - Créer un Realm
     
     ![4  Créer une Realm](https://user-images.githubusercontent.com/103313351/219461721-70f3612a-4841-48b6-9225-36e6cea4c11b.PNG)

     
     - Créer un client à sécuriser
     
     ![5  Créer un client à sécuriser](https://user-images.githubusercontent.com/103313351/219461797-6ec21010-21ce-4db8-bbf9-4692957257f2.PNG)

     
     - Créer des utilisateurs
     
     ![6  Créer des utilisateurs](https://user-images.githubusercontent.com/103313351/219461823-a38ed1ca-eec4-4906-ac03-d1bfec73da34.PNG)

     
     - Créer des rôles
     
     ![7  Créer des rôles](https://user-images.githubusercontent.com/103313351/219461864-7b1447de-46cb-4288-af6c-456ea0d401f2.PNG)

     
     - Affecter les rôles aux utilisateurs
     
     ![8  Affecter les rôles aux utilisateurs](https://user-images.githubusercontent.com/103313351/219461900-df90a11e-6a21-4976-8728-225e7c2886c9.PNG)

     
     - Tester les différents modes d'authentification avec Postman en montrant les contenus de Access-Token, Refresh Token 
     
     I/
     
     ![POSTMAN Tester auth Client ID et Client Secret](https://user-images.githubusercontent.com/103313351/219462151-a8173f31-4f7e-4711-9ffd-d9395e532ee1.PNG)


      II/
      
      ![POSTMAN Tester auth Refresh Token](https://user-images.githubusercontent.com/103313351/219462214-b3a5bc41-b133-45d9-bf67-d799159f03db.PNG)
      
      III/
      
      ![POSTMAN  Tester auth avec mdp](https://user-images.githubusercontent.com/103313351/219462318-a763c1d7-058f-4e3f-ae3c-c7dbd880f404.PNG)
     
9. Sécuriser les micro-services et le frontend angular en déployant les adaptateurs Keycloak

![POSTMAN Analyser les contenus des deux JWT Access Token et Refresh Token](https://user-images.githubusercontent.com/103313351/219462425-a5260501-fb74-4567-a8a1-0489bed9ca87.PNG)


![POSTMAN Changer les paramètres des Tokens Access Token et Refresh Token](https://user-images.githubusercontent.com/103313351/219462447-e2d3a55d-cf24-49cc-8059-44d5134b4fa1.PNG)
