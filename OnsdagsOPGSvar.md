## 1) Monitoring HTTP Headers 1
- Der bliver sendt et GET request med en URL
- vi modtager derefter en statuskode 200, hvilket betyder at alt gik godt.
- Ændre vi dermimod index.html til index1.html får vi en 404 fejl som outputter en file not found fejl i headeren.
  
## 2) Monitoring HTTP Headers 2
- her får vi en 304 status kode på index.html som indikere at der ikke er blevet gjordt nogle ændringer siden sidste request og derfor bliver requestet ikke transmitteret.
- css og image er blevet tilføjet og kan nu ses som GET metoder også.
- I connection headeren ser vi at den er keep-alive.

## 3) 
- her får vi redirect og r.html
  - Redirect giver en 302 status kode og viser samtidig hvilken url vi har requestet samt hvilken location vi sendes til. nemlig r.html
  - r.html giver en status kode 200.
  - URL'en er hermed og ændret til at outputte r.html til sidst.

## 3a) Redirecting to HTTPs instead of HTTP
- Her møder jeg som den første GET request status kode 301 (permantly moved) som siger at det ikke er en sikker forbindelse og jeg ikke er det rigtige sted. jeg bliver derfor redirected til en https URL og giver dermed en satus kode 200. Nu viser den hjemmesiden og jeg er det rigtige sted.

## 4a) Status Codes (5xx)
- Vi får en status kode 500 som er en serverfejl og dermed ikke klienten som har lavet en fejl.

## 4b) Status Codes (4xx)
- Vi får en status kode 404 (file not found) som siger at siden ikke findes og klienten har lavet en fejl.

## 4c) Status Codes Ranges


## 6) Get/post-parameters
- her sender vi et GET request og får en status kode 200 fordi at alt er gået godt. 
- i URL'en stå der nu: http://localhost:8080/Onsdag02_09_2020/getPost6.html?fname=a&lname=2&hidden=12345678#
  - vi har altså fået vores fornavn og efternavn med som parametre i URL'en.
- Ændre vi metoden i HTML'formen til POST får vi igen en status kode 200 for at alt gik fint til, men nu har vi # med som parameter i URL'en istedet for fornavn og efternavn.
http://localhost:8080/Onsdag02_09_2020/getPost6.html#
  
## 7) Sessions (Session Cookies)
- A
  - Giver os mulighed for at indsætte request parametre.

- B
  - Jeg skriver /SessionDemo?=name=alex når jeg køre filen.
  - Giver muligheden for at indtaste mit navn og giver efterfølgende en welcome alex side.

- E
  - Det nuværende state opretholdes via en session cookie
  - Slettes denne session-cookie vil formularen dukke op igen og der skal dermed tastes navn på ny.

## 8) Persistent Cookies
- A
  - Her ser vi vi cookies levetid osv. Den session cookie der bliver sat lever utroligt længe og også selvom browseren lukkes helt.
  Nedenunder ses et billede af de 2 cookies vi får.
<img src="Annotation 2020-09-02 165142.png">
  