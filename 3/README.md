# ModuleTool Implementation


## DB structure

This diagram uses classDiagram to provide a visual representation of your data model and the relationships between entities. Each class has its attributes listed and relationships are represented by lines with varying types of connectors to indicate the nature of the relationship (e.g., composition, association).

![db_structure3](/db_structure3.png)


### Specification

+ Expectation
    + id  
    + description  
    + role: customer, manager

+ Requirement
    + id
    + description

+ DataModel
    + id
    + language: php, js, python
    + name: domain, url, host, 
    + type: file, class, function, url
    + format: json, html, yaml, text, string, integer, bool    




### Implementation

+ Documentation
    + Expectation: one
    + Requirement: many
    + TestData: many
    + Description: string    

+ Component
    + id  
    + type: file, class, function, url
    + input: DataModel
    + output: DataModel
    + comments: string
    + license: string
    + autor: string


+ DataValue
    + id
    + type
    + value
    + format

      
+ TestData
    + id
    + input_value: DataValue
    + output_value: DataValue
    + input_type: DataModel
    + output_type: DataModel



### Iteration


+ Environment
    + id
    + type: local, remote, vm  
    + configuration: docker, docker-comopse
    + volume
    + service
    + Stage: prototype, local, test, production

      
+ Deployment
    + id    
    + Documentation: one
    + Component: many
    + Environment: many     
    + Stage: prototype, local, test, production
    
      
## Monitoring

 + Logs
    + id
    + Deployment: one
    + Message
    


## Iteration

```php
try{
    // component
}catch e {
    // logs messages
}
```


---

+ [edit](https://github.com/ModuleTool/docs/edit/main/3/README.md)
+ [git](https://github.com/ModuleTool/docs/)
