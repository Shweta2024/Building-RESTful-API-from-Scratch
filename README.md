## What is REST & RESTful?

- REST stands for :  **RE**presentational
**S**tate
**T**ransfer

- REST : It is an architectural style to build APIs. 

- RESTful : APIs which is built by following the REST Architecture are called RESTful APIs.


- Some other Architectural styles for designing APIS are :- **GraphQL**, **Soap**, **Falcor** etc.

<br>

## Architectural Constraints/ Priciples

An API is called RESTful if it follows the below **06** constraints :

<h3>1. Client-Server </h3>


> Servers & clients may also be replaced and developed independently as long as the interface between them is not altered.

The client and the server applications MUST evolve separetely without any dependency on each other. A client should know only the resource URLs.


<h3> 2. Stateless </h3>


Make all client-server interactions stateless. The server will not be able to store anything about the latest HTTP request made by the client. It'll treat every request as a new one. **No session, no history**.

Each request from the client to the server should contain all the information necessarly to understant & complete request including authentication & authorization details.

> No client context shall be stored on the server between requests. The client is responsible for managing the state of the application.


<h3> 3. Cacheable </h3>

> Well-managed caching can partially or completely eliminate some client-server interactions, futher improving performance & scalibility.


<h3> 4. Layered System </h3>

> We can have an intermediate layer between the client & the server. This layer can offer additional feature like security, load balancing, caching etc.

Example : Suppose we have deployed the APIs on server A and stored data on server B and we are authenticating the requests in server C.

<h3> 5. Uniform Interface </h3>
 
 It is the core to design a REST API. It contains **04** constraints : 
 
 - **Identification of Resources** : The interface must uniquely identify each resource involved in the intercation bertween the client & the server.
 
 - **Manipulation of resources through representations** : The resources should have uniform representation in the server response. API consumer/client should use these representations to modify the resources state(modify/delete) in the server.
 
 - **Self-descriptive Messages** : Each resource representation should carry enough information to describe how to process the message. It should also provide information of the additional actions that the client can perform on the resource.
 
 - **Hypermedia as the engine of application state** : After accessing a resource the client should be able to take all the currently available actions using hyperlinks.
 

<h3> 6. Code on Demand (*Optional) </h3>

This is an **Optional** constraint. Servers can extened the functionality of ther client by transfering executable code/files to them.

<br>

## Comparision of HTTP requests with CRUD operations in DB :- 
- **GET** is similar to **READ**
- **POST** is similar to **CREATE**
- **PUT** & **PATCH** is similar to **UPDATE**
- **DELETE** is similar to **DELETE**

Difference between **PUT** & **PATCH**?

- **PUT** : It updates a document by completely replcing it with another document.

- **PATCH** : It  updates a document by updating a specific field of document.


We need to perform the below operations :- 

![WhatsApp Image 2022-12-20 at 7 12 11 PM](https://user-images.githubusercontent.com/75883328/208681247-34f018cc-dd17-4008-aff7-6a989f05e732.jpeg)
