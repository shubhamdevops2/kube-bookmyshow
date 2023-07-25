# Node.js URL shorten project

This project is created to understand the architecture of shorten URL application which generates the short URL from the given long hsoted URL.

Example -

**Input URL ->** https://en.wikipedia.org/wiki/Artificial_intelligence , 
**Output URL ->** http://localhost:3000/70ovli4d


##

![architecture image.png](https://github.com/shubhamdevops2/kube-bookmyshow/blob/main/architecture%20image.png)

To accomplish this we have created three microservices as below:

1) URLshorten repository- [frontend](https://github.com/shubhamdevops2/bookmyshow_urlshorten)
2) handler repository- [handler for application and database](https://github.com/shubhamdevops2/bookmyshow_handler)
3) mongodb - Backend mongodb database

##

### URLshorten frontend 

This application serves as a frontend that communicates exclusively with the handler server. It facilitates the seamless sharing of data with the handler server, which, in turn, manages the storage and retrieval of data in the backend MongoDB database.

### Handler server

This server functions as a middleware between the front-end and backend applications, facilitating the communication and passing API requests between the two. It acts as an intermediary, enabling seamless interaction and data exchange between the front-end and backend components of the application.

### MongoDB 

The image used to run this backend server is obtained from the **public Docker Hub**, simplifying the deployment process

This backend server serves as the data storage and retrieval component for the frontend application. It is responsible for handling API requests and interacting with the public Docker Hub to fetch images as needed. The data from the frontend is stored in the backend database, and the backend server facilitates the retrieval of this data when requested by the frontend.

##

### Ingress

Our microservices deployment benefits from load balancing using NGINX Ingress as the Kubernetes Ingress load balancer. It efficiently distributes incoming traffic among the microservices, provides routing and path-based traffic management, handles seamlessly connecting clients to the appropriate backend microservices.

## Please read the below files for the microservices kuberenetes architecture

1) URLshorten - urlshorten-definition.yaml
1) Handler - handler-definition.yaml
1) MongoDB - mongodb-definition.yaml
4) Ingress - ingress.yaml
