# RentManager

Rentmanager : Application web pour une agence de location de voiture permettant de gérer les clients, véhicules et réservation

-----------------------------------------------------------------------------------------------------------------------------------	 
// CONFIGURATION L'ENVIRONNEMENT //
-----------------------------------------------------------------------------------------------------------------------------------	

 1. Vous devez avoir préalablement installé Eclipse JEE 2020 et Tomcat v9 ou un IDE equivalent. 
 2. Le projet doit avoir les versions des modules suivants (Facet properties) :
 	- Dynamic Web Module 4.0
 	- Java 1.8
 	- Javascript 1.0


-----------------------------------------------------------------------------------------------------------------------------------	
// DEMARAGE //
-----------------------------------------------------------------------------------------------------------------------------------	

Exécutez le programme via le "Home Servlet" sur le serveur local (Run on server)


-----------------------------------------------------------------------------------------------------------------------------------	
// FONCTIONNALITES //
-----------------------------------------------------------------------------------------------------------------------------------	

	- Basique : lister, ajouter, modifier et supprimer les clients, vehicules et réservations
	
    - Gestion des erreurs et contraintes métier suivantes : 
    	* un client n'ayant pas 18ans ne peut pas être créé
        * un client ayant une adresse mail déjà prise ne peut pas être créé
        * le nom et le prénom d'un client doivent faire au moins 3 caractères
        * une voiture ne peux pas être réservé 2 fois le même jour
        * une voiture ne peux pas être réservé plus de 7 jours de suite par le même utilisateur
        * une voiture ne peux pas être réservé 30 jours de suite sans pause 
        * si un client ou un véhicule est supprimé, alors il faut supprimer les réservations associées
        * une voiture doit avoir un modèle et un constructeur, son nombre de place doit être compris entre 2 et 9
        
    - Fontionnalités disponible en mode console (CliControler) a éxécuter en tant que java application et non sur le serveur
    
    - Architecture en 3 niveaux : 
    	1. Classes objets "model" (clients, vehicle etc..)
    	2. Classes secondaires "Dao" assurant la liaison avec la BDD SQL
    	3. Classes Tertiaires "Services" assurant les contraintes métier
    	4. Les controllers "Servlet" assurant l'interraction entre l'utilisateur et l'application web

        

-----------------------------------------------------------------------------------------------------------------------------------	
//AUTEURS// : Noémie LEMAIRE - EPF 4A - P2021 - MIN
-----------------------------------------------------------------------------------------------------------------------------------															
