# Low level solution

## DB structure

This diagram uses classDiagram to provide a visual representation of your data model and the relationships between entities. Each class has its attributes listed and relationships are represented by lines with varying types of connectors to indicate the nature of the relationship (e.g., composition, association).

![db_structure2](/db_structure2.png)


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
    + Expectation_id: one
    + Requirement_id: many
    + TestData_id: many
    + Description: string    

+ Component
    + id  
    + type: file, class, function, url
    + input: DataModel
    + output: DataModel
    + comments: string
    + license: string
    + autor: string

+ TestData
    + id
    + input_value: DataValue
    + output_value: DataValue
    + input_type: DataModel
    + output_type: DataModel

DataValue
    + id
    + type
    + value
    + format


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
    + Component_id: Component
    + Environment_id: Environment
    + Documentation_id: one
    + Component_id: many
    + Stage: prototype, local, test, production
    
      
## Monitoring

 + Logs
    + id
    + Deployment_id
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

+ [edit](https://github.com/ModuleTool/docs/edit/main/2/README.md)
+ [git](https://github.com/ModuleTool/docs/)
