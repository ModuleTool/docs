# docs.ModuleTool.com

+ Service-based component management tools

## DB structure  

### Prototype

+ Expectation
  + id
  + description

+ Requirements
  + id
  + description
  + input
    + object_type: domain, url, host, 
    + object_format: file, class, function, url
  + output
    + object_type: domain, url, host, 
    + object_format: file, class, function, url

+ Module
  + id  
  + parent_id
  + language: php, js, java
  + format: file, class, function, url
  + value

+ Implementation
  + Expectation_id
  + Requirements_id
  + Module_id
  + Stage: prototype, local, test, production

  
### Service

+ Object
  + Type: domain, url, host, 
  + Format: json, html, yaml, text, string, integer, bool
+ View
+ Query  



## How to use?

Build Prototype
+ Preparing specification based on customer **expectations**
+ Creating **Requirements** based on customer **expectations**
+ Creating **Modules** based on **Requirements** defined based on the customer **expectations**

Run Prototype
+ SELECT query on Implementation table to get the the list of modules necessary to generate the network of modules

Customer usage
+ SELECT QUERY on VIEW through saved QUERY to get the DATA Object
  

---
+ [edit](https://github.com/ModuleTool/docs/edit/main/README.md)
+ [git](https://github.com/ModuleTool/docs)
