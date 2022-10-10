## springboot-microservice-project
Spring boot project CURD operations with REST API and Microservices. 



Run all the projects one by one in following order.
-discovery
-gateway
-profile
-txns
-statement



Open POSTMAN and hit the following URLS


Eureka discovery server
localhost:9000



#PROFILES(port:9100)


-@GetMapping("/{ahid}")
 localhost:9100/1


-@GetMapping("/{ahid}/exists")
 localhost:9100/1/exists


-@PostMapping
 localhost:9100
 
 Json Body:
 {
    "firstName":"Mitesh",

    "lastName":"Pawanarkar",

    "mailId":"miteshpawanarkar@gmail.com",

    "mobile":9819854737

 }

-@PutMapping
 localhost:9100
 
 Json Body:
 {

    "ahId":1,

    "firstName":"Mitesh",

    "lastName":"Pawanarkar",

    "mailId":"miteshpawanarkar@gmail.com",

    "mobile":9819854737

 }



#TXNS(port:9200)

-@PostMapping    localhost:9200

Json Body:
{

"header":"Salary",

"amount":650000,

"type":"CREDIT",

"dateOfTransaction":"2022-07-01",

"holder":{

"ahId":2

}
    
    }

@GetMapping("/{ahId}/balance")
localhost:9200/1/balance

@GetMapping("/{ahId}/{from}/{to}")
localhost:9200/1/2022-07-09/2022-10-09

@DeleteMapping("/{txnId}")
localhost:9200/1




#STATEMENT(port:9300)

- @GetMapping("/{ahId}/{year}")
 localhost:9300/1/2022

- @GetMapping("/{ahId}/{year}/{month}")
 localhost:9300/1/2022/July











------------------------------------------------------------------------------------------------------------------------------------------------------------------------

##For educational purpose


<<Http Status Code>>


POST-201 CREATED


GET-200 OK


PUT-202 ACCEPTED,


DELETE-204 NO CONTENT


500 internal server error


404 not found




