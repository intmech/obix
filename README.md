# obix
node-red flows for interacting with tridium niagara systems via obix

How to ssetup a Niagara 4 Station to be able to communicate via oBIX

Step #1 

obix needs https in niagara 4

In Niagara 4 Station/Services/WebService view:AXpropertySheet 
-> turn on https 
-> specify https port

Step #2 

obix needs a driver installed in the station

In Niagara 4 Station/Config/Drivers 
-> New -> Type to Add = Obix Network

Step #3

obix user needs a non default authentiation scheme

In Niagara 4 Station/Services/AuthenticationService/AuthenticationSchemes 
-> Add from Palette
baja/AutheticationSchemes/WebServicesSchemes/HTTPBasicScheme

Step #4

obix need’s a user account with admin rights on the Niagara station

In Niagara 4 Station/Services/UserService 
-> Duplicate Admin User 
-> name obixUser 
-> got to new obixUser's ax property sheet 
-> set password 
-> change AuthenticationSchemeName = HTTPBasicScheme

